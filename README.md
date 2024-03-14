### Project Requirements

#### Description:
Develop a Python script/bot to notify via Telegram about cryptocurrency prices based on the Relative Strength Index (RSI) indicator, using the Binance API.

#### Background:
When trading any asset, mathematical calculation-based indicators are commonly used to generate entry and exit signals. The RSI helps us to get a general idea of where our asset stands, whether it's overbought or oversold. Many traders use the crossing of certain levels (for example, 70 for overbought signals and 30 for oversold signals) as entry or exit signals in the market. For instance, a cross above 70 could be a sell signal, while a cross below 30 could be a buy signal.

#### Requirements:

1. **Github Repository Creation**:
   - Create a Github repository for this project.

2. **Python Virtual Environment (VENV)**:
   - Set up a Python virtual environment configured to use the necessary libraries.
   - Python 3.9 should be used.

3. **Business Rules**:
   - The script will receive as arguments the cryptocurrency symbol (e.g., "BTCUSDT") and its time interval (e.g., 1m, 3m, 5m, 15m, 30m, 1h, 2h, 4h, 6h, 8h, 12h, 1D, 3D).
   - The Binance public API will be used to fetch cryptocurrency data: [Binance API](https://api.binance.com/api/v3/klines?symbol=BTCUSDT&interval=15m&limit=100).
   - If the script does not receive arguments, it should have default values to make the request.
   - The script will run infinitely, making constant requests to the Binance API to obtain data for RSI calculation.
   - While the script is running you should print in terminal the following values: DATE - SYMBOL - PRICE - RSI_VALUE (Recommend logging library and enable colors)

4. **RSI Rules**:
   - If RSI <= 30 or RSI >= 70, send notification.

#### Additional Information:
- Binance API Documentation: [Binance API Docs](https://binance-docs.github.io/apidocs/spot/en/#general-info)
- klines: https://binance-docs.github.io/apidocs/spot/en/#kline-candlestick-data
- Current symbol information: https://binance-docs.github.io/apidocs/spot/en/#current-average-price
  - last price endpoint: GET /api/v3/ticker/price


### TEST

Running the script in terminal should look like this:

```bash
python main.py BTCUSDT 1h
