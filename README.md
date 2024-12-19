
# Automated Trading Bot for Binance

This project implements an automated trading bot using the Binance API. It analyzes moving averages to identify buying and selling opportunities for assets, operating continuously.

---

## **How It Works**

The bot performs the following steps:

1. **Data Retrieval**:
   - Uses the Binance API's `get_klines` function to fetch the price history (candlesticks) of a specified asset.
   - Converts the data into a pandas DataFrame for easier indicator calculations.

2. **Strategy**:
   - Calculates two moving averages: a short-term one (7 periods) and a long-term one (40 periods).
   - Compares the moving averages:
     - If the short-term average exceeds the long-term average, the bot buys the asset.
     - If the short-term average falls below the long-term average, the bot sells the asset.

3. **Order Execution**:
   - Operates through market orders, buying or selling the specified amount.

4. **Continuous Loop**:
   - Repeats the above steps every hour, ensuring real-time operations.

---

## **Development Environment**

To run this project, you need the following environment:

- **Operating System**: Windows, macOS, or Linux
- **Python**: Version 3.8 or higher
- **Required Libraries**:
  - `pandas`
  - `python-binance`
  - `python-dotenv`

Make sure to install the dependencies using the command:
```bash
pip install -r requirements.txt
```

---

## **Best Practice: Protecting API Keys**

**Important:** Never expose your API private keys in public repositories, such as GitHub. Use `.env` files to securely store your credentials. This project uses the `python-dotenv` library to load keys directly from the `.env` file. Example configuration:

`.env`:
```plaintext
KEY_BINANCE=YourAPIKey
SECRET_BINANCE=YourSecretKey
```

---

## **Disclaimer**

This bot is not an investment recommendation. It was created for educational purposes only. The cryptocurrency market is volatile and carries significant risks. Before using this code, ensure you understand the risks involved.

**We suggest** taking the course offered by the [Varos platform](https://plataforma.varos.com.br/) for a better understanding of this bot's functionality and trading strategies.

---

## **License**

This project is distributed under the MIT License. See the `LICENSE` file for more details.
