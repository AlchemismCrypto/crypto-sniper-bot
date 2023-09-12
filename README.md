<div align="center">
    <img src="https://i.imgur.com/WhSRUjY.png">
    <h3 align="center">Alchemism - Crypto Sniper Bot</h3>
    <img src="https://img.shields.io/discord/921546042346979388?color=5865F2&label=Discord&logo=discord&logoColor=white&raw=true"></img>
    <p align="center">
        Alchemism is a cryptocurrency sniper bot designed for efficiency and speed when trading on blockchain networks.
        <hr>
        <a href="#getting-started">⬇️ Download Lite Version</a>
        /
        <a href="https://github.com/zookyy/bsc-sniper/issues">🐞 Report a bug</a>
	/
        <a href="https://Alchemism.io">🌐 Visit our website</a>
	/
        <a href="https://Alchemism.io/discord">💬 Join our Discord</a>
	/
	<a href="https://t.me/Alchemismcrypto">💬 Join our Telegram</a>
    </p>
</div>

## Table Of Contents

<ul>
    <li>
		<a href="#description">Description</a>
		<ul>
			<li><a href="#features">Features</a></li>
			<li><a href="#supported-chains">Supported chains</a></li>
			<li><a href="#supported-tokens">Supported tokens</a></li>
		</ul>
	</li>
    <li>
        <a href="#getting-started">Getting started</a>
        <ul>
            <li><a href="#requirements">Requirements</a></li>
            <li><a href="#installation">Installation</a></li>
            <li><a href="#configuration">Configuration</a></li>
        </ul>
    </li>
	<li><a href="#go-premium">Go Premium</a></li>
	<li><a href="#contact">Contact</a></li>
</ul>


