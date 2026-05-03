# Venera (VNR) CPU Mining Guide

Simple step-by-step guide to mine **Venera (VNR)** using **XMRig** on Linux.

---

## ⚡ Requirements

- Linux (Ubuntu/Debian recommended)
- CPU with RandomX support
- Basic terminal knowledge

---

## 📦 Install dependencies

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install git build-essential cmake automake libtool autoconf -y
````

---

## ⬇️ Download XMRig

```bash
wget https://github.com/xmrig/xmrig/releases/download/v6.24.0/xmrig-6.24.0-linux-static-x64.tar.gz
tar -xzf xmrig-6.24.0-linux-static-x64.tar.gz
cd xmrig-6.24.0
```

---

## ⚙️ Configure miner

```bash
nano config.json
```

Paste:

```json
{
  "autosave": true,
  "cpu": {
    "enabled": true,
    "huge-pages": true,
    "asm": true
  },
  "randomx": {
    "mode": "fast",
    "1gb-pages": false,
    "rdmsr": true,
    "wrmsr": true,
    "numa": true
  },
  "pools": [
    {
      "url": "mine.veneralabs.org:9099",
      "user": "YOUR_WALLET_HERE",
      "pass": "x",
      "tls": true,
      "keepalive": true
    }
  ]
}
```

---

## ▶️ Start mining

```bash
./xmrig -c config.json
```

Or limit threads:

```bash
./xmrig -c config.json -t 24
```

---

## 🌐 Resources

| Resource | Link |
|--------|------|
| 🌍 Website | https://veneralabs.org/ |
| ⛏ Mining Pool | https://pool.veneralabs.org/ |
| 👛 Wallet | https://wallet.veneralabs.org/ |
| 💬 Discord | https://discord.gg/CtbUTCx3m7 |




---

## 🚀 About Venera

Venera (VNR) is a privacy-focused cryptocurrency based on the Cryptonote protocol (similar to Monero), designed for CPU mining using RandomX.

The project is evolving into a hybrid ecosystem:

- 🔒 Proof-of-Work (PoW) base layer (mining)
- ⚡ Future Proof-of-Stake (PoS) payment layer
- 🧠 Zero-knowledge proofs (ZK) for scalable and private transactions
- 💱 Stablecoins (USDV / EURV) backed by VNR

The goal is to build a decentralized and privacy-oriented payment system.

---

## ⛏ Mining & Rewards

Mining Venera allows you to earn:

- VNR (native coin)
- USDT (via pool rewards)

### 🏆 Miner Tier System (based on uptime)

| Tier | Boost | Requirement | Daily Crates |
|------|------|------------|-------------|
| Standard | 0% | None | 1 |
| Silver | +0.4% | 14 days uptime | 1 |
| Gold | +0.8% | 28 days uptime | 2 |
| Diamond | +1.3% | 50 days uptime | 3 |

👉 Higher uptime = higher rewards + more crates

---

## 🎁 Staking Rewards

You can also earn rewards by staking VNR:

| Staked Amount | Rewards |
|--------------|--------|
| 5,000 VNR | 2 daily crates |
| 10,000 VNR | 4 daily crates |
| 25,000 VNR | 2 platinum crates |
| 50,000 VNR | 2 platinum + 1 USDT crate |
| 100,000 VNR | 5 platinum + 3 USDT crates |

✔ Rewards are distributed every 30 days  
✔ No expiration on crates  

---

## 📄 Whitepaper & Vision

Venera is evolving toward a **sharded Layer-1 blockchain** with:

- Zero-knowledge proofs (ZK-SNARKs)
- High throughput payments
- Stablecoin infrastructure
- Cross-chain bridge

👉 Full details:  
https://veneralabs.org/whitepaper

---

## 🌐 Resources

| Resource | Link |
|----------|------|
| 🌍 Website | https://veneralabs.org/ |
| ⛏ Mining Pool | https://pool.veneralabs.org/ |
| 👛 Wallet | https://wallet.veneralabs.org/ |
| 💬 Discord | https://discord.gg/CtbUTCx3m7 |

---

## ⚠️ Disclaimer

This is an early-stage project.  
Always do your own research before mining or investing.
