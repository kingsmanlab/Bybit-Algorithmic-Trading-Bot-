# Bybit-Algorithmic-Trading-Bot-
Algorithmic Bitcoin Trading Bot for Bybit Exchange Writing on Java

![Java](https://img.shields.io/badge/JDK-14%2B-blue)
![JavaFx](https://img.shields.io/badge/JAVAFX-14%2B-yellowgreen) 
![Jfreechart](https://img.shields.io/badge/Jfreechart-Custom-orange)

## STILL WORK IN PROGRESS

### Some ScreenShot

<p align="center"><img width=100% height=35% src="https://i.ibb.co/5xBqZDL/ss1.jpg"></p>

<p align="center"><img width=100% height=35% src="https://i.ibb.co/Fw7tR8w/ss2.jpg"></p>

### Indicators used for the bot 
  - vwap for Trend Indicators
    * vwap really good indicators to get what average price for the asset, from my research many big Institutional using this.
    * and i modified vwap and add 2 line more from vwap, to get overbought and oversell price. (why not just use rsi ? just doing research urself why i dont use rsi for that ^_^ )
  - using Donchian Channel for Signal entry.
   * donchian will give line for get what high price and low price on period last candle, on this bot i using 50 candle period.
   * donchian used too for detect sideways trends.
  - using 3 sma : SMA25,SMA50,SMA200 
   * SMA will use to make sure signal from Donchian is valid or not.
   
 ### Method
   - Algo method for bot to make decision is not like usual, i make algo with calculation price range interract with indicator, not like if price crossing sma25 buy, or if price        crossing sma50 sell. I already tried that traditional method, but Risk Reward Ratio not profitable.
   - This is an example backtest of the method that i made 
      <p align="center"><img width=100% height=50% src="https://i.ibb.co/t3ttMK6/ss3.jpg"></p>      
      <p align="center"><img width=100% height=50% src="https://i.ibb.co/ZK20Jqb/ss4.jpg"></p>
   - Backtest using 13 Days Data with 5Minutes TimeFrame. From Backtest bot still dont doing much trades, but with that small trades bot likely profit on win and lose compaison.
   - Bot use SQLite for store data market from the past.
   - Bot use Websocket connection to bybit for realtime data and RestApi for others call.
  
### WHY BYBIT?
  - on USDT Perpetual Markets, we can make Long and Short position in the same time in one account.
  - Bybit have good features like Stop lose, Trailing Stop and positive fee for market maker.
  - Maybe Binance or Bitmex Good too, but i want to try implement on bybit first, because with that bybit features i dont need to much hard coding.
  - from API Doc bybit have good limit rate for calling Rest API.

### Limitation will come later
  - Maybe later on first release, u will cant add ur custom indicators with this bot,but u still can modified stoploss and take profit triggers,and some calculation for make         decicison signal entry.
  - Bot will have 2 version, Regular and Pro version.
  - Maybe only support for USDT Perpetual market, why? because for each asset need different Algo method.
  - only using 5 minutes TimeFrame, why? because different timeframe need different calculation for the algorithm. so this bot will optimized for 5 Minutes TimeFrame.
  
### interesting for Contributing? 
  - if u have experience on trading, java and javaFx. u can contributing on this project. just DM me on discord -> h4ckm3-+#0960
