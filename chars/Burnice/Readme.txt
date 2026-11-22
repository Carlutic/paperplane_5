更改[左/右Bust01]骨的付与率，可以調整乳搖幅度，值越小乳搖效果越小。[*由於使用付与親，在PmxEditor中測試胸部物理時將不會起作用，需要在MMD中進行測試。]
[左/右Bust01]ボーンの付与率を変更することで胸の揺れの振幅を調整でき、値が小さいほど胸の揺れの効果が小さくなります。[*付与親を使用しているため、PmxEditorで胸の物理演算をテストしても効果が現れません。MMDでテストする必要があります。]
Change the payment rate of [左/右Bust01] bone, you can adjust the shaking amplitude, the smaller the value, the smaller the shaking effect. [*Since '付与親' is used, testing breast physics in PmxEditor will not work. You need to test it in MMD.]

目前測試[左/右足ＩＫ]的Loop為40，單位角為114.592的時候動作流暢。如果出現抖動的動作可以參考以下提示進行調整。[X測試不足]
現在、[左/右足IK]のテストでは、Loopを40、単位角を10に設定すると動作がスムーズになります。もし動作が揺れる場合は、以下のヒントを参考に調整してください。[テスト不足]
Currently, testing the [left/right leg IK] with a Loop of 40 and a unit angle of 10 results in smooth motion. If jittery motion occurs, you can refer to the following tips for adjustment.[Insufficient testing]

為了解決部分穿模問題隱藏了部分身體網格，所以請盡可能使用表情來隱藏衣服，如有必要使用表情[身體Full*]顯示完整身體。
一部のクリッピング問題を解決するために、一部のボディメッシュを非表示にしています。そのため、可能な限り表情を使用して衣装を隠してください。必要に応じて、表情[身體Full*]を使用して完全なボディを表示してください。
To address some clipping issues, parts of the body mesh have been hidden. Therefore, please try to use expressions to hide the clothing as much as possible. If necessary, use the expression [身體Full*] to display the full body.


1. 單位角太小的情況：
當單位角設定得太小時，每次迭代的旋轉角度非常小，導致 MMD 可能在單幀內無法完成所有 IK 計算，動作表現不夠流暢。
這種情況下會出現一些問題，比如：
即使沒有播放動畫，IK 骨骼也會慢吞吞地變化（「うにょーん」是形象化的描述，類似於動作被拉長或變形的感覺）。
如果試圖快速移動 IK 骨骼，角色的骨骼追隨動作會顯得緩慢、遲鈍，表現出拖延的效果。

2. 單位角太大的情況：
當單位角設定得過大時，每次旋轉角度增量過大，使得 IK 計算的精度變低。
這會帶來以下問題：
計算結果變得粗糙，可能需要增加 Loop 次數來彌補精度不足。
動作可能會出現「抖動」（「ぷるぷる」是描述 IK 骨骼快速細微抖動的效果），特別是在接近目標位置時尤為明顯。

3. 調整建議：
設定 IK 的 Loop/單位角 時，建議先將這些值設定為較大的初始值。
然後逐步減少 Loop 次數，以找到動作的平衡點。
接下來，逐漸減少單位角的值，直到 IK 動作達到流暢、自然的效果。