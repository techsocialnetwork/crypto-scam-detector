# 🛡️ Crypto Scam Detector

A web-based tool to analyze cryptocurrency wallets and tokens for suspicious activity patterns, potential scams, and risk factors.

🔗 **Live Demo**: https://techsocialnetwork.github.io/crypto-scam-detector/

## Features

### 🔍 Wallet Analysis
- Scan any wallet address across multiple chains
- Detect connections to known scam projects
- Identify suspicious transaction patterns

### ⚠️ Risk Detection
- **Risk Score**: 0-100 calculated from multiple factors
- **Known Scam Connections**: Links to confirmed rug pulls
- **Wash Trading Detection**: Artificial volume between wallets
- **Liquidity Risk**: LP token ownership concentration
- **Token Concentration**: Supply held by few wallets
- **Creator Anonymity**: Team verification status

### 🌐 Multi-Chain Support
- Ethereum (ETH)
- Binance Smart Chain (BSC)
- Polygon (MATIC)
- Arbitrum
- Base
- Solana

### 📊 Analysis Results
- Risk score with visual indicator
- Detailed alert cards for each risk factor
- Connected wallets/projects table
- Transaction volume tracking

### 🎨 UI Features
- Dark/Light mode toggle
- Responsive design
- Real-time analysis simulation
- Clean, intuitive interface

## How It Works

1. **Enter** a wallet address or token contract
2. **Select** the blockchain network
3. **Click** Analyze
4. **Review** the risk score and detailed findings

## Risk Factors Analyzed

| Factor | Description |
|--------|-------------|
| Known Scam Connections | Links to wallets/projects confirmed as scams |
| Wash Trading | Circular transactions to fake volume |
| Liquidity Ownership | % of LP tokens held by creator |
| Token Concentration | % of supply held by top wallets |
| Contract Verification | Is source code public? |
| Creator Anonymity | Known team vs anonymous developers |

## Disclaimer

⚠️ This tool provides automated analysis based on on-chain data patterns. It is **not financial advice** and should not be the sole basis for investment decisions. Always conduct your own research (DYOR).

## Tech Stack

- Pure HTML/CSS/JavaScript
- No backend required (demo mode)
- Chart.js for visualizations
- Responsive design

## Future Enhancements

- [ ] Real blockchain API integration
- [ ] Machine learning risk models
- [ ] Historical scam database
- [ ] Community reporting system
- [ ] Browser extension
- [ ] Mobile app

## License

MIT License
