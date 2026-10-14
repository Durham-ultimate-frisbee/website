# Durham University Ultimate Frisbee Club 网站

[English](README.md) | **中文**

网址：**https://durham-ultimate-frisbee.github.io/website/**

杜伦大学极限飞盘俱乐部（DUF）的官方网站，由俱乐部成员维护。

## 这是什么

- **页面**：首页（含训练时间）、关于、成员、荣誉、新闻、联系方式。
- **网站上的所有内容都在 [`content/`](../content/) 文件夹里**，都是简单的文本文件，不需要碰代码。
- **改错了也没关系**：内容填错时网站不会更新，并且会用英文告诉你具体要改哪里。线上网站会一直保持上一个正确的版本。
- **免费、保护隐私**：网站是托管在 GitHub Pages 上的普通网页，没有服务器、登录、追踪，也不用 Cookie。照片里隐藏的位置信息会被自动清除。

## 谁在维护

| 角色 | 谁 | 负责什么 |
|---|---|---|
| **网站维护者** | 有这个仓库权限的俱乐部成员 | 内容：成员、荣誉、新闻、训练时间、照片 |
| **技术负责人** | Tao（[@alvinz26](https://github.com/alvinz26)），网站的作者 | 代码和设计。`content/` 以外的任何修改都需要他批准 |

**新来的维护者**：请俱乐部管理员把你加到这个仓库，角色选 **Write**。
你卸任时，也用同样的方法把接任的人加进来。

## 怎么改内容

| 文件 | 管什么 |
|---|---|
| [`content/site.yaml`](../content/site.yaml) | 队名、颜色、logo、社交链接、顶部横幅、荣誉筛选项 |
| [`content/people.yaml`](../content/people.yaml) | exec、队长、教练，每人每个赛季写一条 |
| [`content/honours.yaml`](../content/honours.yaml) | 成绩：赛季、赛事、队伍、名次，有的话加上参赛名单 |
| [`content/news/`](../content/news/) | 新闻，每篇一个文件 |
| [`content/pages/join.md`](../content/pages/join.md) | 首页的 "New to ultimate?" 板块，包括训练时间表 |
| [`content/pages/about.md`](../content/pages/about.md) | 关于页 |
| [`content/images/`](../content/images/) | logo、照片、新闻封面 |

**怎么修改**（直接在 GitHub 网页上改，不用安装任何东西）：

1. 打开要改的文件，点 ✏️ **Edit**。
2. 改好后点 **Commit changes…** → 保持选中 **Create a new branch and start a pull request** → 点 **Propose changes** → 点 **Create pull request**。
3. 等自动检查变成**绿色 ✓**（几分钟），点 **Squash and merge**。

只改 `content/` 里的内容不需要任何人批准。每个字段的含义见 [docs/data-model.md](../docs/data-model.md)，中文的分步说明见 [docs/content-guide.md](../docs/content-guide.md)。

## 每个新赛季要做的

- [ ] **Exec**：在 `content/people.yaml` 里加上新一届 exec，赛季写新的（例如 `2027/28`）。去年的不要删，成员页只会显示最新赛季。
- [ ] **训练**：更新 `content/pages/join.md` 里的训练时间表。
- [ ] **荣誉**：每次比赛后在 `content/honours.yaml` 里加上成绩。有参赛名单的话一起写上，排行榜要用到。
- [ ] **新闻**：在 `content/news/` 里发选拔、体验课、比赛结果、社交活动的消息。
- [ ] **横幅**：更新或删掉 `content/site.yaml` 里的 `notice:`。

## 照片

- 只用**照片里每个人都同意放到网上**、并且**摄影师也同意使用**的照片。
- 上传到 `content/images/` 里对应的文件夹（比如 `content/images/people/`），再在文件里写上路径，比如 `photo: images/people/alex-smith.jpg`。
- 用 JPG，宽度 2000 像素左右就够了。发布时会自动清除照片里的位置和相机信息。

## 改完多久生效

合并后通常**几分钟**就会生效。仓库顶部的 **Actions** 页可以看进度：黄色表示正在发布，绿色 ✓ 表示已经上线（刷新一下网页），红色 ✗ 表示有地方要改。

## 出错了怎么办

- 红色 ✗ 表示内容检查发现了问题，**线上网站不受影响**。
- 点红色 ✗ → **Details**，找到以 `Content check failed` 开头的那一段，里面写明了是哪个文件、哪一条、哪个字段、要怎么改：

  ```
  content/people.yaml → 2027/28 · Alex Smith (line 12)
    • role — is required but missing.
  ```

- 改好后再保存一次就行。每一个历史版本都会被保存，什么都不会丢。
- 解决不了、或者想加新功能：在这个仓库里开一个 issue，并 @alvinz26。

## 致谢

网站由 **Tao**（[@alvinz26](https://github.com/alvinz26)）设计和开发，基于他的开源项目 [team-site-template](https://github.com/alvinz26/team-site-template)（[MIT 许可证](../LICENSE)）。请保留页脚的 "Website by Tao" 署名。
