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
