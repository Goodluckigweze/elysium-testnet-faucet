# Elysium Testnet Faucet

A clean, open-source faucet for claiming 100 ELYS on Elysium Testnet.

## Use it

Open `index.html` directly in a browser or host it with any static hosting provider such as GitHub Pages, Netlify, or Cloudflare Pages. No build step or environment variables are required.

The page uses ethers.js v6 from a CDN and connects directly to the user’s EVM wallet. It never asks for token approval.

## Network details

| Setting | Value |
| --- | --- |
| Network | Elysium Testnet |
| Chain ID | `99801` (`0x185d9`) |
| RPC | `https://testnet-rpc.elysium.kinetiq.xyz` |
| Token | Elysium Test Token (ELYS) |
| Faucet contract | `0x245bFe8c6c2429f6a7743d53377Ae39b98500459` |

## Run locally

Because wallet providers can restrict local file URLs, serve the folder with a small static server when testing locally:

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080` and connect MetaMask or another compatible EVM wallet.

## Safety

This faucet never asks for token approval and cannot drain your wallet. It is completely safe.

## License

MIT. See [LICENSE](LICENSE).
