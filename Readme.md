# 🟣 Zaino Desktop  
### A Developer Toolkit for Building, Testing & Debugging on the Zcash Ecosystem

Zaino Desktop is an all-in-one **local development environment** for the Zcash ecosystem.  
It provides a friendly UI for running nodes, building shielded transactions, exploring RPCs,  
and testing wallets on **testnet** or **regtest** — without needing to manually manage configs, nodes, or CLI tools.

This tool is built for **wallet developers**, **protocol researchers**, **node operators**,  
and **Zcash ecosystem builders** who want a faster way to prototype and debug privacy-preserving applications.

---

## 🚀 Features

### 🖥️ 1. Node Manager
Run and manage a local Zcash node with one click.

- Start/stop Zebra or zcashd  
- Testnet or Regtest mode  
- Live sync status (height, peers, uptime, progress)  
- Real-time logs viewer (filter + search)  
- Regtest mining controls:
  - Mine 1 block  
  - Auto-mine mode  
- Optional: edit node configs

---

### 🧪 2. RPC Playground
A Postman-style interface for exploring Zcash RPC methods.

- Preloaded RPC calls:
  - `getblockchaininfo`, `getrawtransaction`, `z_listaddresses`  
  - `z_sendmany`, `z_getoperationstatus`, `getblock`, etc.
- Auto-suggest RPC method names  
- Save custom RPC requests  
- JSON formatter with highlighting  
- Request history  
- Error inspector  
- Works with Zebra or zcashd RPC

---

### 🔐 3. Shielded Transaction Builder & Decoder
Build, sign, broadcast, and inspect shielded transactions visually.

#### Transaction Builder
- Select source wallet/address  
- Enter recipient, amount, memo  
- Orchard or Sapling  
- Fee estimator  
- Build → Sign → Broadcast (testnet/regtest)

#### Transaction Decoder
- Decode raw hex → show full transaction structure  
- Visualize:
  - Notes (value, diversifier, orchard/sapling)  
  - Nullifiers  
  - Anchors & Merkle path  
  - Proof generation/verification result  
- Export JSON or hex  
- Compare transactions side-by-side (optional)

---

### 👛 4. Wallet Dev Sandbox
A safe, isolated environment for wallet experimentation.

- Create or import:
  - Seed phrase  
  - Viewing key (read-only)  
- Generate shielded addresses  
- QR code for receiving  
- Live balances (shielded + transparent)  
- Transaction history  
- Send transactions via Transaction Builder  
- Regtest Auto-Fund:
  - “Fund with 10 ZEC” (mines a block instantly)

---

## 📦 Tech Stack

- **Electron.js** — desktop shell  
- **React + TypeScript** — frontend UI  
- **Rust** — core engine (IPC bridge, wallet, transaction logic)  
- **Zebra / zcashd** — node backend  
- **librustzcash / orchard / zcash_primitives** — cryptography, TX building  
- **WASM** — fast client-side decoding & key ops  
- **SQLite or filesystem storage** — encrypted wallet storage  

---

## 📚 Getting Started

### **Prerequisites**
- Rust stable
- Node.js ≥ 18
- Yarn or npm
- Docker (optional, for managed Zebra)
- macOS/Linux (Windows support in progress)

---

## 🔧 Installation

```bash
git clone hhttps://github.com/Timi16/Zaino-desktop
cd zaino-desktop
yarn install
