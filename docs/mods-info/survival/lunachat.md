# LunaChat

## LunaChatとは？

「LunaChat」とは、チャットのチャンネルを指定できるMODです。  
半角英数字だけのローマ字も、日本語に変換することもできます。（例えば、"kakkakun" → "かっかくん" のように表示されます）

### コマンド一覧

<table>
	<thead><tr><th>コマンド</th><th>説明</th></tr></thead>
	<tbody>
		<tr><td>`/ch create <channel>`</td><td>新しいチャットチャンネルを作成する</td></tr>
		<tr><td>`/ch join <channel>`</td><td>指定したチャンネルに参加する</td></tr>
		<tr><td>`/ch join !`</td><td>発言先を通常チャットに戻す（グローバルチャットへ）</td></tr>
		<tr><td>`/ch leave`</td><td>現在参加中のチャンネルから退出する</td></tr>
		<tr><td>`/ch list [page]`</td><td>チャンネル一覧を表示。参加中・未参加などが色分け表示される。ページ指定も可</td></tr>
		<tr><td>`/ch info`</td><td>チャンネル의メンバー情報（オンライン・オフライン、モデレーター）を表示する</td></tr>
		<tr><td>`/ch log [d=YYYY][p=名][f=キーワード]`</td><td>当日または指定日のログを表示。プレイヤー名やキーワードでフィルタ可能</td></tr>
		<tr><td>`/ch accept`</td><td>招待されたチャンネルの参加を承諾する</td></tr>
		<tr><td>`/ch deny`</td><td>チャンネルへの招待を拒否する</td></tr>
		<tr><td>`/ch hide [channel]`</td><td>特定チャンネルの発言を非表示にする（指定省略で現在のチャンネル）</td></tr>
		<tr><td>`/ch unhide [channel]`</td><td>非表示にしたチャンネルの発言を再表示する</td></tr>
		<tr><td>`/jp off`</td><td>日本語変換（Jp機能）をオフにする（英語入力を優先したい時など）</td></tr>
		<tr><td>`/jp on`</td><td>日本語変換をオンにする</td></tr>
	</tbody>
</table>

## 補足（便利な使い方例）

例えば、特定の仲間だけで話せる「秘密チャット」を作りたい場合...

1. `/ch create mysecret` で新規チャンネル作成。
2. `/ch join mysecret` で参加。
3. `/ch option password=abc123` でパスワード設定。
4. 仲間のみ参加を許可すれば、安全に会話ができます。

ゲームによってはチーム限定チャットやPvP用チャットなど、用途に応じた運用が柔軟に行えるのが魅力です。