#把本地项目放到GitHub中


* 1.在 Github 上创建一个库.
* 2.本地的 Git 开始初始化.
>https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/0013743256916071d599b3aed534aaab22a0db6c4e07fd0000

* 3.为本地项目添加远程库
>https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/0013752340242354807e192f02a44359908df8a5643103a000

* 4.遇到 rejected 错误的解决
>https://github.com/waylau/github-help/blob/master/Dealing%20with%20non-fast-forward%20errors%20%E5%A4%84%E7%90%86%20non-fast-forward%20%E9%94%99%E8%AF%AF.md

```
$ git fetch origin
# Fetches updates made to an online repository
$ git merge origin branch
# Merges updates made online with your local work
$ git pull origin branch
```

* 5.问题 ```refusing to merge unrelated histories``` 的解决
>http://blog.csdn.net/lindexi_gd/article/details/52554159

```
git pull origin master ----allow-unrelated-histories
```

* 6.删除远程仓库
>https://git-scm.com/book/zh/v1/Git-%E5%9F%BA%E7%A1%80-%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93%E7%9A%84%E4%BD%BF%E7%94%A8

```
tiandeMacBook-Pro-2:Android-nRF-Toolbox tianzeng$ git remote -v
myorigin        git@github.com:ghzjtian/Android-nRF-Toolbox.git (fetch)
myorigin        git@github.com:ghzjtian/Android-nRF-Toolbox.git (push)
origin  git@github.com:NordicSemiconductor/Android-nRF-Toolbox.git (fetch)
origin  git@github.com:NordicSemiconductor/Android-nRF-Toolbox.git (push)
tiandeMacBook-Pro-2:Android-nRF-Toolbox tianzeng$ git remote add origin https://gitee.com/gitzjtian/GLB_BLE.git
fatal: remote origin already exists.
tiandeMacBook-Pro-2:Android-nRF-Toolbox tianzeng$ git remote rm origin
tiandeMacBook-Pro-2:Android-nRF-Toolbox tianzeng$ git remote -v
myorigin        git@github.com:ghzjtian/Android-nRF-Toolbox.git (fetch)
myorigin        git@github.com:ghzjtian/Android-nRF-Toolbox.git (push)
tiandeMacBook-Pro-2:Android-nRF-Toolbox tianzeng$ 

```