## Description
![Alt Text](https://i.imgur.com/8M3XqVQ.gif)

Alchemism is a fast and efficient cryptocurrency trading bot written in NodeJS. It automates the process of buying and selling tokens on blockchain networks as soon as liquidity is added and trading is enabled.
<br><br>
The bot operates with lightning speed when connected to a reliable node, such as one from Quicknode, allowing for buy/sell transactions in under 5 seconds.
<br><br>
The version of the bot available on GitHub is the lite version, offering basic functionality. The premium version provides access to additional advanced features.

### Features

Current features supported by the **FREE** version:

- [x] Buying (BNB & ETH pairs only)
- [x] Gas estimation system
- [x] Regular liquidity sniper

Additional features supported by the **premium** version:
- [x] Buying (ALL pairs)
- [x] Multi-blockchain support.
- [x] Bytecode checker / blocker.
- [x] MethodID waiter.
- [x] Multi-buy mode (all transactions are in the same block). 
- [x] Wrapped mode for any ETH-like token (BNB, MATIC, etc..). 
- [x] Tax checker (all pairs are supported)
- [x] Pinksale / dxsale support.
- [x] Sell using a delay
- [x] Sell using the space key
- [x] Auto / manual selling
- [x] Mempool sniping mode.
- [x] Block-offset system
- [x] Auto updates (updates are done automatically without the need of a re-download)
- [x] Trailing auto-sell.
- [x] Support

You can view the latest feature list here: [Alchemism Features](https://Alchemism.io/docs/#features)

### Supported chains
- Binance Smart Chain
- Arbitrum
- Avalanche
- Ethereum
- Polygon
- Cronos
- Milkomeda
- Metis
- Fantom
- Dogechain

To switch the blockchain the bot operates on, simply update the WSS_NODE endpoint in the config.ini file to the desired endpoint.

#### Public WSS Nodes
- Binance Smart Chain: wss://bsc-ws-node.nariox.org:443
- Ethereum: wss://main-light.eth.linkpool.io/ws
- Polygon: wss://rpc-mainnet.matic.network

_Note: These nodes listed above are free nodes and may not always be online._

### Supported tokens
The bot currently supports any token using the Uniswap interface.

## Getting Started
### Requirements
<ul>
    <li>Windows 10 / Ubuntu / Mac OS</li>
	<li>Latest <a href="https://nodejs.org/en/download/">NodeJS</a> installed.</li>
	<li>Latest <a href="https://git-scm.com/downloads">Git</a> installed.</li>
	<li>A <b>decent</b> internet connection.</li>
	<li>
		A <b>decent</b> BSC node, preferably paid, but free nodes are also an option.
		<ul>
			<li><a href="https://www.quicknode.com/">Quicknode (paid)</a></li>
			<li><a href="https://www.moralis.io/">Moralis (free)</a></li>
		</ul>
	</li>
	<li>A cryptocurrency wallet with a private key. (Creating a new wallet for use with this bot is recommended)</li>
</ul>

### Installation

Video tutorial: [Alchemism Installation](https://youtu.be/kNteZQmck4g)

1. Download and install NodeJS from [here](https://nodejs.org/en/download/).
2. Download and install Git from [here](https://git-scm.com/downloads).
3. Open a command prompt / terminal and clone the repository.
	```sh
	git clone https://github.com/zookyy/bsc-sniper.git && cd bsc-sniper
	```
4. In the same command prompt, install the NPM packages.
	```sh
	npm install
	```
5. Configuration is the next step. 🎉

### Configuration

```ini
[WALLET]
; This is your BSC wallet's private key.
SECRET_KEY=private_wallet_key

; A private node is recommended for better uptime. However, you may also use free nodes.
WSS_NODE=wss://bsc-ws-node.nariox.org:443


[CONTRACTS]
; These variables support some pre-defined contracts (BNB, ETH, BUSD). 
; For other contracts, you'll have to specify the contract address yourself.
INPUT=BNB
OUTPUT=BUSD


[TRANSACTION]

GAS_LIMIT=500000
GAS_PRICE=5

; This variable is the amount of cryptocurrency you wish to use with the input contract.
; For example, if you use WBNB as input, you will specify the amount in WBNB's format.
AMOUNT_IN=0.0033

BUY_SLIPPAGE=10
```

Usage

To launch the bot, use the command node index.js
Premium parameters
General
<table>
  <tr>
    <th>Parameter</th>
    <th>Description</th>
    <th>Accepts</th>
  </tr>
  <tr>
    <td>--buy-only</td>
    <td>Enables manual buy mode. This will only buy the token and then exit.</td>
    <td>-</td>
  </tr>
  <tr>
    <td>--sell-only</td>
    <td>Enables manual sell mode. This will only sell the token and then exit.</td>
    <td>-</td>
  </tr>
  <tr>
    <td>--input</td>
    <td>Overwrites the input parameter in the config.</td>
    <td><code>contract address</code></td>
  </tr>
  <tr>
    <td>--output</td>
    <td>Overwrites the output parameter in the config.</td>
    <td><code>contract address</code></td>
  </tr>
  <tr>
    <td>--config</td>
    <td>Used to specify a different config path (used for multi-config setups).</td>
    <td><code>string</code></td>
  </tr>
  <tr>
    <td>--force-approve</td>
    <td>Forces the approve transaction for the input/output. (used for debugging)</td>
    <td>-</td>
  </tr>
  <tr>
    <td>--simulate</td>
    <td>Simulate your current config as a real transaction.</td>
    <td>-</td>
  </tr>
</table>
Transaction
<table>
  <tr>
    <th>Parameter</th>
    <th>Description</th>
    <th>Accepts</th>
  </tr>
  <tr>
    <td>--wrapped</td>
    <td>Uses the wrapped version of the BNB/ETH token. (available for all blockchains)</td>
    <td>-</td>
  </tr>
  <tr>
    <td>--block-offset</td>
    <td>Waits for a specified number of blocks before sending out the buy transaction.</td>
    <td><code>number</code></td>
  </tr>
  <tr>
    <td>--spam</td>
    <td>Sends a specified number of transactions simultaneously. (spam buy)</td>
    <td><code>number</code></td>
  </tr>
  <tr>
    <td>--amount_in</td>
    <td>Specifies the amount you wish to spend with your INPUT token.</td>
    <td><code>number</code></td>
  </tr>
  <tr>
    <td>--amount_out</td>
    <td>Specifies the amount you wish to buy from your OUTPUT token.</td>
    <td><code>number</code></td>
  </tr>
  <tr>
    <td>--min_liq</td>
    <td>Specifies the minimum liquidity required before the bot starts to buy.</td>
    <td><code>number</code></td>
  </tr>
</table>
Tax
<table>
  <tr>
    <th>Parameter</th>
    <th>Description</th>
    <th>Accepts</th>
  </tr>
  <tr>
    <td>--verify-tax</td>
    <td>Checks whether the taxes for buying/selling do not exceed the configured limits.</td>
    <td>-</td>
  </tr>
  <tr>
    <td>--max-buy-tax</td>
    <td>Sets the maximum allowed buy tax.</td>
    <td><code>number</code></td>
  </tr>
  <tr>
    <td>--max-sell-tax</td>
    <td>Sets the maximum allowed sell tax.</td>
    <td><code>number</code></td>
  </tr>
</table>
Gas
<table>
  <tr>
    <th>Parameter</th>
    <th>Description</th>
    <th>Accepts</th>
  </tr>
  <tr>
    <td>--gas-price</td>
    <td>Sets the gas price.</td>
    <td><code>number</code></td>
  </tr>
  <tr>
    <td>--gas-limit</td>
    <td>Sets the gas limit.</td>
    <td><code>number</code></td>
  </tr>
</table>
Slippage
<table>
  <tr>
    <th>Parameter</th>
    <th>Description</th>
    <th>Accepts</th>
  </tr>
  <tr>
    <td>--buy-slippage</td>
    <td>Sets the buy slippage.</td>
    <td><code>number</code></td>
  </tr>
  <tr>
    <td>--sell-slippage</td>
    <td>Sets the sell slippage.</td>
    <td><code>number</code></td>
  </tr>
</table>
Autosell
<table>
  <tr>
    <th>Parameter</th>
    <th>Description</th>
    <th>Accepts</th>
  </tr>
  <tr>
    <td>--sell-with-multiplier</td>
    <td>Enables the sell with multiplier autosell mode.</td>
    <td>-</td>
  </tr>
  <tr>
    <td>--sell-multiplier</td>
    <td>Sets the multiplier to sell at for the sell with multiplier mode.</td>
    <td><code>number</code></td>
  </tr>
  <tr><td></td><td></td><td></td></tr>
  <tr>
    <td>--sell-with-delay</td>
    <td>Enables the sell with delay autosell mode.</td>
    <td>-</td>
  </tr>
  <tr>
    <td>--sell-delay</td>
    <td>Sets the delay to sell with for the sell with delay mode.</td>
    <td><code>number</code></td>
  </tr>
  <tr><td></td><td></td><td></td></tr>
  <tr>
    <td>--sell-on-loss</td>
    <td>Enables the sell on loss autosell mode.</td>
    <td>-</td>
  </tr>
  <tr>
    <td>--sl-minimum-multiplier</td>
    <td>Sets the minimum multiplier for the sell on loss mode to start.</td>
    <td><code>number</code></td>
  </tr>
  <tr>
    <td>--sl-percentage</td>
    <td>Sets the percentage of the maximum impact on your multiplier.</td>
    <td><code>number</code></td>
  </tr>
</table>
Go Premium
<p>
	For a full list of premium features, refer to the [Features](#features) section.<br>
	If you are interested in purchasing the premium version of the bot, please contact us using the contact methods listed below.
</p>
Contact
<ul>
	<li>Discord: Zooky.#1003</li>
	<li>Telegram: @zookyy</li>
</ul>
```
