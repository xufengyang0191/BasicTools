# Git 学习过程

为什么使用 Git？

Git 是一款分布式的代码版本控制工具，Linux 之父 Linus 嫌弃当时主流的中心式的版本控制工具太难用还要花钱，就自己开发出了 Git 用来维护 Linux 的版本。

Git 的设计非常优雅，但初学者通常因为很难理解其内部逻辑因此会觉得非常难用。对 Git 不熟悉的初学者很容易出现因为误用命令将代码给控制版本控制没了的状况。

但相信我，和 Vim 一样，Git 是一款你最终掌握之后会感叹“它值得！”的神器。

最好先学习 vim。以下教程并不代表学习顺序，按需选择即可，快速入门和基础教程中搭配一个使用即可，这时你已经掌握了 git 大部分的用法，后面的部分可以作为有意思的扩展了解作为提升。

学习 git 的踩坑过程，后面有较为详细的介绍：
- [git 新手够用指南](https://www.bilibili.com/video/BV1e541137Tc/?spm_id_from=333.337.search-card.all.click)（快速入门）
- [狂神 git 教程](https://www.bilibili.com/video/BV1FE411P7B3/?spm_id_from=333.337.search-card.all.click)（快速入门）
- [计算机缺失一课——git](https://missing-semester-cn.github.io/2020/version-control/)（基础教程）
- [廖雪峰的 git 教程](https://www.liaoxuefeng.com/wiki/896043488029600)（基础教程）
- [尚硅谷 git 教程](https://www.bilibili.com/video/BV1vy4y1s7k6)（基础教程）
- [Pro git](https://git-scm.com/book/en/v2)（基础教程）
- [Pro git 中文版](https://git-scm.com/book/zh/v2))（基础教程）
- [A game of learning git](https://learngitbranching.js.org/?locale=zh_CN)（巩固基础）
- [蛋老师的 git 教程](https://www.bilibili.com/video/BV1r3411F7kn/?spm_id_from=333.999.0.0)（巩固基础）
- [上交 IPADS 新人培训——git](https://www.bilibili.com/video/BV1YR4y1E7LX/?spm_id_from=333.999.0.0)（巩固基础）
- [How to write a commit](https://cbea.ms/git-commit/)（基础标准）
- [开源工作者的基本流程](https://www.bilibili.com/video/BV19e4y1q7JJ/?spm_id_from=333.999.0.0)（进阶使用）
- [git 的撤销操作](https://www.bilibili.com/video/BV1ne4y1S7S9/?spm_id_from=333.999.0.0)（进阶使用）
- [五个隐藏的 GitHub 操作](https://www.bilibili.com/video/BV1q54y1f7h6/?spm_id_from=333.337.search-card.all.click)（进阶使用） 
- [git-cheat-sheet](./git-cheat-sheet.pdf)（速查标准）

**说在前面，这里代表一些学习者和本人的部分看法，每个人学习都有不同的体验，上述部分教程没有涉猎到，但是听说评价不错就放在这儿了。**

在 [git 新手够用指南](https://www.bilibili.com/video/BV1e541137Tc/?spm_id_from=333.337.search-card.all.click) 中：比较基础，适合快速入门 git，仅仅涉及了开发流程，没有过多工作原理的介绍，当然这个视频已经可以应付个人日常大部分使用情况，但是涉及协同开发和开源管理等需要多看看后面教程。

在 [计算机缺失一课——git](https://missing-semester-cn.github.io/2020/version-control/) 中：我将这个教程被封为经典，主要是并没有像其他教程一样，仅仅由上而下讲解使用过程。当然，后者在日常使用的过程中当然已经足够，但是当出现错误时很容易手足无措，git 的底层设计和思想本身是非常优雅的，值得学习！教程由底向上讲解 git 的原理和使用，本教程配合 [上交 IPADS 新人培训——git](https://www.bilibili.com/video/BV1YR4y1E7LX/?spm_id_from=333.999.0.0) 食用更佳。

在 [廖雪峰的 git 教程](https://www.liaoxuefeng.com/wiki/896043488029600) 中：这时作者第一个学习所使用的的教程，当时没有发现那么多资源，找到一个评价还不错的就直接使用了，讲解比较详细，大致过一遍能对 git 的业务流程有一个很好的理解，但是里面涉及的应用场景较少，作为打基础搭配其他视频食用更佳。

在 [A game of learning git](https://learngitbranching.js.org/?locale=zh_CN) 中：一个可视化的 git 小游戏，模拟了命令行操作，任务提示清晰，场景丰富，过一遍很好的加深对 git 的使用理解。

在 [蛋老师的 git 教程](https://www.bilibili.com/video/BV1r3411F7kn/?spm_id_from=333.999.0.0) 中：适合看过基础教程对 git 的整体结构有一定的认识之后的同学，对开发涉及的流程进行了一个总结，相信我，看完会对 git 有个更加系统的认识。

在 [上交 IPADS 新人培训——git](https://www.bilibili.com/video/BV1YR4y1E7LX/?spm_id_from=333.999.0.0) 中：该教程中自底向上从 git commit 的数据结构开始剖析 git 的工作流程，适合使用过一段时间 git 的同学使用（前半部分对着 [计算机缺失一课——git](https://missing-semester-cn.github.io/2020/version-control/) 做的），当然视频作者也提到了使用 git 进行项目 debug 的几个应用情景。

在 [How to write a commit](https://cbea.ms/git-commit/) 中，提醒 git 使用者在 git commit 过程中有七个需要注意的规则：
1. 用空行将主题与正文分开
2. 将主题行限制为 50 个字符
3. 将主题行第一个单词的首字母大写
4. 不要以句号结束主题行
5. 主题行语法使用祈使句
6. 正文最好每 72 个字符换行
7. 正文解释：what，why 和 how

在 [开源工作者的基本流程](https://www.bilibili.com/video/BV19e4y1q7JJ/?spm_id_from=333.999.0.0) 中：**项目协同**必看，视频作者以一个微软大厂工作人员身份，讲解如何参与一个开源项目，也是如何多人协同一个项目，保证项目管理不翻车。

在 [git 撤销操作](https://www.bilibili.com/video/BV1ne4y1S7S9/?spm_id_from=333.999.0.0) 中：视频中涉及到 git 使用过程中，如何从不同的操作层级（工作区、暂存区、本地仓库、远程仓库）撤销所提交的操作。

在 [五个隐藏的 GitHub 操作](https://www.bilibili.com/video/BV1q54y1f7h6/?spm_id_from=333.337.search-card.all.click) 中提到的五个技巧：
1. 官方文档中的高级搜索功能，更为准确地搜索
2. 项目主页搜索（`t`）代码行跳转（`l`）更改记录（`b`），官方文档中的快捷键面板（`ctrl+k`）
3. 按下 `。` 可以直接再网页版 vscode 查看代码
4. 在项目主页的网址上加上前缀 `gitpod.io/#/`  在线运行
5. 定期推送新动态