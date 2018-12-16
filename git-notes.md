# Git 笔记

## 两个仓库嵌套

October 的开发工作主要在开发plugin和theme上，根据作者的建议是每个plugin或者theme都需要建立独立的git仓库方便维护。假设October的核心框架我们也在用git管理，那么需要两个仓库嵌套在一起，所以我们可能需要在October的gitignore文件中加入两个文件夹的忽略，这样可以避免把plugin或者theme提交到October仓库中

    plugins
    themes
 