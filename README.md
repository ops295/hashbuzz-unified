![alt text](hackathon-files/hashbuzz-logo.png)

**Project name: hashbuzz**

**Track 3: Immersive Experiences**

**Sub-track 4: Gamified Community Governance**

## 📘 The story of hashbuzz

In 2014, the Ice Bucket Challenge swept across social media. More than 17 million people posted videos. The campaign raised 115 million dollars for the ALS Association in a few weeks. That wave of attention proved two things. People will mobilize for a cause. Attention can move real value. [1](https://www.als.org/blog/als-ice-bucket-challenge-year-end-update-over-94-million-commitments-2014?utm_source=chatgpt.com)

What was missing was a fair way to reward the millions who created that value with their time, creativity, and trust. There was no open ledger of who contributed what. No simple way for communities and campaigners to align incentives, prove authenticity, and share value directly. The moment was powerful. The rails were not built for shared value. The result was a one-time spike instead of an ongoing, verifiable system. (For context on the totals and global scale [2](https://www.als.org/ibc?utm_source=chatgpt.com)).

Hashbuzz exists to make moments like that repeatable and fair. Promoters run on open rules. Engagement is recorded. Rewards flow to the people who earn them. Communities keep more of the value they create.

**Hashbuzz transforms the attention economy into a fair, participatory system that values cultural diversity and local context. By rewarding authentic voices with BUZZ tokens, we amplify influencers, strengthen communities, & help brands build genuine trust.**

![alt text](hackathon-files/shared-value-bee.png)


##  🔀 Hedera Integration Summary 
**Problem statement:** In Africa, micro creators and everyday engagers cannot prove genuine contributions or get paid fairly. Bots, edits, and duplicate entries distort engagement. Closed platforms fragment spend and settlement, so payouts are slow, disputable, and opaque. Local languages and norms are underserved, raising friction and fraud. Brands then face the knock-on problem: they cannot independently verify real reach, audit campaign spend, or reward communities transparently at scale.

Hedera Services Implementation in HashBuzz

**Hedera Token Service (HTS)**

HashBuzz uses HTS for BUZZ token creation and management, choosing it over ERC-20 contracts for its fixed $0.001 transfer fee vs. variable gas fees ($10+) on Ethereum. This predictable pricing makes micro-rewards for African social media engagement economically viable.
**Transaction Types:** TokenCreateTransaction, TokenAssociateTransaction, TokenTransferTransaction, TokenMintTransaction, TokenBurnTransaction
**Economic Justification:** Rewarding 10,000 participants costs $10 in fees vs. $100,000+ on Ethereum, enabling sustainable mass-adoption campaigns for African businesses with limited budgets.

**Hedera Smart Contract Service (HSCS)**
HSCS automates campaign lifecycle management with full Solidity compatibility at predictable fees ($0.02-0.05 per execution). Smart contracts handle escrow, milestone validation, and automated reward distribution at 10,000+ TPS.

**Transaction Types:** ContractCreateTransaction, ContractExecuteTransaction, ContractCallQuery, ContractUpdateTransaction, ContractDeleteTransaction

**Economic Justification:** Processing 1,000 reward distributions costs ~$50 vs. $5,000+ on Ethereum, making programmatic marketing accessible to African SMEs with $100-500 monthly budgets.

**Hedera Consensus Service (HCS)**

HCS provides immutable engagement logging at $0.0001 per message, creating tamper-proof records of Twitter interactions with consensus timestamps to prevent fraud.

**Transaction Types:** TopicCreateTransaction, TopicMessageSubmitTransaction, TopicUpdateTransaction, TopicDeleteTransaction, TopicInfoQuery

**Economic Justification:** Logging 1 million engagements costs $100 vs. $10,000+ for Ethereum events, making transparent marketing verification affordable for African businesses.

**ABFT Consensus Benefits**

3-5 second finality eliminates waiting for block confirmations, crucial for users with intermittent mobile connections. Immediate settlement reduces customer support costs and working capital requirements for campaign organizers.


## 🔗 Improtant files and links

**Team Certification:**
[Ahmed certification](hackathon-files/Ahmed_certificate.pdf) | [Andrew certification](hackathon-files/Andrew_certificate.pdf) | [Shiela certification](hackathon-files/Shiela_certificate.pdf)

**Pitch Deck Presentation:**
[Presentation](hackathon-files/Ahmed_certificate.pdf)

**Video Demo:**
[Youtube link](https://www.youtube.com/watch?v=WhHRjytDD_A)

**Smart Contract Audit:**
[Report](hackathon-files/REP-final-20241115T085933Z.pdf)

---
> **⚡ 10-Minute Setup**: Get HashBuzz running locally in under 10 minutes with our [Quick Setup Guide](#-10-minute-quick-setup)


## 🏗️ Repository Structure

```
hashbuzz-unified/
├── backend/                      # Node.js/Express API Server
├── frontend/                     # React/TypeScript Web Application  
├── smart-contracts/              # Hedera Smart Contracts (Solidity)
├── hackathon-files/              # File for Hedera Africa Hackathon
├── TECHNICAL_DOCUMENTATION.md    # Complete setup & development guide
├── ENVIRONMENT_SETUP.md          # Environment variables guide
└── README.md                     # This file
```

## 🚀 Platform Overview

HashBuzz is a revolutionary social media campaign platform built on Hedera Hashgraph that enables:

- **Twitter Campaign Management**: Create and manage engagement-based marketing campaigns
- **Smart Contract Rewards**: Automated reward distribution via Hedera consensus
- **Quest System**: Gamified user engagement with milestone-based rewards
- **Real-time Analytics**: Live campaign performance tracking and engagement metrics
- **Decentralized Verification**: Blockchain-backed proof of engagement and rewards

## 📋 Technical Stack

### Backend (`/backend/`)
- **Runtime**: Node.js 18+ with TypeScript 5.0+
- **Framework**: Express.js 4.18+ with V201 modular architecture
- **Database**: PostgreSQL with Prisma ORM
- **Blockchain**: Hedera Hashgraph SDK v2.x
- **Queue System**: Redis with Bull queue management
- **Authentication**: JWT with GitHub OAuth integration

### Frontend (`/frontend/`)
- **Framework**: React 18.3.1 with TypeScript
- **UI Library**: Material-UI v7 with custom theming
- **State Management**: Redux Toolkit with RTK Query
- **Build Tool**: Vite 6.0+ for fast development
- **Wallet Integration**: Hedera wallet connect support

### Smart Contracts (`/smart-contracts/`)
- **Language**: Solidity 0.8.x
- **Platform**: Hedera Smart Contract Service (HSCS)
- **Features**: Campaign lifecycle, reward distribution, token management
- **Security**: Multi-sig validation and emergency controls

---
## � Complete Setup & Documentation

### 📖 Main Documentation

| Document | Purpose | When to Use |
|----------|---------|-------------|
| **[TECHNICAL_DOCUMENTATION.md](./TECHNICAL_DOCUMENTATION.md)** | Complete setup, architecture, and development guide | **Start here** for full platform setup | 
| **[HEDERA_AND_HASHBUZZ.md](./HEDERA_AND_HASHBUZZ.md)**| A heigh level overview of commination between hashbuzz component and Hedera network | full platform setup|
| **[ENVIRONMENT_SETUP.md](./ENVIRONMENT_SETUP.md)** | Detailed environment variable configuration | When configuring API keys and credentials |
| **[Frontend README](./frontend/README.md)** | Frontend-specific setup and development | Frontend development and customization |
| **[Backend README](./backend/ReadMe.md)** | Backend API documentation and architecture | Backend development and API integration |
| **[Smart Contracts README](./smart-contracts/README.md)** | Contract deployment and blockchain integration | Smart contract development and deployment |




### 🏗️ Architecture Overview

```
┌─────────────┐    ┌─────────────┐    ┌─────────────┐    ┌─────────────┐    ┌─────────────┐
│   Frontend  │◄──►│   Backend   │◄──►│   Smart     │◄──►│   Hedera    │◄──►│  Mirror     │
│  (React)    │    │  (Node.js)  │    │  Contract   │    │  Network    │    │  Node       │
│             │    │             │    │             │    │             │    │             │
│ • User UI   │    │ • API Logic │    │ • Rewards   │    │ • Consensus │    │ • History   │
│ • Wallet    │    │ • Database  │    │ • Tokens    │    │ • Ledger    │    │ • Queries   │
│ • Auth      │    │ • Twitter   │    │ • Campaign  │    │ • HCS       │    │ • Analytics │
└─────────────┘    └─────────────┘    └─────────────┘    └─────────────┘    └─────────────┘
      │                   │                  │                  │                  │
      ▼                   ▼                  ▼                  ▼                  ▼
localhost:3000     localhost:4000     0.0.CONTRACT    testnet.hedera.com   testnet.mirrornode
```


### 📁 Environment File Structure

```bash
# Copy these example files and configure
cp frontend/.env.example frontend/.env    # Firebase, WalletConnect config
cp backend/.env.example backend/.env      # Database, APIs, Hedera config

# ⚠️ SECURITY WARNING: Never commit real credentials to version control
```

---

**HashBuzz Team** - Building the future of decentralised marketing on Hedera Hashgraph
