# README 
各リポジトリの説明

mtn-2021が自分のアカウント

mtn-2021の編集部分はファイルのページを開いて表示をBlameに変更すれば確認可能

# Tetris2D
* C++でテトリスを実装
* c++の勉強用に作成
* オリジナリティとして縦軸にぬるぬる動く
* 製作期間5日

|file name|sammary|
|:-:|:-:|
|Tetris2D.cpp|本体|
|* peace.h|ピースの挙動を定義|
|その他|フレームワークにより自動生成|

# NOCCA-NOCCA_byAI
* 講義の自由課題でチーム制作したノッカノッカというボードゲーム
* pythonを使用、CUIのみ
* ファイル名がばらばら（メンバーに特に指定しなかったため）
* mtn-2021の主な担当部分はゲーム本体（NoccaNocca.py）と木の展開部分（MakeTree.py）
  * 別のユーザーも編集しているのはPCが手元にない時にメンバーのPCを借りて編集したため
* それ以外にもオブジェクトの定義やバグの除去も担当
* NOCCA_selecteval.pyの担当者がプログラミング初心者だったため補助
* 製作期間3日（自身の担当分のみ）

|file name|sammary|
|:-:|:-:|
|NoccaNocca.py|本体|
|State.py|ボードの状態を表すオブジェクト|
|Operator.py|状態遷移の命令を表すオブジェクト|
|stateTranstion.py|Operatorを受けてボードを変化させる関数|
|Nocca_AI.py|AIを呼び出す関数|
|MakeTree.py|AIのためにボードの木を展開する関数|
|StateNode.py|木のノードを表すオブジェクト|
|evaluateState.py|展開した木の末端を評価する関数|
|NOCCA_selecteval.py|評価から次のAIの手を決定する関数|

# SoftwareArchAssignment
* 講義の自由課題で友人と共同で作成した簡単なメモ共有Webアプリ
* フレームワークはクライアントがReact、サーバがExpress、言語はTypeScript
* データベースはMongoDB
* 実装したブランチはclient-impl
* mtn-2021の担当はクライアント側すべてとサーバ側の極一部
* /srcにソースコード
* 製作期間5日（自身の担当分のみ）

***クライアント側***
|directory name|sammary|
|:-:|:-:|
|components|UIの構成要素|
|images|ロゴなどの画像|
|routes|URL関係のデータ・処理|
|types|型定義|
|utils|その他、使いまわせる処理|

***サーバ側***
|directory name|sammary|
|:-:|:-:|
|router|アクセスをルーティング|
|handler|アクセスを受けて処理|
|repository|データベースへアクセス|

# jaeger & jaeger-ui
* オープンソースの分散トレーシングシステム（をフォークしたリポジトリ）
* jaegerはGo、jaeger-uiはJavaScript & TypeScript
* 研究関連のリポジトリ
* 研究として開発している分散システムの動作を監視する目的で利用
  * 利用する際のデータベースはApache Cassandra を使用
* 開発している分散システムの特異な動作を監視しやすくするため研究の一環として機能を追加
  * 追加したブランチはdisplay-nodes  
  * 編集箇所が分散しているためファイルの詳細は省く（Comparing changes で編集箇所は一応確認可能）
  * 以下のようなUIを追加
    * 分散システム上の特定のサーバに他のサーバからどれだけリクエストが送られたかを表示（棒グラフ）
    * その特定のサーバの状態も表示（散布図・画像ではストレージ残量）
    * 以上を同時に表示するのはサーバの状態によってリクエスト数を調整できていることを確認するため

  ![put_storage_1](https://user-images.githubusercontent.com/86408868/156929640-eb6db068-72bd-40b1-8f84-0bc80984c299.png)

