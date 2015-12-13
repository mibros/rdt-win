Ruby developers tool kit for windows
================

WindowsでRubyの開発環境を手早く整えるツールです。

Install
--------

1. 以下のURLからzipファイル一式をダウンロードして解凍します。

  https://github.com/mibros/rdt-win/archive/master.zip

2. コマンドプロンプトを起動し、解凍したフォルダに移動します。

  c:\に解凍した場合

  ``` batch
    c:\> cd rdt-win-master
  ```

3. Chocolateyのインストールバッチを実行します。

  ``` batch
      c:\rdt-win-master> installChocolatey.cmd
  ```
  インストールが始まるので終わるまで待ちます。

4. 次にChocolatey経由でRubyプログラミングに必要なソフトをインストールします。

  3で使用したコマンドプロンプトを閉じて新しくコマンドプロンプトを立ち上げます。
  コマンドプロンプトからChocolateyのコマンドを使用できるようになります。
  再びrdt-win-masterディレクトリまで移動します。

  ``` batch
    c:\> cd rdt-win-master
  ```
5. インストールバッチを起動します。

  ``` batch
    c:\rdt-win-master> choco-install-ruby.cmd
  ```

  これまた勝手にインストールが始まるので、終わるまで待ちます。<br>
  今のところRuby、devkit、Atom、Gitがインストール対象です。<br>
  インストールされるソフトは、choco-install-ruby.cmd内に記述されています。

6. 最後にテキストエディタAtomにもプラグインをインストールします。

  5で使用したコマンドプロンプトを閉じて新しくコマンドプロンプトを立ち上げます。<br>
  コマンドプロンプトからAtomとAtomのパッケージ管理コマンドが使用できるようになります。<br>
  4の手順と同様に、rdt-win-masterディレクトリまで移動します。

7. Atomパッケージのインストールバッチを起動します。  

  ``` batch
    c:\rdt-win-master> atom-install-packages.cmd
  ```

  これまた勝手にインストールが始まるので、終わるまで待ちます。

8. セットアップが完了したかどうかAtomを使ってテスト用のRubyコードを書きます。

  ``` batch
    c:\rdt-win-master> atom
  ```
  Atomが起動します。<br>
  WindowsのスタートメニューにGitHub,incというのが追加されているはずなので、<br>
  普通にそちらから起動しても大丈夫です。

9. Rubyコードを書き、Alt+Rを押します。

  ``` ruby
    puts 'hello world'
  ```
  エディタ右側に、Rubyプログラムの実行結果が表示されれば、無事セットアップ完了です。

License
--------

  MIT

ReleaseNotes
--------

### 0.2.0 - 13 Dec 2015
- railsパッケージ追加

### 0.1.1 - 4 Dec 2015
- インストール方法説明追加

### 0.1.0 - 3 Dec 2015
- ミニマムセット公開
