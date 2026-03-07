# 📘 宣戦布告システム

サバイバルサーバーでの戦争や宣戦布告、クラン（勢力）などのシステムを管理するためのMODです。  
コマンドや専用の画面を通じて、他のプレイヤーやクランに対して正当な手順で戦争を仕掛けることができます。

{% hint style="success" %}
**DeclarationCoreでできることは次の通りです**

* **クラン（陣営）の作成と管理**
* **ゲーム内GUIによる分かりやすい宣戦布告**
* **戦争状態の自動判定（PvPや破壊の許可制）**
* **Discordへの自動通知連携**
* **公平なルールに基づく戦争の進行**

**など**
{% endhint %}

このMODによって、Discordを持っていないプレイヤーでもゲーム内だけで完結して戦争に参加でき、ルールが明確化されることで安心してサバイバルを楽しむことができます！

{% hint style="warning" %}
戦争を開始するには、相手側の**明示的な合意**が必要です。
合意がない状態でのPvPや拠点破壊はシステムによって制限されており、これに違反する行為は禁止されています。
{% endhint %}

また、初期スポーン周辺の保護エリアや、運営に承認された公共施設などは、戦争中であっても破壊することはできません。


### クラン関連

<table>
	<thead>
		<tr>
			<th width="250">コマンド</th>
			<th>説明</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><code>/war clan gui</code></td>
			<td>クラン管理GUIを開きます。</td>
		</tr>
		<tr>
			<td><code>/war clan create &#x3C;name></code></td>
			<td>新しくクランを作成します。</td>
		</tr>
		<tr>
			<td><code>/war clan invite &#x3C;player></code></td>
			<td>他のプレイヤーを自分のクランに招待します。</td>
		</tr>
		<tr>
			<td><code>/war clan join &#x3C;name></code></td>
			<td>招待されたクランに参加します。</td>
		</tr>
		<tr>
			<td><code>/war clan leave</code></td>
			<td>現在所属しているクランから脱退します。</td>
		</tr>
		<tr>
			<td><code>/war clan disband</code></td>
			<td>所属しているクランを解散します（リーダーのみ）。</td>
		</tr>
		<tr>
			<td><code>/war clan info [all|leader|member|general]</code></td>
			<td>クランの情報を表示します。</td>
		</tr>
		<tr>
			<td><code>/war clan set war_leader auto</code></td>
			<td>クランリーダーをメンバー内からランダムに再選出します。</td>
		</tr>
		<tr>
			<td><code>/war clan set war_leader &#x3C;mcid></code></td>
			<td>指定したプレイヤーを新しいクランリーダーに設定します。</td>
		</tr>
		<tr>
			<td><code>/war allclan info</code></td>
			<td>サーバーに存在する全クランのメンバー一覧を表示します。</td>
		</tr>
	</tbody>
</table>

### 宣戦・戦争関連

<table>
	<thead>
		<tr>
			<th width="250">コマンド</th>
			<th>説明</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><code>/war fukoku</code></td>
			<td>宣戦布告メニューを表示します。相手や条件（PvP/破壊）を設定できます。</td>
		</tr>
		<tr>
			<td><code>/war accept &#x3C;id></code></td>
			<td>受け取った宣戦布告に同意します（GUI上からも可能です）。</td>
		</tr>
		<tr>
			<td><code>/war deny &#x3C;id></code></td>
			<td>宣戦布告を拒否します。</td>
		</tr>
		<tr>
			<td><code>/war cancel &#x3C;id></code></td>
			<td>送信した宣戦布告を取り消します。</td>
		</tr>
		<tr>
			<td><code>/war menu</code></td>
			<td>自分が関わっている宣戦の一覧を表示します。</td>
		</tr>
		<tr>
			<td><code>/war info [war_id]</code></td>
			<td>宣戦情報の詳細を表示します。</td>
		</tr>
		<tr>
			<td><code>/war help</code></td>
			<td>利用可能なコマンドのヘルプを表示します。</td>
		</tr>
	</tbody>
</table>

## 戦争のステータス

宣戦布告が行われると、状態（ステータス）は次のように変化します。

* **PENDING（合意待ち）**
  * 宣戦布告が送られ、相手の返答を待っている状態です。まだ戦争は始まっていません。
* **PREPARING（開始待機）**
  * 相手が合意し、戦争開始までの**5分間のカウントダウン**中の状態です。
* **ACTIVE（戦争中）**
  * 戦争が開始された状態です。設定されたルール（PvP/破壊）が有効になります。
* **ENDED（終了）**
  * 戦争が終了した状態です。

## ルールと制限

* **同時宣戦数**: 同時に関われる宣戦は最大2件までです（うち戦争中は1件まで）。
* **リーダー権限**: クランに所属している場合、宣戦布告や合意の判断ができるのはリーダー（または設定された戦争リーダー）のみです。
* **取り消し**: 合意前なら自由に取消可能ですが、合意後や戦争中は双方の合意が必要になります。