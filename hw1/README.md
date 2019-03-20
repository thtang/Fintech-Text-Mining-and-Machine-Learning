# ETF crawler

## packages
* pandas: Data visualization. Doing preprocessing with original data to filter some new ETF. And save the processed data to csv format.
* requests: Get the data from Yahoo finacne by crawler
* re : Regular expression helps us to find some keys in the raw HTML

## Flow chart
![image](https://www.draw.io/?lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=ETF_crawler.drawio#R3ZnbcpswEIafxjPthTuADMa3cZ0007pJ43Q6k5uODItRIhARwoc8fQUIA8b2OI0d6ubCA6sDq%2F33Y5HSQcNgecVx5I%2BZC7RjaO6ygz53DKNvW%2FI3NayUoa%2Fnhhknbm6qGCbkBZRRU9aEuBDXOgrGqCBR3eiwMARH1GyYc7aod%2FMYrT81wjNoGCYOpk3rL%2BIKP7fahlXavwCZ%2BcWTdWuQt0yx8zTjLAnV8zoG8rK%2FvDnAxVxqobGPXbaomNCog4acMZFfBcsh0DS0RdjycZc7Wtd%2BcwjFIQMerhfh1979cmIx9vj71kvm9rg7sPNp5pgmUKwj81asigiBKwOmbhkXPpuxENNRab3IogDpczR5V%2Fb5xlgkjbo0PoIQK6U%2BTgSTJl8EVLU216KWF7OEO7BvAUqn1MnKSBWCK2ABCL6SHThQLMi8rjpWyTNb91sPvWVE%2BmJoKs%2BRqWRUaa4jrT6FwHwGQo0qZZAXFTdKUybOa4SyGkLdAXbTheFFikc8T7OfSD0Mjckc1Eb3l%2FKXkljEDUlLwdLoL3wiYBLhLNALSXldHDkpHTLKeDYWuSbYbk%2FaY8HZE1RabGOKLGufnHPgApZ7dVKtxqAe74KiRcmoXtj8Cp%2BWtlvZmiavFUDX0Lmjol5ceabuXapxbKjeFPrC8UrkLwkVwPMsj7O0kFkhpwkdiARhYeqGl%2FcwNN3s6kYX6Q256mK8EgMMtudsw8BybJh6R8Kgv%2FnaMZocWFs46J%2BOA%2FPMOThBeh9WM9Dmy%2BnENWO90IpUN1OBSYqH8NNK8ZxgSjwC7rpgxKtgyui%2BknEurBi9%2FvuxMuix5OLl4W41HieT796PZ%2F3G7zbD3x4pG8n%2Bt%2Bj0mjVk69JbLRhrN3cnfsSJU%2F1USotIEpNwljn5nID8bPoQQgaGDKjc3wCmZaFxGHsi8PGolHi2A85WSqa22TO101CCLPTJbJmTplrnw8nu7D%2BAEvROlOxzshL1n3GGBg5dHBd5z%2FNdRk5NtsuwcJAmcjiNoyxq2kRwCc71TYFT3tfFArfDRwOGLSIezEev32uZjubO78zpQAfSYbZJR3O3NwGaHkBtVhCH0STINhxhCgqOIsguiCgQKnnwOA7gP4DCtLdsx98Vin%2Fp3OooULw12Q%2FbgtjGybYgu1dVp4iyeYqDhwnNvq4cHMNxtxvtMGEN2maieUwywfONV4%2BWVfbqaWEbR4NvC%2FzG0aCtne5sUN6WJ%2FQ5FOV%2FQdDoDw%3D%3D)

## Possible Problems
* Some packages may not be installed. Just install them by pip or conda.
* Because of some network problem or other problem, the requests.get() may failed, you should check your network status ,modify timeout value and try for more times.
* Since Yahoo finance is sensitive to your cookie settings, you should use the right crumble in the code, or you should clear your cookie.
* You should put the 'Total Bond Market ETF List (82).csv' in the same directory with the code.
* Some data maybe lost in Yahoo Finance, so we decided to obtain the data from other website.