# 学习机通用case

- 学习机是一个复杂的系统，有很多全局功能，全局应用；局部应用或功能开发的时候，一定要关注和全局应用的关联和影响情况。
  
## 平板的通用case，开发中要关注的


- 1）切换应用至后台：

    - 若视频在暂停状态，切后台再回来仍暂停状态；

    - 若视频正在播放模式，切后台先暂停再回来继续播放；

- 2）切换至多任务：

    - 若视频在暂停状态，切多任务再回来仍暂停状态；

    - 若视频正在播放模式，切多任务先暂停再回来继续播放；

- 3）来第三方通话-视频通话：

    - 若视频在暂停状态，视频通话再回来仍暂停状态；

    - 若视频正在播放模式，视频通话则先暂停再回来继续播放；

- 4）来第三方通话-语音电话：

    - 若视频在暂停状态，语音通话再回来仍暂停状态；

    - 若视频正在播放模式，语音电话先暂停再回来继续播放；

- 5）语音助手小x：

    - 若视频在暂停状态，唤起小x再回来仍暂停状态；

    - 若视频正在播放模式，唤起小x先暂停关闭小帮继续播放；

- 6）闹钟：

    - 若视频在暂停状态，闹钟关闭再回来仍暂停状态；

    - 若视频正在播放模式，闹钟打断先暂停关闭闹钟继续播放；

- 7）护眼提醒：

    - 若视频在暂停状态，护眼提醒关闭再回来仍暂停状态；

    - 若视频正在播放模式，护眼提醒先暂停关闭护眼提醒继续播放；

- 8）时间管控：

    - 视频在暂停状态，时间管控（延长）关闭再回来仍暂停状态；

    - 若视频正在播放模式，时间管控先暂停调整时间管控（延长）继续播放；
 
    - 说明：若时间管控未调整（未调整）走系统统一的管控模式。

- 9）低电量提醒：

    - 若视频在暂停状态，低电量提醒关闭再回来仍暂停状态；

    - 若视频正在播放模式，低电量提醒先暂停关闭低电量提醒继续播放；

- 10）充电：

    - 若视频在暂停状态，充电开启仍暂停状态；

    - 若视频正在播放模式，充电不打断播放模式；

- 11、解绑：

    - 解绑走系统模式，播放视频环节无特殊处理

- 12、杀进程：

    - 杀进程动作进行时视频播放模式变为暂停，若本身未暂停模式仍保持

- 13、升级：

    - 若视频在暂停状态，升级弹窗关闭仍暂停状态；

    - 若视频正在播放模式，升级弹窗出现则暂停，关闭弹窗则继续播放；

- 14、锁屏/息屏：

    - 若视频在暂停状态，锁屏/息屏后开启仍暂停状态；

    - 若视频正在播放模式，锁屏/息屏视频暂停播放开启后继续播放（待定）

- 15、蓝牙设备：键盘、耳机对音频和输入的影响

- 16、网络-弱网（1-5k）：

    - 若视频在暂停状态，弱网仍可以进行暂停动作，若无法实现需呀有提示语告知用户。

    - 若视频正在播放模式，有对应的逻辑。

- 17、网络-断网：

    - 若视频在暂停状态，弱网仍可以进行暂停动作，若无法实现需呀有提示语告知用户。

    - 若视频正在播放模式，有对应的逻辑。

- 18、贴反光镜：

    - 若视频在暂停状态，贴反光镜仍保持暂停状态

    - 若视频正在播放模式，贴反光镜则暂停播放，贴反光镜动作结束继续播放（待定）

- 19、切换导航：三键导航和手势导航


- 20、切换年级：

    -切换年级中断且关闭正在解读的视频。

- 21、应用双开

    - 彼此互不影响，尤其是语音，视频等逻辑

- 22、loading及回退

    - 不能出现空白页，要么有loading，要么有数据；要给用户明确的展示。

等等，音视频、UI布局，手写笔等一些全局变更会导致重新刷新和变化，一定要关注；否则迭代过程中会出现很多bug。