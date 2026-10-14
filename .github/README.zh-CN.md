# Durham University Ultimate Frisbee Club 网站

[English](README.md) | **中文**

网址：**https://durham-ultimate-frisbee.github.io/website/**

## 这是什么

杜伦大学极限飞盘俱乐部（DUF）的网站，包括首页（含训练时间）、关于、成员、荣誉、新闻和联系方式。

这是一个用 [Astro](https://astro.build) 构建的静态网站，免费发布在 GitHub Pages 上，没有服务器、登录、追踪，也不用 Cookie。网站上的所有内容都放在 [`content/`](../content/) 文件夹里，都是简单的文本文件，更新内容完全不用碰代码。如果填错了，网站不会更新，并且会用英文提示该改什么；线上网站会一直保持上一个正确的版本。

由 **Tao**（[@alvinz26](https://github.com/alvinz26)）设计和开发。

## 要更新哪些内容

| 文件 | 管什么 |
|---|---|
| [`content/people.yaml`](../content/people.yaml) | exec、队长、教练，每人每个赛季写一条（网站只显示最新赛季） |
| [`content/pages/join.md`](../content/pages/join.md) | 首页的 "New to ultimate?" 板块，包括训练时间表 |
| [`content/honours.yaml`](../content/honours.yaml) | 成绩：赛季、赛事、队伍、名次，有的话加上参赛名单 |
| [`content/news/`](../content/news/) | 新闻，每篇一个文件 |
| [`content/pages/about.md`](../content/pages/about.md) | 关于页 |
| [`content/site.yaml`](../content/site.yaml) | 队名、颜色、logo、社交链接、顶部横幅 |
| [`content/images/`](../content/images/) | logo、照片、新闻封面 |

**怎么修改**（在 GitHub 网页上操作）：

1. 打开要改的文件，点 ✏️ **Edit**。
2. 点 **Commit changes…** → 保持选中 **Create a new branch and start a pull request** → **Propose changes** → **Create pull request**。
3. 等自动检查出现**绿色 ✓**（几分钟），点 **Squash and merge**。再过几分钟网站就会更新。

每个字段的含义见 [docs/data-model.md](../docs/data-model.md)，中文的分步说明见 [docs/content-guide.md](../docs/content-guide.md)。

## 照片

- 只用**照片里每个人都同意放到网上**、并且**摄影师也同意使用**的照片。
- 上传到 `content/images/` 里对应的文件夹，再在文件里写上路径，比如 `photo: images/people/alex-smith.jpg`。
- 用 JPG，宽度 2000 像素左右就够了。网站发布时会自动清除照片里的位置和相机信息。

## 出错了怎么办

- 红色 ✗ 表示内容检查发现了问题，线上网站不受影响。
- 点红色 ✗ → **Details**，找到以 `Content check failed` 开头的那一段，里面写明了哪个文件、哪一条、哪个字段、要怎么改：

  ```
  content/people.yaml → 2027/28 · Alex Smith (line 12)
    • role — is required but missing.
  ```

- 改好后再保存一次就行。每个历史版本都会保留，什么都不会丢。
- 还是解决不了，就在这个仓库里开一个 issue。

---

基于 [team-site-template](https://github.com/alvinz26/team-site-template) · [MIT 许可证](../LICENSE)
