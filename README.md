# Elysium Testnet Faucet

[![Live Faucet](https://img.shields.io/badge/Live%20Faucet-Open%20App-7d75ff?style=for-the-badge)](https://elysium-testnet-faucet--goodluckigweze.replit.app) [![License: MIT](https://img.shields.io/badge/License-MIT-59d99f?style=for-the-badge)](./LICENSE)

> A simple, safe, open-source faucet for developers building on Elysium Testnet.

## Live demo

Try the faucet here: **[elysium-testnet-faucet--goodluckigweze.replit.app](https://elysium-testnet-faucet--goodluckigweze.replit.app)**

## Demo

<video src="https://github.com/Goodluckigweze/elysium-testnet-faucet/raw/refs/heads/main/assets/elysium-faucet-demo.mp4" controls width="360"></video>

[Open the screen recording directly](./assets/elysium-faucet-demo.mp4) if the embedded player is not available in your GitHub view.

## What it does

- Connects to an EVM-compatible wallet such as MetaMask
- Automatically switches to Elysium Testnet or adds the network when needed
- Shows the connected wallet address and live ELYS token balance
- Lets each eligible wallet claim 100 ELYS through the faucet contract
- Enforces a **5-minute cooldown per wallet** between successful claims
- Displays clear pending, success, error, and cooldown messages
- Uses no token approvals and never requests permission to move user funds

## Network configuration

| Setting | Value |
| --- | --- |
| Network | Elysium Testnet |
| Chain ID | `99801` (`0x185d9`) |
| RPC URL | `https://testnet-rpc.elysium.kinetiq.xyz` |
| Token | Elysium Test Token (ELYS) |
| Claim amount | `100 ELYS` |
| Claim cooldown | `5 minutes per wallet` |
| Faucet contract | `0x245bFe8c6c2429f6a7743d53377Ae39b98500459` |

## Quick start

This is a single-file static website. There is no build step, backend, database, or environment variable required.

1. Download or clone this repository.
2. Open `index.html` in a browser, or serve the folder locally:

```bash
python3 -m http.server 8080
```

3. Visit `http://localhost:8080`.
4. Connect a wallet and claim test ELYS.
5. After a successful claim, wait 5 minutes before claiming again from the same wallet.

The cooldown is enforced by the faucet contract, so refreshing the page or reconnecting the wallet does not bypass it.

The page loads [ethers.js v6](https://docs.ethers.org/v6/) from the jsDelivr CDN.

## Project structure

```text
index.html   # Complete faucet application: markup, styles, and wallet logic
README.md    # Project documentation
LICENSE      # MIT license
```

## Safety

This faucet never asks for token approval and cannot drain your wallet. It is completely safe.

The app only requests the wallet connection needed to read the account, read the ELYS balance, and submit the faucet claim transaction. Always verify wallet prompts before signing any transaction.

## License

Released under the [MIT License](./LICENSE). You are welcome to use, modify, and redistribute this project.
