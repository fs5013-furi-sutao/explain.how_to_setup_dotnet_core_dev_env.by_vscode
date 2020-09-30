# VSCode で .NET Core の開発環境構築
VSCode で .NET Core の開発環境を構築する方法について説明する。

## .NET Core とは
「.NET Core」は、Microsoft 社が開発しているオープンソースのソフトウェアフレームワーク。

.NET Framework と違い、MacやLinuxなどクロスプラットフォームで動作する。
「.NET Core 3.0」以降では、コンソールアプリや Web 、モバイルに加えて、Windows Forms や WPF アプリもサポートされている。

## .NET Core SDK のインストール
.NET Core の開発には .NET Core SDK が必要になる。

.NET Core SDK は、Scoop の main バケットにもある。.NET Core SDK をインストールする。
```cosole
scoop install dotnet-sdk
```

## VSCode のインストール
VSCode をまだ導入していない場合は、以下を参照してインストールを済ませる。

VSCode のポータブル版を導入する方法:  
https://github.com/fs5013-furi-sutao/explain.how_to_install_vscode_portable.with_scoop

## C# 拡張機能のインストール
VSCodeを起動。ショートカット[Ctrl + Shift + X] で拡張機能を表示。

検索ワード「C#」を入力。検索結果一覧から[C# for Visual Studio Code]を選択し、[install] をクリックする。

## 【動作確認】プロジェクトの作成～デバッグ
Git Bash を起動。
C#のプロジェクトを格納するフォルダ（例：C:/github/sample/csharp/Test）を作成します。
```console
mkdir ./first.net.core
```

cdコマンドで作成したフォルダ内に移動。
```console
cd ./first.net.core
```

プロジェクトを作成する。
```console
dotnet new console
```

Program.cs などのファイルが自動生成される。

VSCode でプロジェクトフォルダ（例：first.net.core）を開き、「Ctrl + Shift + D」にてデバッグを表示。

以下のようなメッセージが出現したら、「Yes」を選択。
Required assets to build and debug are missing from 'first.net.core'. Add them?

メニューの [Run] - [Add Configuration...] を選択。デバッグ可能な種類の一覧から[.NET Core]を選択。

デバッグの再生ボタンをクリック。

Visual Studio Codのターミナルに「Hello World!」と表示されたらデバッグ成功。
