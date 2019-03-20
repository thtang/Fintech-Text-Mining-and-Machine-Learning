# ETF crawler

## packages
* pandas: Data visualization. Doing preprocessing with original data to filter some new ETF. And save the processed data to csv format.
* requests: Get the data from Yahoo finacne by crawler
* re : Regular expression helps us to find some keys in the raw HTML

## Flow chart
![image](https://github.com/thtang/Fintech-Text-Mining-and-Machine-Learning/blob/master/hw1/ETF_crawler_flowchart.png)

## Possible Problems
* Some packages may not be installed. Just install them by pip or conda.
* Because of some network problem or other problem, the requests.get() may failed, you should check your network status ,modify timeout value and try for more times.
* Since Yahoo finance is sensitive to your cookie settings, you should use the right crumble in the code, or you should clear your cookie.
* You should put the 'Total Bond Market ETF List (82).csv' in the same directory with the code.
* Some data maybe lost in Yahoo Finance, so we decided to obtain the data from other website.