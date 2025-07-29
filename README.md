# ChainLet - Web3 Wallet (Wagmi Version )

A comprehensive Web3 wallet application similar to MetaMask, featuring ERC-20 token support, faucet integration, and multi-account management.

## 🚀 Tech Stack

### Frontend (Client)
- **Framework**: Next.js 15.3.4
- **Styling**: Tailwind CSS 4
- **Web3 Integration**: Wagi + Viem
- **State Management**: Zustand 5.0.6
- **Notifications**: React Hot Toast
- **Development**: ESLint, PostCSS

### Backend (Smart Contracts)
- **Blockchain Framework**: Hardhat 2.25.0
- **Smart Contract Language**: Solidity ^0.8.28
- **Contract Standards**: OpenZeppelin Contracts 5.3.0
- **Network**: Ethereum Sepolia Testnet
- **RPC Provider**: Alchemy
- **Verification**: Etherscan API integration

## ✨ Features

### 🔐 Wallet Management
- **Multi-Account Support**: Create and manage multiple wallet accounts
- **Account Import/Export**: Import accounts via mnemonic phrases or private keys
- **Secure Storage**: Local storage with encrypted private key management
- **Account Switching**: Easy switching between multiple accounts
- **Account Deletion**: Safe account removal with confirmation

### 💰 Token Management
- **ETH Balance Tracking**: Real-time Ethereum balance monitoring
- **ERC-20 Token Support**: Add and manage custom ERC-20 tokens
- **Token Balance Display**: Automatic balance updates for all tokens
- **Token Transfer**: Send ETH and ERC-20 tokens to other addresses
- **Transaction History**: View past transactions and their status

### 🚰 Faucet Integration
- **SHAN Token Faucet**: Integrated faucet for Shangesh (SHAN) tokens
- **Cooldown Management**: Automatic cooldown tracking between requests
- **Balance Monitoring**: Real-time faucet balance and availability
- **One-Click Claims**: Simple token claiming interface

### 🎨 User Interface
- **Modern Design**: Beautiful gradient backgrounds with animated elements
- **Responsive Layout**: Mobile-friendly responsive design
- **Dark Theme**: Elegant dark theme with purple/blue gradients
- **Toast Notifications**: Real-time feedback for all operations
- **QR Code Generation**: Generate QR codes for wallet addresses
- **Tab-Based Navigation**: Organized interface with multiple tabs

### 🔗 Blockchain Features
- **Sepolia Testnet**: Deployed on Ethereum Sepolia testnet
- **Real-time Data**: Live blockchain data integration via Alchemy
- **Transaction Confirmation**: Real-time transaction status updates
- **Gas Estimation**: Automatic gas fee calculation
- **Network Status**: Connection status monitoring

## 🏗️ Smart Contracts

### Shangesh Token (SHAN)
- **Contract Address**: `0x752e937d41F444f3eDe4A8A0632F1BfB8768DF4A`
- **Features**:
  - ERC-20 compliant token
  - Capped supply (10,000,000 SHAN)
  - Burnable tokens
  - Miner rewards system
  - Owner-controlled block rewards

### Faucet Contract
- **Contract Address**: `0x1E4081F2B2Ab3b66021598A35c469Ef08D81DB6A`
- **Features**:
  - Cooldown mechanism (1 minute default)
  - Configurable withdrawal amounts (50 SHAN default)
  - Owner controls for withdrawal limits
  - Balance monitoring
  - Emergency withdrawal functions

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ 
- npm or yarn
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd ChainLet
   ```

2. **Install Frontend Dependencies**
   ```bash
   cd client
   npm install
   ```

3. **Install Smart Contract Dependencies**
   ```bash
   cd ../ERC20_token
   npm install
   ```

4. **Environment Setup**
   Create a `.env` file in the `ERC20_token` directory:
   ```env
   ALCHEMY_SEPOLIA_RPC_URL=your_alchemy_url
   PRIVATE_KEY=your_private_key
   ETHERSCAN_API_KEY=your_etherscan_api_key
   ```

### Running the Application

1. **Start the Frontend**
   ```bash
   cd client
   npm run dev
   ```
   Open [http://localhost:3000](http://localhost:3000) in your browser.

2. **Smart Contract Development**
   ```bash
   cd ERC20_token
   npx hardhat compile
   npx hardhat test
   npx hardhat run script/deploy.js --network sepolia
   ```
   
## 🔧 Development

### Smart Contract Development
```bash
# Compile contracts
npx hardhat compile

# Run tests
npx hardhat test

# Deploy to Sepolia
npx hardhat run script/deploy.js --network sepolia

# Verify contracts
npx hardhat verify --network sepolia <contract-address> <constructor-args>
```

### Frontend Development
```bash
# Development server
npm run dev

# Build for production
npm run build

# Start production server
npm start

# Lint code
npm run lint
```

## 🌐 Network Configuration

- **Network**: Ethereum Sepolia Testnet
- **Chain ID**: 11155111
- **RPC URL**: Alchemy Sepolia endpoint
- **Block Explorer**: [Sepolia Etherscan](https://sepolia.etherscan.io/)

## 🔒 Security Features

- **Local Key Storage**: Private keys stored locally in browser
- **No Server Communication**: All sensitive operations happen client-side
- **Mnemonic Backup**: BIP-39 compliant mnemonic phrase generation
- **Transaction Confirmation**: Multi-step confirmation for all transactions
- **Input Validation**: Comprehensive validation for all user inputs

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](ERC20_token/LICENSE) file for details.

## 👨‍💻 Author

**Shangesh S** 

---
