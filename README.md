# ChickenBot  
### Slack上で稼働するチキンなBot    
### 機能一覧    
##### 1.挨拶機能    
挨拶に対して返答してくれる機能    
##### 2.アラーム機能    
当日の日の出の時間毎に自動的にアラームを鳴動する機能    
##### 3.おすすめ映画提案機能    
「!おすすめ映画」と投下するとメンションメッセージでは2019年の映画、ダイレクトメッセージではマイナーな映画のURLと一言コメントとTSUTAYAやGEOのURLを返す機能    
##### 4.割り当て機能     
指定された文字を自動的にランダムで割り当てる機能    
(ex.)  
「!割り当てメーカー」(改行)    
あ.い.う.え.お(改行)    
1.2.3.4.5 (と送信すると)    
い - 2    
う - 3    
あ - 4    
お - 1    
え - 5 (の様にシャッフルして返してくれる)    
##### 5.占い機能    
今日の運勢を占ってくれる機能    
「おみくじ」を入力すると今日の運勢とメッセージを送ってくれる    
##### 6.料理レシピ提案機能    
「!献立」と投下すると ランダムで卵料理のレシピのURLとメッセージを投下    
「!他のレシピ」と投下すると ランダムで卵料理以外のレシピのURLとメッセージを投下    
### Eclipseへのインポートと実行    
Eclipseへのimport    
1.Select File>Import>Git - Projects from Git    
2.Clone URI    
3.set clone URI to https://github.com/CraneIjtmw/ChickenBot.git　←コピーしてEclipseで貼り付け
4.適宜[NEXT]を押していく    
5."Import as general project"をチェックして、"finish" を押す    
credentialsをセットする    
  
1.プロジェクト上で、右クリック  
2.Configure>Convert to Maven project  
3.(これでmaven projectとしてEclipseに読み込まれます)  
4.https://my.slack.com/services/new/bot からBOT用のAPI Tokenを取得します  
5.BOTのusernameを決めたら、[Add bot integration]をクリックします  
6.EclipseにAPI Token for BOT をセットします    
7.src/main/java直下にcredentials.propertiesというファイルを作り、以下のように取得したapi tokenをセットします    
slack.bot_api_token=xoxb-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx 
  
1.https://mariadb.com/kb/en/library/about-mariadb-connector-j/ からMariadb用のjarをダウンロード  
2.プロジェクト上で、右クリック  
3.ビルド・パス>ビルド・パスの構成>ライブラリー>外部JARの追加  
4.ダウンロードしたMariaDBの.jarを選択>適用>適用して閉じる  
5.README2.mdを参照してデータベースを作成  
  
1.ChickenBot/src/main/java/org/example/ChickenBot.java右クリック>実行>javaアプリケーション  
2.SlackでBotに対してチャンネル、メンション、ダイレクトの3種類から「!メニュー」を送信  
