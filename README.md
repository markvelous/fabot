# Remarkable Flashloan Arbitrage Bot (FABOT)

Time to make some fictitious arbitrages between Uniswap V2 and Sushiswap

>Bot is still a work in progress ... 

In consideration of CSA, this bot has not been deployed live (yet) and is used to demonstrate the understanding of the subject

This demo shows the bot in action on a forked ethereum mainnet.

## Installation

```bash
npm install
npm install -g ganache-cli
git clone https://github.com/sushiswap/sushiswap.git
```

Open a new terminal and run the following with the RPC URL
```bash
ganache-cli --fork https://rinkeby.infura.io/v3/[API KEY] -b 2 -d
```

Run the demo script with either a or b option 
```bash
node ./src/demo_environment.js -a
#or
node ./src/demo_environment.js -b
```

The script will create two tokens and their correspond liquidity pools on Uniswap and Sushiswap with certain amounts that make an arbitrage opportunity possible.

Create a .env file on the root project directory with the following paremeters:

```bash
ADDR_ARBITRAGE_CONTRACT = [Arbitrage contract hash]
ADDR_UTILS = [Utility contract hash]
ADDR_TOKEN0 = [Token 0 hash]
ADDR_TOKEN1 = [Token 1 hash]
PRICE_TOKEN0 = [Price of Token 0]
PRICE_TOKEN1 = [Price of Token 1]
PRIVATE_KEY = [Receiver wallet private key]
PROJECT_ID = [RPC API key, e.g. infura]

ADDR_DAI = '0x6b175474e89094c44da98b954eedeac495271d0f'
ADDR_ETH = '0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2'
ADDR_SFACTORY = '0xC0AEe478e3658e2610c5F7A4A2E1777cE9e4f2Ac'
ADDR_SROUTER = '0xd9e1cE17f2641f24aE83637ab66a2cca9C378B9F'
ADDR_UFACTORY = '0x5C69bEe701ef814a2B6a3EDD4B1652CB9cc5aA6f'
ADDR_UROUTER = '0x7a250d5630B4cF539739dF2C5dAcb4c659F2488D'
LOCAL_DEPLOYMENT = true
VALID_PERIOD = 5
```

`I am still working on this ...`

Execute the bot for flashswap or normalswap
```bash
node ./src/bot_flashswap.js
#or
node ./src/bot_normalswap.js
```
Once there is an arbitrage (shown in the console logs), stop the bot (Ctrl-C). 

## License

[MIT](https://tldrlegal.com/license/mit-license)
