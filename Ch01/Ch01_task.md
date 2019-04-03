https://gitlab.com/101camp/py/blob/master/ch01.md
# ch01: CLI 是朋友
> command-line interface 命令行界面的缩写

就是大家不时会看到的黑漆漆的一个窗口,里面运行得快速滚动的不明代码/字符的东西...

其实, 在窗口系统没被 Jobs 整合为商用系统前,
世界上所有电脑都是通过 CLI 来操作/使用/控制的...

## summary
> 提要

好的, 通过自己的折腾, 完成任务的同学们, 讲真哪:

- 本质上已经证明自己拥有编程能力了
- 因为, 编程就是这样一种行为模式:
    + 明确问题/目标
    + 分析/分解为一系列阶段任务
    + 每个任务都有明确的达成指标
    + 逐一完成并检验
    + 齐了...
- 这其中最困难的, 就是每个子任务的 `达成指标`:
    + 需要自己独立设定
    + 并设计对应实验来检验
    + 什么是实验?
        * 就是实际检验
        * 输入给定数据
        * 获得期待数据
        * 比如: 这坨代码
            - 给 `1+1` 进去
            - 出来的一定是 `2`
            - 否则, 就是代码有问题


## story
> 场景/背景/情景/...

上节说过笔者在毕业多年后, 通过 Python 才完整的进行了一次软件开发活动,
破除迷妄, 自此有自信自学到需要的所有技术.

那么, 猜? 是什么软件?

- `天气预报网络自动抓取工具` ...
- 因为之前自学过 asp/ActionScript/PHP/.. 等等开发技术
- 但是, 都没有形成一个实用功能的独立构造, 都是在原有系统基础上的功能增补
- 所以, 在发现 Python 是种跨平台的通用脚本语言后:
    + 决定续上大学时一直未了的心愿
    + 独立完成一个软件的开发:
        * 有实用功能
        * 有用户交互
        * 可以运行在各种系统中
        * ...
- 前后用了两周的业余时间;
    + 最终才形成那个不到100行的脚本
    + 但是, 包含预期的所有功能
    + 特别是过程中不得不学习并运用了几十个, 在开始前自己绝对预想不到的知识点:
        * 网络请求
        * 页面解析
        * CLI 交互
        * 排版
        * 用户文档
        * ...
- 再回头和以往各种语言的开发体验一对比:
    + 彻底对 Python 有了认同感
    + 内置的模块太多了, 几乎支持支撑日常绝大多数情景中的开发
    + 社区生态也非常强大, 而且有 Zope 这种怪兽级别的大型应用体系
    + ...
- 一切, 都是从完成一个今天看起来功能微小到可以忽略不计的工具软件而来

所以: 

    学习编程
        就得从编程直接开干



### 增补一点背景要求:

- 课程所有内容是在 macOS 系统环境中完成的
- 并包含一部分 Linux/Android 环境中的内容
- 如果学员本地环境是 Windows 可能没有专门说明
    + 好在 Python 本身是跨平台的
    + 只要有了运行环境, 其它所有调试/自学过程总厂没有差异
    + 即便有不同, 通过日常的搜索也足以自行解决
- 只是, 这一课程特殊在:
    + 对于大家如何自行解决问题的过程异常关注
    + 并要求大家尽可能通过合适的渠道反馈给课程
    + 以便进行针对性分析/辅导
    + 并想证明, 在自学过程中, 失败经验远比成功体验要有用
        * 因为每一次失败都是自身进步的契机, 将获得全新知识点/技能树
        * 而每一次成功,只是已往旧经验有效的简单证明

## problems
> 现实问题,知识阐述

上节任务是:

- 完成基本环境安装:
    + Python 2.7.15
    + zhpy 模块
- 并运行指定代码
- 尝试理解其中涉及的编程常识:
    + 并形成分析/说明
    + 发布在下述仓库 Issue 中

得承认, 开篇任务其实故意埋了很多坑:

- Python 是种软件嘛? 从哪儿下载? 2.7.15版本又从哪下载?
- 如何安装? 如何知道安装好了?
- 什么是模块? zhpy 是什么鬼? 模块怎么安装? 从哪儿安装?
- ...
- `尝试理解...编程常识` 这好象不是行为,只是结果:
    + 如何理解, 怎么尝试?
    + 怎知识什么是常识?
    + 分析/说明应该如何写?
    + Issue 是什么? 怎么发布文字到 Issue 中?
    + ...
- 可以说, 每一个细微的行动都可能迎头撞到无数问题:
    + 这是进入任何一种陌生知识领域应该的状态
    + 但是, 这种状态的体验是极端的, 令人反感的
    + 要是过程中, 没有起过几次白毛汗, 内心,甚至于真的开口骂这坑爹的课程
    + 说明, 你并没有开始尝试完成任务...
    + 那么, 就象私人健身教练服务:
        * 想减少的体脂是在自己身上
        * 教练提供锻炼方案, 给出计划, 行动要求
        * 如果不真的来撸铁/跑步/控制/饮食/...
        * 那么, 无论花多少𫓨去充值
        * 肥膘是一克也不可能自行消失的哪.
- 所以, 先撞起来:
    + 过程中, 有任何具体问题, 都可以去仓库 Issue 中提出问题
    + 有讲师/助教/同学/路人/扫地僧/... 无数好心人来回答帮助
    + 但是, 如果不问, 就憋在心里扎小人, 对课程学习是一丝帮助也冇咯


### Q & A
> 收集并集中回答学员在此反复撞出的问题, 
> 当然, 期待所有具体问题, 都是自行解决并记要下来, 课程简直的复制过来就好 ;-)

