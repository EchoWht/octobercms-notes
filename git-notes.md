# Git 笔记

## 两个仓库嵌套

October 的开发工作主要在开发plugin和theme上，根据作者的建议是每个plugin或者theme都需要建立独立的git仓库方便维护。假设October的核心框架我们也在用git管理，那么需要两个仓库嵌套在一起，所以我们可能需要在October的gitignore文件中加入两个文件夹的忽略，这样可以避免把plugin或者theme提交到October仓库中

    plugins
    themes

## fork后保持和原始仓库同步更新

当我们fork作者的原始仓库时，原始仓库有代码更新时我们的仓库是不会同步更新的，如果需要将原始仓库的代码同步到自己的仓库中，需要进行下面的操作

1. git remote add octobercms https://github.com/octobercms/october.git
2. git fetch octobercms
3. git merge octobercms/master 或者 git merge octobercms/develop
4. git push -u origin master 
5. php artisan october:up 
