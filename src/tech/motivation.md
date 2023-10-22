# mdBookで静的コンテンツを生成してAzureにデプロイするまでの流れを，Github Actionsで自動化する
## はじめに
内容はタイトルの通りです。
静的コンテンツを配信するだけであればGithub Pagesの方がお手軽だと思います。

Azure環境のセットアップに関するワークフローの記述は，[このチュートリアル](https://github.com/skills/deploy-to-azure)の内容を参考にしています。
数あるクラウドサービスのうちAzureを利用するのはそのためです。
チュートリアルからコピペした部分もあるので，そこには適切なライセンスを当てています。

今回行うことはAzureの無料枠で収まるはずですが，紹介する手順を真似た結果課金が発生したとしても，私は一切の責任を負いません。
その点はご了承ください。
ただ，Azure環境のリソースを削除するワークフローも紹介するので，デプロイしてちょっとサイトを覗いた後そのワークフローを実行する分にはとんでもないことにならないはずです。

最終的なファイル群はこちらにあります。
[github:yaaamaada/myblog](https://github.com/yaaamaada/myblog)

## 手順
### 開発環境でmdBookプロジェクトを立ち上げる


### ワークフローを記述する


### ワークフローを実行する


## おわりに
mdBookで静的コンテンツを生成してAzureにデプロイするまでの流れを，Github Actionsで自動化しました。
GithubもAzureも覚える操作が多くて大変ですね。

## 参考資料
* [skills/deploy-to-azure: Create two deployment workflows using GitHub Actions and Microsoft Azure.](https://github.com/skills/deploy-to-azure)
* [mdbookをGitHub PagesにActionsから自動デプロイする - BioErrorLog Tech Blog](https://www.bioerrorlog.work/entry/mdbook-github-pages-cd)
* [peaceiris/actions-mdbook: GitHub Actions for mdBook (rust-lang/mdBook) ⚡️ Setup mdBook quickly and build your site fast. Linux (Ubuntu), macOS, and Windows are supported.](https://github.com/peaceiris/actions-mdbook)
* [Automated Deployment: GitHub Actions · rust-lang/mdBook Wiki](https://github.com/rust-lang/mdBook/wiki/Automated-Deployment%3A-GitHub-Actions)
<!-- * [mdBook Documentation](https://rust-lang.github.io/mdBook/index.html) -->
