Android 镜像使用帮助
====================

参考 Google 教程 <https://source.android.com/source/downloading.html>，
将 `https://android.googlesource.com/` 全部使用 `git://aosp.tuna.tsinghua.edu.cn/android/` 代替即可。

**本站资源有限，每个 IP 限制并发数为 4，请勿使用 `repo sync -j8`
这样的方式同步。**

替换已有的 AOSP 源代码的 remote
----------------------------

如果你之前已经通过某种途径获得了 AOSP 的源码，但是你希望以后通过 TUNA 同步，只需要将
`.repo/manifests.git/config` 中的


       url = https://android.googlesource.com/platform/manifest


改为下面的 code 即可：


       url = git://aosp.tuna.tsinghua.edu.cn/android/platform/manifest


**这个方法也可以用来在同步 Cyanogenmod 代码的时候从 TUNA 同步部分代码**

FAQ
---

1. 镜像的是什么？

   - 是按照 google 指南建立的镜像 git 仓库。

2. 为何不能通过浏览器访问？

   - 暂时没有 gitweb, 而且反正是 git bare 仓库，没有可以直接看到的内容。

3. 出现 `curl: (22) The requested URL returned error: 404 Not Found
Server does not provide clone.bundle; ignoring.` 怎么办？

   - 无视即可。
