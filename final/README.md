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
2. Student's t-test is adopted to examine the significance of relationships ([Hypothesis Testing for Collocations](https://nlp.stanford.edu/fsnlp/promo/colloc.pdf)).
3. Given several interested questions, we can visualize their connection and strength as below.

| <img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/final/visualization/t_test_vis3.png">  | <img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/final/visualization/t_test_vis2.png">  |  <img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/final/visualization/t_test_vis1.png"> |
|---|---|---|

4. Also, with the aid of the real investment data for each user, we generate a interaction matrix and treat funds as items.
5. [LightFM](https://github.com/lyst/lightfm) is used to implement the factorization of interaction matrix for funds recommendation.
6. To discover discriminative questions, we leverage [LightGBM](https://github.com/microsoft/LightGBM), an implementation of Gradient Boosting Decision Trees, with prediction target of risk index (Expected shortfall, Standardivation) to compute the feature importance.

|Part of tree |
|---|
|<img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/final/visualization/part_of_tree.png">   |

| w/ Investment data  |  w/o Investment data |
|---|---|
|  <img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/final/visualization/y_weight_feature_importance.png"> | <img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/final/visualization/y_mean_feature_importance_without_amount.png">  |

# Our Team
* 戴如宜  `財金系碩士班` `r07723062`
* 湯忠憲  `資料科學學程碩士班` `r06946003` `thtang@nlg.csie.ntu.edu.tw`
* 陳熙  `資工系碩士班` `r07922151`

# Reference
* 基金風險報酬等級分類標準 [[link]](https://www.moneydj.com/funddj/notes/rrnotes/rrnotes.htm)
* 中華民國證券投資信託暨顧問商業同業公會證券投資信託基金募集發行銷售及其申購或買回作業程序 [[link]](http://www.selaw.com.tw/LawArticle.aspx?LawID=G0101073&ModifyDate=1080328&rng=17)
* Metadata Embeddings for User and Item Cold-start Recommendations [[link]](https://arxiv.org/abs/1507.08439)
* LightGBM: A Highly Efficient Gradient Boosting Decision Tree [[link]](https://papers.nips.cc/paper/6907-lightgbm-a-highly-efficient-gradient-boosting-decision-tree)
* Collocations [[link]](https://nlp.stanford.edu/fsnlp/promo/colloc.pdf)
