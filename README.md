# QPBot Prime

やっつけで書いたReadmeです。バグ報告、機能要望は直接ご報告いただくか、Githubのissueまで。 \
コードは当面公開しない予定です。Django, python-telegram-botなどで実装されています。

## 利用方法

- まずはイベントを作成する、しないに関わらずBotとの個別チャットで ```/start``` を実行してください。

- イベントを確認する場合は ```/ff``` を実行してください。チャットルームでは短縮版が、個別チャットでは参加表明を行ったイベントの詳細版と参加者リスト、参加ボタンが表示されます。

- イベントは8名集まると通知が出ます。このとき、主催者にメンションが飛び、イベントの開催ボタンが表示されます。

- イベントを開催確定すると、参加と未定を選択した人にメンションが飛びます。

- イベント開始1時間前に通知が出ます。このとき、主催者にメンションが飛び、イベントの中止ボタンが表示されます。

- イベント開始30分前に通知が出ます。このとき、参加と未定を選択した人にメンションが飛びます。

- イベントの作成は個別チャット内で ```/create``` を実行してください。

- 最長1年後のイベントが作成可能です。

- イベントのタイトルは255文字までです。絵文字も入るよ。

- イベントの詳細は8,191文字までです。URLを入れた場合はプレビューが1つだけ出ます。

- イベント作成者はイベントの各項目の編集、イベントの開催確定、イベントの中止を行うことができます。

- Botがいる他のチャットルームにイベントを共有し、参加者を募ることができます。

## FAQ

1. Q> チャットでイベント参加ボタンなどを押しても何も反応がない。 \
   A> Botとの個別チャットで ```/start``` を実行してください。実行後はボタンを押したら個別が飛んでくるようになります。

## 実装予定の機能

気が向いたら実装するものリスト。バグ報告、機能要望はGithubのissueまで。

- 管理者機能の実装
  - イベント作成者以外も編集、中止ができる権限を付与する。

- 集合場所をイベント情報に付与する。

- Google Calendar連携機能
  - イベントをGoogle Calendarに登録する。

## 更新履歴

### v3.0.0

- Botを全てのチャットルームで動作するようにしました。

### v2.13.4

- python-telegram-bot 20.4を導入したことにより、現行のコードを刷新しました。以下のURLの変更内容を適用しています。
<https://github.com/python-telegram-bot/python-telegram-bot/wiki/Transition-guide-to-Version-20.0>

### v2.10.1

- 開催確定は1度だけ送ることができるように変更しました。
- 過日のイベントについて、開催確定および中止を行うことができないように変更しました。

### v2.10.0

- イベント開催確定機能を追加しました。現時点では一度イベントの開催を確定すると解除できませんが、確定通知を何度も送ることができます。

### v2.9.0

- サイコロを振れるようになりました。

### v2.7.4

- python-telegram-bot 12.2.0を導入したことにより、現行のコードを刷新しました。以下のURLの変更内容を適用しています。
<https://git.io/fxJuV>

### v2.7.0

- チャットルーム情報を更新するための ```/refresh``` コマンドを追加しました。新しいチャットルームに入った場合はこちらのコマンドを実行してください。

### v2.6.2

- すでに存在しないチャットルームに入っていた場合、```/create```と```イベントの転送```で送信先のチャット一覧が表示されないバグを修正しました。

### v2.6.0

- 個別での```/ff```実行時に不参加者のリストを表示するようにしました。

### v2.5.1

- ボタンを押した際に出てくる処理中のアイコンを止める処理を追加しました。押しても反応が分かりにくいという点が少し軽減されていると思います。

### v2.5.0

- イベント開始1時間前に通知が出るようになりました。このとき、主催者にメンションが飛び、イベント中止ボタンが表示されるようになりました。

### v2.4.2

- イベントが転送できない問題を修正しました。([#1](../../issues/1))

### v2.4.1

- ```/start``` 実行時に表示されるメッセージを修正。

### v2.4.0

- 初版リリース
