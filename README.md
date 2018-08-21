# DiscordのAPIを用いてBOTを作る
※私的備忘録

## **必要なもの**
  - python (今回は3.6.5を使用。)
    - discord.py
    - PyNaCl
    - youtube-dl
  - Discord BOTユーザー及びそのトークン 

  - ※PyNaClとyoutube-dlは作成するBOTによっては使用しませんので任意で導入して下さい。

## **1. pythonの導入**
   1. [公式サイト](https://www.python.org/downloads)からWindows版Pythonインストーラをダウンロードする。
   
   2. ダウンロードしたインストーラを実行し、作業を完了させる。(環境変数にpythonのパスを書き込むか聞かれた場合は、承諾することで手動でのパス設定を省ける。)

## **2. discord.pyの導入**
   1. コマンドプロンプトを管理者権限で開き、以下のコマンドを実行する。

   ```terminal
   python -m pip -V
   ```

   実行結果

   ```terminal
   pip 10.0.1 from C:\Program Files\Python36\lib\site-packages\pip (python 3.6)
   ```

   ※使用中のpipバージョンよりも最新のバージョンにアップデート可能な場合は
   
   ```terminal
   python -m pip install --upgrade pip
   ```
   を実行することで更新可能。

   2. 続いて、
   
   ```terminal
   pip install discord pynacl youtube-dl
   ```
  
   を実行しパッケージをインストールする。

   3. 正常にインストール出来たかを確認するには

   ```terminal
   python -m pip freeze
   ```
   
   で導入パッケージの一覧が表示される。

## **3. Discord アプリケーションとBOTユーザーの作成**
   1. [アプリケーション作成画面](https://discordapp.com/developers/applications/me)から「新しいアプリ」をクリックし
   アプリケーション名と概要を入力。任意でBOTアイコンやOAuthのリダイレクトを指定する。
   
   2. 保存するとアプリケーションが作成され、クライアントIDや秘密鍵が発行される。

   3. ページ下部にスクロールしBOT欄から「BOTを作成」のボタンをクリックするとユーザー名とトークンが発行される。
   - ※ここで発行されたトークンは後に使うので、メモに控えておく。

   4. ページ上部にスクロールし「Generate OAuth2 URL」からSCOPES欄にあるURLをコピー。コピーしたURLにアクセスしプルダウンから自分のサーバーを選び認証する。

## **4. BOTプログラム**
   参考:[Pythonで簡単なDiscord Botの作り方 - Qiita](https://qiita.com/PinappleHunter/items/af4ccdbb04727437477f#botを書く) 

## **5. 実際に使ってみる**
   4.で作成した.pyのディレクトリをコマンドプロンプトで開き、BOTを起動させる。

   ```terminal
   python filename.py
   ```
   以上。
