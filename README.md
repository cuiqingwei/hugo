<img align="right" width="150" alt="logo" src="https://user-images.githubusercontent.com/5889006/190859553-5b229b4f-c476-4cbd-928f-890f5265ca4c.png">

# Hugo Theme Stack 快速启动模板

这是 [Hugo theme Stack](https://github.com/CaiJimmy/hugo-theme-stack) 的快速启动模板。它使用 [Hugo modules](https://gohugo.io/hugo-modules/) 功能来加载主题。

它包含基本的主题结构和配置。GitHub action 已被设置为自动将主题部署到公共 GitHub 页面。此外，还有一个定时任务每天自动更新主题。

## 视频教程

如果您在设置过程中感到困惑，这里有一个视频教程，展示如何使用此模板建立新的 Hugo 网站，并将其部署到 GitHub Pages：https://www.youtube.com/watch?v=8qDdQQ6Ifxo

## 开始使用

1. 点击*使用此模板*，并在 GitHub 上创建您的存储库为 `<username>.github.io`。（您也可以使用不同的存储库名称，但随后生成的网站将在 `https://<username>.github.io/<repository-name>` 可用。）
![第1步](https://user-images.githubusercontent.com/5889006/156916624-20b2a784-f3a9-4718-aa5f-ce2a436b241f.png)

2. 创建存储库后，创建与其关联的 GitHub codespace。
![创建 codespace](https://user-images.githubusercontent.com/5889006/156916672-43b7b6e9-4ffb-4704-b4ba-d5ca40ffcae7.png)

3. 在等待 codespace 创建期间，转到新创建存储库的 `Settings` -> `Pages`，并将 `Build and deployment` -> `Source` 设置为 `GitHub Actions`。
![更改构建和部署源](https://github.com/user-attachments/assets/192459bf-25d8-441e-8029-c108d789e449)

4. 创建 codespace 后，您可以通过在终端中运行 `hugo server` 来测试网站是否成功构建，并查看您的新网站的实际效果。

5. 检查 `config` 文件夹中的配置文件。您可以编辑它们以满足您的需求。确保更新 `config/_default/config.toml` 中的 `baseurl` 属性为您网站的 URL。例如，如果您的新存储库名为 `my-blog`，则 `baseurl` 应为 `https://<username>.github.io/my-blog/`。

6. 完成网站编辑后，只需提交并推送即可。GitHub action 将自动将网站部署到与存储库关联的 GitHub page。

---

如果您不想使用 GitHub codespace，也可以在本地机器上运行此模板。**您需要在本地安装 Git、Go 和 Hugo extended。** 有关更多信息，请查看官方 Hugo 文档：https://gohugo.io/installation/

## 手动更新主题

运行：

```bash
hugo mod get -u github.com/CaiJimmy/hugo-theme-stack/v4
hugo mod tidy
```

> 此启动模板已配置为主题的 `v4` 版本。由于 Go 模块的限制，一旦 `v4` 或更高版本的主题发布，您需要手动更新主题。（修改 `config/module.toml` 文件）

## 部署到其他静态页面托管服务

查看官方 Hugo 文档：https://gohugo.io/host-and-deploy/
