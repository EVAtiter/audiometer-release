# Privacy Policy / プライバシーポリシー

**Last updated / 最終更新日: 2026-06-29**

---

## 日本語

### 1. はじめに

Audio Meter VU（以下「本アプリ」）は、ユーザーのプライバシーを尊重します。本ポリシーは、本アプリがどのような情報を取り扱うか、または扱わないかを明示するものです。

### 2. 収集する情報

**本アプリは、いかなる個人情報も収集しません。**

具体的には以下のいずれも行いません:

- ユーザーアカウントの作成・管理
- 氏名・メールアドレス・電話番号などの個人情報の取得
- 位置情報の取得
- アプリ使用状況や利用統計の収集
- クラッシュレポートの自動送信
- 広告 ID・追跡 ID の収集
- 連絡先・カレンダー・写真など macOS の機密データへのアクセス

### 3. 本アプリが扱う音声について（重要）

本アプリは、VU メーターの針を振らせるために、お使いの Mac で**再生されているシステム音声**を Core Audio のプロセスタップ（`AudioHardwareCreateProcessTap`）でリアルタイムに読み取ります。このために macOS の「システムオーディオ録音」権限（`NSAudioCaptureUsageDescription`）の許可を求めます。

ただし本アプリは、音声に対して以下のことしか行いません:

- 受け取った音声から**音量レベル（左右チャンネルの振幅）のみ**を即座に算出し、針の表示に使います。
- 音声そのものを**録音・保存・記録しません**。レベルを算出した後の音声バッファは保持されず、ただちに破棄されます。
- 音声データを**ファイルに書き出したり、外部に送信したりすることは一切ありません**。
- 特定のアプリの音声を選り分けたり、その内容（会話・楽曲等）を解析・認識したりしません。本アプリが見るのはシステム全体のステレオミックスの**振幅の大きさ**だけです。

つまり本アプリが行うのは「録音」ではなく、音量計のための**一時的なレベル測定**だけです。

### 4. ローカルに保存されるデータ

本アプリは、以下の情報をお使いの Mac 上（UserDefaults / サンドボックスコンテナ）のみに保存します。これらは外部に送信されません。

- 表示モード（通常 / 最前面 / デスクトップに常駐）
- メーターウィンドウの位置・表示するディスプレイ
- 「再生に追従（自動スリープ）」などの UI 設定

これらのデータは、本アプリをアンインストールすることで削除されます。

### 5. ネットワーク通信

**本アプリはインターネット通信を行いません。**

- 外部サーバーへのデータ送信なし
- 外部 API の呼び出しなし
- アップデートチェックなし（App Store / Apple の更新メカニズム経由でのみ更新されます）

### 6. 第三者サービス

本アプリは、Google Analytics、Firebase、その他のアナリティクスや広告 SDK を一切利用していません。

### 7. 児童のプライバシー

本アプリは特定の年齢層を対象としたものではなく、また 13 歳未満の児童から意図的に個人情報を収集することはありません。

### 8. プライバシーポリシーの変更

本ポリシーは予告なく改定される場合があります。変更がある場合、本ページの「最終更新日」を更新します。

### 9. お問い合わせ

ご質問・ご意見は GitHub Discussions または Email までお願いします:

- GitHub Discussions: https://github.com/EVAtiter/audiometer-release/discussions
- Email: info@slack-kingdom.com

---

## English

### 1. Introduction

Audio Meter VU ("the App") respects user privacy. This policy outlines what information the App handles and does not handle.

### 2. Information We Collect

**The App does not collect any personal information.**

Specifically, the App does NOT:

- Create or manage user accounts
- Collect names, email addresses, phone numbers, or any other personal data
- Access location data
- Collect usage statistics or analytics
- Automatically send crash reports
- Collect advertising or tracking identifiers
- Access sensitive macOS data such as Contacts, Calendar, or Photos

### 3. About the Audio the App Handles (Important)

To move the VU meter needles, the App reads the **system audio currently playing** on your Mac in real time, using a Core Audio process tap (`AudioHardwareCreateProcessTap`). This is why the App requests the macOS "system audio recording" permission (`NSAudioCaptureUsageDescription`).

However, the only things the App does with that audio are:

- It computes **only the volume level** (left/right channel amplitude) from the incoming audio and uses it to drive the needles.
- It does **not record, save, or store** the audio itself. Audio buffers are discarded immediately after the level is computed and are never retained.
- It never writes the audio to a file or transmits it anywhere.
- It does not single out the audio of any specific app, nor analyze or recognize its content (speech, music, etc.). The App only looks at the **amplitude** of the system-wide stereo mix.

In other words, the App performs a transient level measurement for a volume meter — not recording.

### 4. Locally Stored Data

The App stores the following information only on your Mac (UserDefaults / sandbox container). None of it is transmitted externally.

- Display mode (normal / always-on-top / on the desktop)
- Meter window position and which display it appears on
- UI preferences such as "Follow playback (auto-sleep)"

This data is deleted when the user uninstalls the App.

### 5. Network Communication

**The App does not communicate over the internet.**

- No data transmission to external servers
- No external API calls
- No update checks (updates are delivered only via the App Store or Apple's update mechanisms)

### 6. Third-Party Services

The App does not use Google Analytics, Firebase, or any other analytics or advertising SDKs.

### 7. Children's Privacy

The App is not directed at any specific age group and does not knowingly collect personal information from children under 13.

### 8. Changes to This Policy

This policy may be revised without prior notice. When changes are made, the "Last updated" date at the top of this page will be updated.

### 9. Contact

For questions or feedback, please use GitHub Discussions or Email:

- GitHub Discussions: https://github.com/EVAtiter/audiometer-release/discussions
- Email: info@slack-kingdom.com
