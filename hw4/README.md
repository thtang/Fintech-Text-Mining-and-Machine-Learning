# ETF 評比績效理論實作
## Discussion

|  NIG Dist.	|  Dist. of most of other ETFs 	|
|---	|---	|
| <img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/hw4/AGZD_weekly.png">  	|  <img src="https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/hw4/LDUR_weekly.png"> 	|
1. 本組考慮的 ETF 中，多數 ETF 的 return 分配不符合 NIG distribution， 因此在計算 A 評比指標時會有許多 NaN 值。
2. 週資料或月結果評比相似嗎 ? 不相似
    * edit_distance for B between weekly and monthly data: 34
    * edit_distance for C between weekly and monthly data: 21
3. 不同指標評比結果相似嗎 ?
    * edit_distance for weekly data between B and C: 34
    * edit_distance for monthly data between B and C: 29
4. 整體而言，指邊間的排序差異大於周月資料的排序差異。
