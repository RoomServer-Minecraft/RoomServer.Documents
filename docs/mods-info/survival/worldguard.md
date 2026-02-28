# WorldGuard

## WorldGuardとは？

「WorldGuard」とは、指定エリアでのプレイヤーの行動を制限することで、範囲内の建造物を保護するMODです。  
コマンド操作により、ブロックの破壊やアイテムの使用などに、制限をかけることができます。

{% hint style="success" %}
**WorldGuardでできることは次の通りです**

* **建築できるプレイヤーの限定**
* **指定エリアへの進入の制限**
* **ドアやチェストの開閉の制限**
* **指定エリアでの延焼の無効化**
* **指定エリアでの爆発の無効化**

**など**
{% endhint %}

このプラグインで、皆さんの建築を、荒らしやルールの違反者から守ります！

{% hint style="warning" %}
運営に申請してのみ、保護を書けることができます。

保護されるまでの期間・保護がかかっていない建設途中/建造物の荒らしについては原則自己責任となります。

（荒らし復旧時に使用する資材は申請することで貸与されます。余った資材はすべて返却または燃やして消す必要があります。）
{% endhint %}

保護された後、チケットはそのまま残されます。（保護以外のことでの使用は禁止です。）

## 権限一覧

> すべて運営に申請する必要があります。

