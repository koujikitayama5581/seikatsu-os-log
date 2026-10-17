# 生活OSログ Ver.1.39 PWA（iPhone 12）

## 大事なこと
- **アップロードするのは `index.html`、`manifest.webmanifest`、`sw.js`、3枚のPNGアイコン、合計6ファイル**です。ZIP自体をアップロードするのではありません。
- アプリのコードはWeb上に公開されますが、入力した生活記録・写真は各端末のブラウザ保存領域に保持され、通常の利用でGitHubには送信されません。非公開アプリの仕組みではありません。
- **iPhoneとMacのデータは自動同期されません**。Macのデータを移すにはMacのJSONバックアップをiPhone側で復元します。
- 保存はブラウザに依存します。iPhoneのストレージ整理やアプリ削除等で消える可能性があるため、定期的にJSONを書き出してください。
- 元のHTML（Ver.1.38）とその記録は消さないでください。

## GitHub Pagesで設置（無料）
1. MacBookのブラウザで https://github.com を開いてアカウントを作成・ログイン。
2. 右上＋ → New repository。名前を例えば `seikatsu-os-log` と入力し、Publicを選び、Create repository。
3. `Add file` → `Upload files` で、このフォルダ内の6ファイルをアップロードし、Commit changes。
4. リポジトリの `Settings` → `Pages` → `Build and deployment` のSourceで `Deploy from a branch`、Branchは `main`、フォルダは `/ (root)` としてSave。
5. しばらくするとPages画面に `https://＜アカウント名＞.github.io/seikatsu-os-log/` が表示されます。**表示された実際のURL**を利用してください。

## iPhone 12への追加
1. iPhone 12でSafariを起動し、上記URLを開き、カレンダーが表示されることを確認。
2. Safariの共有ボタン → `ホーム画面に追加` → `追加`。
3. ホーム画面の「生活OSログ」アイコンから起動。
4. ネットがある状態で1回開いた後、機内モードでも開くか試す（最初の読み込みに成功している必要があります）。
5. 必ずテスト記録を入力して、アプリを閉じて開き直し、記録が残るか確認。

## 旧MacデータをiPhoneに移す
Macの古いHTML → メニュー → バックアップ・復元 → JSONを保存。ファイルをAirDrop等でiPhoneへ。iPhoneのホーム画面版で、バックアップ・復元 → JSONから復元を選択して読み込み。**復元はiPhone側の記録を上書きします**。

## 更新に関する注意
更新時は同じGitHub PagesのURLを使い続けてください。別のアドレスだと別の保存領域になります。サービスワーカーはオフラインキャッシュを使うため、コード更新後に再起動を要することがあります。Ver.1.39では登録／オフライン起動は実ブラウザで要確認です。
