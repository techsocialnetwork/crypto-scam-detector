# Crypto Scam Detector - Roadmap

## ✅ Completed

### v1.0 - Basic On-Chain Analysis
- [x] Ethereum mainnet integration
- [x] Token name/symbol/ticker lookup
- [x] Total supply & decimals
- [x] Interactive D3.js holder graph
- [x] Risk scoring algorithm
- [x] Top holder concentration analysis
- [x] Pattern detection (basic)
- [x] Dark/light mode
- [x] Responsive design

## 🚧 In Progress / Planned

### v1.1 - Enhanced Analysis
- [ ] **Trades Over Time** (IN/OUT visualization)
  - Requires: Backend database for historical data
  - Storage: Time-series trade data
  - Display: Chart.js timeline graph
  - Features: Volume trends, buy/sell pressure
  
- [ ] Multi-chain support
  - BSC, Polygon, Arbitrum, Base
  
- [ ] Advanced pattern detection
  - Wash trading algorithms
  - Circular transaction detection
  - Liquidity rug pull indicators

### v1.2 - Backend Infrastructure
- [ ] Node.js/Python backend
- [ ] PostgreSQL/MongoDB database
- [ ] Cron jobs for data indexing
- [ ] WebSocket real-time updates
- [ ] Caching layer (Redis)

### v1.3 - Historical Data
- [ ] Trade history storage
- [ ] Price data integration
- [ ] Holder change over time
- [ ] Volume analysis
- [ ] Whale movement alerts

### v2.0 - Advanced Features
- [ ] Machine learning risk models
- [ ] Community reporting system
- [ ] Known scam database
- [ ] Browser extension
- [ ] Mobile app
- [ ] API for developers

## 📝 Technical Notes

### Trades Over Time - Implementation Plan

**Why Backend Needed:**
- Ethereum RPC has rate limits (5 calls/sec on free tier)
- Historical data requires scanning many blocks
- Storing trade data enables fast queries
- Real-time updates need WebSocket

**Architecture:**
```
Frontend (GitHub Pages)
    ↓ HTTP/WebSocket
Backend (Node.js/Vercel)
    ↓ Queries
Database (PostgreSQL/Supabase)
    ↓ Indexes
Blockchain (Ethereum RPC)
```

**Database Schema:**
```sql
trades (
    id SERIAL PRIMARY KEY,
    token_address VARCHAR(42),
    from_address VARCHAR(42),
    to_address VARCHAR(42),
    amount DECIMAL,
    timestamp TIMESTAMP,
    block_number INTEGER,
    tx_hash VARCHAR(66)
);
```

**Features:**
- Volume chart (IN vs OUT over time)
- Cumulative holder growth
- Large transaction alerts
- Price correlation (if available)

## 🎯 Next Priority

1. **Backend setup** (Vercel/Render + Supabase)
2. **Trade indexing service** (cron job)
3. **Time-series charts** (Chart.js)
4. **Real-time updates** (WebSocket)

## 💡 Ideas

- Heatmap of transaction times (detect bot patterns)
- Social sentiment integration (Twitter/Reddit)
- Contract similarity analysis (detect copy-paste scams)
- Cross-chain bridge monitoring
- NFT scam detection

---

*Last updated: April 20, 2026*