<table>
	<thead><tr><th width="292">名称</th><th width="331">説明</th><th>デフォルト</th></tr></thead>
	<tbody>
		<tr><td>`build`</td><td>保護領域内でオーナーとメンバー以外が建築できる</td><td>deny</td></tr>
		<tr><td>`chest-access`</td><td>保護領域内でオーナーとメンバー以外がチェストを開けれる</td><td>deny</td></tr>
		<tr><td>`vehicle-place`</td><td>保護領域内のオーナーとメンバー以外の乗り物設置</td><td>deny</td></tr>
		<tr><td>`vehicle-destroy`</td><td>保護領域内のオーナーとメンバー以外の乗り物除去</td><td>deny</td></tr>
		<tr><td>`block-break`</td><td>保護領域内でオーナーとメンバー以外がブロックを破壊</td><td>deny</td>
		</tr><tr><td>`block-place`</td><td>保護領域内でオーナーとメンバー以外がブロックを設置</td><td>deny</td></tr>
		<tr><td>`damage-animals`</td><td>保護領域内で友好的な動物への攻撃</td><td>deny</td></tr>
		<tr><td>`ride`</td><td>保護領域内でMOB(動物を含む)を乗り物に乗せる</td><td>deny</td></tr>
		<tr><td>`use`</td><td>保護領域内のオーナーとメンバー以外のドア/ボタン/レバー/感圧版などの使用</td><td>allow</td></tr>
		<tr><td>`sleep`</td><td>保護領域内での睡眠</td><td>allow</td></tr>
		<tr><td>`lighter`</td><td>保護領域内での火打石の使用</td><td>allow</td></tr>
		<tr><td>`fire-spread`</td><td>保護領域内での火災の広がり</td><td>allow</td></tr>
		<tr><td>`lava-fire`</td><td>保護領域内での溶岩での火災</td><td>allow</td></tr>
		<tr><td>`lightning`</td><td>保護領域内での落雷</td><td>allow</td></tr>
		<tr><td>`pvp`</td><td>保護領域内でのPVP</td><td>allow</td></tr>
		<tr><td>`water-flow`</td><td>保護領域内での水の流れ</td><td>allow</td></tr>
		<tr><td>`lava-flow`</td><td>保護領域内での溶岩流</td><td>allow</td></tr>
		<tr><td>`ice-form`</td><td>保護領域内の水が氷になる</td><td>allow</td></tr>
		<tr><td>`ice-melt`</td><td>保護領域内の氷が融解する</td><td>allow</td></tr>
		<tr><td>`snow-fall`</td><td>保護領域内に雪が積もる</td><td>allow</td></tr>
		<tr><td>`snow-melt`</td><td>保護領域内の雪が融解する</td><td>allow</td></tr>
		<tr><td>`leaf-decay`</td><td>保護領域内の葉崩壊</td><td>allow</td></tr>
		<tr><td>`tnt`</td><td>保護領域内でのTNT爆発</td><td>allow</td></tr>
		<tr><td>`enderman-grief`</td><td>保護領域内でのエンダーマンによるブロック抜き去り</td><td>allow</td></tr>
		<tr><td>`enderpearl`</td><td>エンダーパールを利用して保護領域内への侵入</td><td>allow</td></tr>
		<tr><td>`enderdragon-block-damage`</td><td>エンダードラゴンによる地形ダメージ</td><td>allow</td></tr>
		<tr><td>`ghast-fireball`</td><td>保護領域内でのガストのファイヤーボールの地形/プレーヤーダメージ</td><td>allow</td></tr>
		<tr><td>`creeper-explosion`</td><td>保護領域内でのクリーパー爆発による地形/プレーヤーダメージ</td><td>allow</td></tr>
		<tr><td>`other-explosion`</td><td>保護領域内でその他のMOBによる地形/プレーヤーダメージ</td><td>allow</td></tr>
		<tr><td>`mob-spawning`</td><td>保護領域内でのMOB発生</td><td>allow</td></tr>
		<tr><td>`mob-damage`</td><td>保護領域内でのＭＯＢからのダメージ</td><td>allow</td></tr>
		<tr><td>`pistons`</td><td>保護領域内でのピストンの利用</td><td>allow</td></tr>
		<tr><td>`grass-growth`</td><td>保護領域内での草ブロックの伝達</td><td>allow</td></tr>
		<tr><td>`mushroom-growth`</td><td>保護領域内でキノコの成長</td><td>allow</td></tr>
		<tr><td>`mycelium-spread`</td><td>保護領域内での菌糸の伝達</td><td>allow</td></tr>
		<tr><td>`soil-dry`</td><td>保護領域内での土壌の乾燥</td><td>allow</td></tr>
		<tr><td>`invincible`</td><td>保護領域内でプレイヤーが無敵</td><td>allow</td></tr>
		<tr><td>`send-chat`</td><td>保護領域内でのチャットの使用</td><td>allow</td></tr>
		<tr><td>`receive-chat`</td><td>保護領域内でのチャットの受信</td><td>allow</td></tr>
		<tr><td>`game-mode`</td><td>保護領域内でのゲームモードの設定（SURVIVAL , CREATIVE , ADVENTURE）</td><td>-</td></tr>
		<tr><td>`time-lock`</td><td>保護領域内の時間を固定(0-24000)。__global__用？</td><td>-</td></tr>
		<tr><td>`weather-lock`</td><td>保護領域内の天気を固定(downfall , clear)</td><td>-</td></tr>
		<tr><td>`potion-splash`</td><td>保護領域内でのスプラッシュポーションの効果</td><td>allow</td></tr>
		<tr><td>`entity-item-frame-destroy`</td><td>MOBによる額縁の破壊</td><td>allow</td></tr>
		<tr><td>`entity-painting-destroy`</td><td>MOBによる絵画の破壊</td><td>allow</td></tr>
		<tr><td>`item-pickup`</td><td>保護領域内でアイテムを拾う</td><td>allow</td></tr>
		<tr><td>`item-drop`</td><td>保護領域内でアイテムを捨てる</td><td>allow</td></tr>
		<tr><td>`exp-drop`</td><td>保護領域内で経験値の獲得</td><td>allow</td></tr>
		<tr><td>`deny-message [メッセージ]`</td><td>保護領域内での行動を拒否されたプレイヤーへのメッセージ</td><td>-</td></tr>
		<tr><td>`entry`</td><td>保護領域内への侵入</td><td>allow</td></tr>
		<tr><td>`exit`</td><td>保護領域の外へ出る</td><td>allow</td></tr>
		<tr><td>`greeting`</td><td>領域に入った時のメッセージ<br>例：/flag [領域名] greeting [メッセージ]<br>%name%!で領域に侵入してきた人の名前が表示されます。</td><td>-</td></tr>
		<tr><td>`farewell`</td><td>領域を出た時のメッセージ</td><td>-</td></tr>
		<tr><td>`deny-spawn [MOB name1,MOB name2,...]`</td><td>指定したMOBの領域内でのスポーン<br>例：/rg flag deny-spawn SKELETON, CREEPER, ZOMBIE, ...</td><td>-</td></tr>
		<tr><td>`heal-delay [整数]`</td><td>体力回復速度の時間を秒単位で設定</td><td>-</td></tr>
		<tr><td>`heal-amount`</td><td>1回あたりの体力回復量の設定。１でハート半分</td><td>-</td></tr>
		<tr><td>`heal-min-health`</td><td>最小体力値</td><td>-</td></tr>
		<tr><td>`heal-max-health`</td><td>最大体力値</td><td>-</td></tr>
		<tr><td>`feed-delay [整数]`</td><td>満腹度回復速度の時間を秒単位で設定</td><td>-</td></tr>
		<tr><td>`feed-amount`</td><td>１回あたりの満腹度回復量を設定。１で半分</td><td>-</td></tr>
		<tr><td>`feed-min-hunger`</td><td>最小満腹度</td><td>-</td></tr>
		<tr><td>`feed-max-hunger`</td><td>最大満腹度</td><td>-</td></tr>
		<tr><td>`teleport [here｜x,y,z]`</td><td>テレポートポイントに設定。<br>/rg tp [保護エリア名]でテレポート</td><td>-</td></tr>
		<tr><td>`spawn`</td><td>保護領域内で死亡した時のスポーンポイント</td><td>-</td></tr>
		<tr><td>`blocked-cmds [コマンド1,コマンド2,...]`</td><td>指定したコマンドの使用を無効化</td><td>-</td></tr>
		<tr><td>`allowed-cmds [コマンド1,コマンド2,...]`</td><td>指定したコマンドのみ使用許可</td><td>-</td></tr>
		<tr><td>`send-chat`</td><td>領域内でのチャットの送信</td><td>allow</td></tr>
		<tr><td>`receive-chat`</td><td>領域内でのチャットの受信</td><td>allow</td></tr>
		<tr><td>`notify-enter`</td><td>オーナーとメンバー以外が保護領域内に入った時通知するか</td><td>deny</td></tr>
		<tr><td>`notify-leave`</td><td>オーナーとメンバー以外が保護領域から出た時通知するか</td><td>deny</td></tr>
	</tbody>
</table>
