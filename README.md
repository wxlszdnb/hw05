# 高性能并行编程与优化 - 第0x讲的回家作业

通过 pull request 提交作业。会批分数，但是：

没有结业证书，回家作业仅仅作为评估学习效果和巩固知识的手段，不必为分数感到紧张 :)
量力而行，只要能在本课中，学到昨天的自己不懂的知识，就是胜利，没必要和别人攀比。
注意不要偷看别人的作业哦！

- 课件：https://github.com/parallel101/course
- 录播：https://space.bilibili.com/263032155

作业提交时间不限 :) 即使完结了还想交的话我也会看的~ 不过最好在下一讲开播前完成。

- 如何开 pull request：https://zhuanlan.zhihu.com/p/51199833
- 如何设置 https 代理：https://www.jianshu.com/p/b481d2a42274

## 评分规则

- 完成作业基本要求 50 分（详见下方"作业要求"）
- 能够在 PR 描述中用自己的话解释 25 分
- 代码格式规范、能够跨平台 5 分
- 有自己独特的创新点 20 分
- 明显抄袭现象 -100 分

## 作业要求

修改 main.cpp，修复并改进其中的 HTTP 服务器：

- 把 `login`, `register` 等函数变成多线程安全的 - 10 分
- 把 `login` 的登录计时器改成基于 chrono 的 - 5 分
- 能利用 `shared_mutex` 区分读和写 - 10 分
- 用 `lock_guard` 系列符合 RAII 思想 - 5 分
- 让 ThreadPool::create 创建的线程保持后台运行不要退出 - 15 分
- 等待 tpool 中所有线程都结束后再退出 - 5 分

并通过 `main()` 函数中的基本测试。

## 关于内卷

如果你把 map 改成了自己实现的基于 hash 的，甚至是用了 CAS 的。
只要是在 **满足作业要求且不出错** 的基础上，这是件好事！
老师会酌情加分，视为“独特的创新点”，但最多不超过 20 分。