- Python 的娘家: [About Python™ | Python.org](https://www.python.org/about/)
- 模块大本营: [PyPI – the Python Package Index · PyPI](https://pypi.org/)
- [py.101.camp ch00-mapping {by gen2htm4io101camp.py v11.10.27 at:181230 18:40:45,710261}](http://io.101.camp/)
- [[ch00]开发任务求助：zhpy安装失败](https://gitlab.com/101camp/py/issues/3)
    + [[ch00]求助：zhpy的interpreter运行错误](https://gitlab.com/101camp/py/issues/7)
- [2d[ch00] 探索过程：孤子分支克隆到本地](https://gitlab.com/101camp/py/issues/6)
    + [[CH00][求助]GitLab SSH Keys - Permission denied (publickey)](https://gitlab.com/101camp/py/issues/9)
    + [「ch00」环境配置求助：ssh公钥生成失败+后续记录](https://gitlab.com/101camp/py/issues/4)
    + [[ch00]小焱对gitlab环境设置的折腾记录](https://gitlab.com/101camp/py/issues/5)
- [1w[BC] 版本仓库中应该放什么文件?](https://gitlab.com/101camp/py/issues/8)
- [[ch00]问题：互联网链接失效的解决方案](https://gitlab.com/101camp/py/issues/10)



## task
> 开发任务

现在开始, 就冲一个实用软件来折腾吧:

- Python 除了操作系统其它各种软件都能开发
- 当然, 课程目标不是引导所有学员变成 小马 那种全能程序猿
- 所以, 得找一个复杂度不高, 功能单一, 解决实际问题, 又有足够丰富的扩展空间
- 即,可玩度, 实用性, 复杂度 均衡的工具
- 这类工具数量也不少, 参考:[我能用 Python 做什么 | 湾区日报](https://wanqu.co/a/6708/%E6%88%91%E8%83%BD%E7%94%A8-python-%E5%81%9A%E4%BB%80%E4%B9%88/)
    + [aosabook/500lines: 500 Lines or Less](https://github.com/aosabook/500lines)
    + [jobbole/ProgrammingProjectList](https://github.com/jobbole/ProgrammingProjectList) ~ 不愁没练手的小项目了
    + ...

权衡再三, 还是来一个不常见的:

    时间帐单记录器

功能:

- 记录每次投入 `py.101.camp` 课程真正用时
- 形成客观数据, 以便进一步:
    + 发现时间黑洞
    + 重获时钟体感
    + 明确详细效能
    + ...
- 参考: [Learn python in Y Minutes](https://learnxinyminutes.com/docs/python/)
- 独立完成以下最小功能集:
    + 可运行
    + 每次输入 `,` 时开始计时
    + 每次输入 `.` 时结束计时
    + 并立即打印本次计录到多长自学/专注/专发时间
- 建议:
    + 工程名: my time logger
    + 缩写: myTL
    + 代码: mytl_v0.py
- 要求: 
    + 开发/测试/运行环境统一为 Python 3.7.0
    + 或基于相同基础版本的其它发行版
    + 以及, 思考一下, 为什么.

![ch01-0-mtl0](gif/ch01-0-mtl0.gif)


### social coding 
> 光说不练徦把式, 这门课配套有代码仓库, 并强烈建议通过真实的编程实践掌握知识点.

- 仓库: https://gitlab.com/101camp/py
    + 各自专有分支中组织任务代码
- 提案: https://gitlab.com/101camp/py/issues
    + 可以提问/讨论/建议/...
- 维基: https://gitlab.com/101camp/py/wikis/home
    + 汇集各种资料/FAQ/知识点资料/...
- 列表: 101camp@googlegroups.com
    + 订阅: 发空白邮件-> 101camp+subscribe@googlegroups.com
    + 退订: 发空白邮件-> 101camp+unsubscribe@googlegroups.com
    + 用邮件和所有同学/助教们讨论一切嗯哼...


## refer
> 参考资料,扩展阅读...

- [Command-line Applications](https://docs.python-guide.org/scenarios/cli/)
- [如何向完全没有任何编程知识的人介绍编程 - ghosTB10G](http://devrel.zoomquiet.top/data/20140121194425/index.html)
    + [一个神奇的故事——为什么程序能够工作](http://blog.shell909090.org/blog/archives/2530/)
    + [极简 Python 上手导念 - Zoom.Quiet Personal Static Wiki](http://wiki.zoomquiet.io/pythonic/MinimalistPyStart)
    + ...
- [刻意练习 ( [美] 安德斯·艾利克森（Anders Ericsson） / 罗伯特·普尔（Robert Pool）)](https://book.douban.com/subject/26895993/)
    + [天才源自刻意练习 ([美] 杰夫·科尔文)](https://book.douban.com/subject/27088714/)
    + [刻意练习：如何成为一个高手 (（美）道格•莱莫夫 / 艾丽卡•伍尔韦 / 凯蒂•叶兹)](https://book.douban.com/subject/27054052/)
    + ...
- [奇特的一生 ([俄] 格拉宁)](https://book.douban.com/subject/1115353/)
    + [把时间当作朋友 - 李笑来](https://read.douban.com/ebook/1283450)
    + [暗时间 (刘未鹏)](https://book.douban.com/subject/6709809/)
    + [拖延心理学 - 〔美〕简·博克, 〔美〕莱诺拉·袁 ](https://read.douban.com/ebook/24304618)
    + ...
- ![Markdown](https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/96px-Markdown-mark.svg.png) [Markdown - Wikipedia](https://en.wikipedia.org/wiki/Markdown)
    + [Markdown Cheatsheet · adam-p/markdown-here Wiki](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
    + [Daring Fireball: Markdown Syntax Documentation](https://daringfireball.net/projects/markdown/syntax)
    + [Markdown Guide](https://www.markdownguide.org/)
    + ...


## logging
> 版本/追踪/修改...


- 180117 初稿
- 180101 init.
