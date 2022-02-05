# TESetup

gaku 様の Tablacus Explorerのインストーラを作ってみました。それだけです。

動作確認あまりしてないので、何かあっても全く責任持ちません。気が向かないと質問は基本無視します。
自己責任で。

## ビルド環境
- windows 10 pro
  - Visual studio 2022 community
## テスト版作成時のビルド方法

- Visual studioの拡張機能管理から、`Microsoft Visual Studio Installer Projects`を入れる。
- gaku様公式の[Tablacus ExplorerのgitHub](https://github.com/tablacus/TablacusExplorer)を、ローカルのどこかにクローンし、
  このブランチの「TESetup1」ディレクトリをコピーして配置。
- (任意）gaku様のTE.slnをVisual studio 2022 communityでビルドできるようにする
- 公式のTE展開しDebug下に`te32.dll、te64.dll、te32.exe、te64.exe`をコピー。または、TE.slnの既存のプロジェクトをビルド。TEのファイルを一通りそろえる。
- `TESetup1\TESetup1.vdproj`)をビルド。(テスト時はgaku様のTE.slnへ追加)
- 「TESetup1」ディレクトリ内の以下生成物がインストーラ。Releaseディレクトリごとコピーしてsetup.exe実行でインストーラ起動する。
	- `TESetup1\Release\setup.exe`
	- `TESetup1\Release\TESetup1.msi`


## インストール後の環境
コントロールパネルのプログラムと機能に登録されるの以外は、以下をするのと同じ
- インストーラで指定したパスにTEを展開
- デスクトップにショートカット作成
  - `Shortcut to TE32.exe`
  - `Shortcut to TE64.exe`
- スタートメニューに追加
  - スタートメニューのTablacusExplorerディレクトリ下。

※インストーラで、「すべてのユーザー」を選択してインストール、TE64.exe起動、コントロールパネルからアンインストール
までしか確認してません。

## 公式様リンク集
このページは恐らく更新しないよ!


- [Tablacus Explorer](https://tablacus.github.io/explorer.html)
- [Tablacus ExplorerのgitHub](https://github.com/tablacus/TablacusExplorer))
- [作者様Twitter](https://twitter.com/tablacus)