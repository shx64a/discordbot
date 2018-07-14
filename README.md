# Discord BOTAPIを用いてBotを作る
※備忘録

## **必要なもの**
   - python (今回は3.6.5を使用)
   - Discord BOTユーザー及びそのトークン 

## **1. pythonの導入**
   1. 公式サイト(https://www.python.org/downloads)からWindows版Pythonインストーラをダウンロードする。
   
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

   ※```python -m pip install --upgrade pip``` が表示される場合は実行しておく。

   2. 続いて、
   
   ```terminal
   python -m pip install discord
   ```
  
   を実行する。

   実行結果
   
   ```terminal
    Successfully installed aiohttp-1.0.5 async-timeout-3.0.0 chardet-3.0.4 discord-0.0.2 discord.py-0.16.12 multidict-4.3.1 websockets-3.4
   ```

   3. パッケージが正常にインストール出来たか確認するには

   ```terminal
   python -m pip freeze
   ```
   
   で導入パッケージの一覧が表示される。

## **3. Discord アプリケーションとBOTユーザーの作成**
   1. [アプリケーション作成画面](https://discordapp.com/developers/applications/me)から「新しいアプリ」をクリックし
   アプリケーション名と概要を入力。任意でBOTアイコンやOAuthのリダイレクトを指定する。
   
   2. 保存するとアプリケーションが作成され、クライアントIDや秘密鍵が発行される。

   3. ページ下部にスクロールしBOT欄から「BOTを作成」のボタンをクリックするとユーザー名とトークンが発行される。
   ※ここで発行されたトークンは後に使うので、メモに控えておく。

   4. ページ上部にスクロールし「Generate OAuth2 URL」からSCOPES欄にあるURLをコピー。コピーしたURLにアクセスしプルダウンから自分のサーバーを選び認証する。

## **4. BOTプログラム**
   [~~Qiitaの記事に丸投げ~~](https://qiita.com/PinappleHunter/items/af4ccdbb04727437477f#botを書く)   

## **5. 実際に使ってみる**

   以上。
