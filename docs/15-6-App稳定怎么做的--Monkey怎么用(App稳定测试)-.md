## 15-6-App稳定怎么做的--Monkey怎么用(App稳定测试)-

稳定性这块，我们当时用的是SDK自动的一个 Monkey工具进行测试的，其实 Monkey工具主要通过模拟用户发送伪随机时间去操作软件，通过执行 Monkey命令，它会自动出报告，执行测试大概在10万次，每个动作的间隔时间250ms，主要就是看软件长时间，随机乱操作的情况，是否会出现异常，闪退，崩溃等现象。

一般我都是在下班的时间晚上时间执行 Monkey命令，并把生成的报告导出到电脑端，大概需要6、7小时，第二天早上看报告，分析报告，如果出现问题，一般利用上次执行的那个种子值，再进行执行命令进行复测一下，

像 monkey命令：

adb shell monkey -p com.xy.android.junit -s 种子值 --throttle 250  --ignore -crashes --ignore -timeouts -monitor-native-crashes -v -v 100000 > E:\monkey_log\monkey_log.txt

这里主要关注几个点，1、指定种子值 2、忽路一些异常，保证能正常执行完成

3、设置间隔时间 4、配置一些时间比例  5、然后就是执行的次数。

对于报告怎么分析这块，主要看有不有 CRASH(崩溃)，ANR(超时无响应)， Exception(异常)等的情况像看有不有空指针异常( NullPointException)啊，0OM等现象啊等等，

找到 CRASH崩溃ANR超时无响应 Exception异常的位置，看出现错误的上一个动作是什么，什么做了什么动作导致错误出现。异常信息会详细的指出哪个 Activity出现了问题，甚至于哪个函数出问题了，具体哪个位置。然后把报告中出现的日志信息截图发给开发，开发修复完成之后，我们会根据种子值在进行复测一下。

稳定性这块我们当时就是这么做的。

我在运行 monkey发现过很多的问题我就简单的说几个问题，举个例子在查看 monkey运行日志中

(1)  com.androidserver.am.NativeCrashListener.run(NativeCrashListener.java：129)

属于本地监听代码导致的崩溃，手机监听代码导致的崩溃，他是手机产生的原因，不是代码的原因不做处理。

(2) ∥Short Msg:java.lang.IllegalArgumentException传参异常：需要一个stng类型，给我一个int类型

(3) ∥Short Msg:java.lang.NullPointerException  空指针异常

(4) ∥Short Msg:Native crash 本地代码导致的奔溃

(5) (com.koudaizhekou.tbk/com.uzmap.pkg.EntranceActivity)  超时无响应

等等等……
