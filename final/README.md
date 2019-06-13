<img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/final/visualization/logo2.png" width=80> Julia: Give You A Better Choice
===========
Julia is a recommender system based on machine learning methods.

Main advantages of Julia:
* For customers:
  - Data driven.
  - Comfort to use.
  - Get your foot in the door !
* For banks:
  - Attractive to user.
  - Reduce the cost.
  - Benefit to running a comprehensive KYC.

## Get Started
* Follow Line ID <b>@705ijejy</b> or scan the QR code below: <br><img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/final/visualization/705ijejy.png" width=180>
* Say "<b>嗨</b>" to Julia. <br><img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/final/visualization/62375490_339107223430898_7475202257256972288_n.png" width=280>
* Julia will guess your interests once you ...
  - type <b>user ID</b> of you are an regular customer:<br><img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/final/visualization/62375490_339107223430898_747520225288_n.png" width=280>
  - key in "<b>回答問題</b>" and pick up one answer: <br><img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/final/visualization/64484645_1028972093973824_6274146208055296000_n.png" width=280>  <img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/final/visualization/62470169_451843808712758_31400634995768832_n.png" width=280>

## How it works
1. We construct the relationship matrix of questions by computing their co-occurrence rate. 
2. Student's t-test is adopted to examine the significance of relationships. 
3. Given several interested questions, we can visualize their connection and strength as below.

| <img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/final/visualization/t_test_vis3.png">  | <img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/final/visualization/t_test_vis2.png">  |  <img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/final/visualization/t_test_vis1.png"> |
|---|---|---|

4. Also, with the aid of the real investment data for each user, we generate a interaction matrix and treat funds as items.
5. LightFM is used to implement the factorization of interaction matrix for funds recommendation.
6. To discover discriminative questions, we leverage LightGBM, an implementation of Gradient Boosting Decision Trees, with prediction target of risk index (Expected shortfall, Standardivation) to compute the feature importance.

|Part of tree |
|---|
|<img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/final/visualization/part_of_tree.png">   |

| w/ Investment data  |  w/o Investment data |
|---|---|
|  <img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/final/visualization/y_weight_feature_importance.png"> | <img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/final/visualization/y_mean_feature_importance_without_amount.png">  |
