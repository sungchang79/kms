## Security > Secure Key Manager > リリースノート

### 2021. 09. 28.
#### バグ修正
* 権限グループを利用して付与した権限の場合、認識が正常にできなかった問題を修正
* 使用履歴初期化ボタンが正常に動作しなかった問題を修正

### 2020. 03. 24.
* ユーザーがSecure Key Managerコンソールで作業した内容をCloud Trailに記録
* CSVファイルを使用した認証データ(IPv4アドレス/MACアドレス)の大量登録機能を追加
* CSVファイルを使用した認証データ(IPv4アドレス/MACアドレス)のダウンロード機能を追加

### 2019. 12. 24.

#### キー保存場所の画面を改善
* キー保存場所リストの表示方式を変更
* キー保存場所の下位メニューを変更
* キー保存場所にクイックメニューを追加

#### 使用履歴画面を改善
* プロジェクト単位でAPIの使用履歴を照会できるように変更

#### 統計画面を追加
* プロジェクト単位でAPI使用統計を照会できる画面を追加

### 2019. 07. 23.

#### UI改善
* テキストとボタンが重なって表示される現象を修正
* 日本語で画面を表示する時、テキストが改行される現象を修正

### 2019. 05. 28.

#### サービスリリース
* 機密データ(データベース接続情報、アプリケーションキー、パスワードなど)、対称鍵、非対称鍵などをアプリケーションサーバーに保存する場合、危険にさらされることがあるデータを中央集中的に安全に管理し、認証をパスしたクライアントのみアクセスできるように制御するサービスです。
