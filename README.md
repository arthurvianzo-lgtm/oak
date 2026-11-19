 ██████╗ ██████╗ ██╗ ██████╗ ███╗   ██╗     ██████╗  ██████╗ ██╗  ██╗
██╔═══██╗██╔══██╗██║██╔═══██╗████╗  ██║    ██╔═══██╗██╔══██╗██║ ██╔╝
██║   ██║██████╔╝██║██║   ██║██╔██╗ ██║    ██║   ██║███████║█████╔╝
██║   ██║██╔══██╗██║██║   ██║██║╚██╗██║    ██║   ██║██╔══██║██╔═██╗
╚██████╔╝██║  ██║██║╚██████╔╝██║ ╚████║    ╚██████╔╝██║  ██║██║  ██╗
 ╚═════╝ ╚═╝  ╚═╝╚═╝ ╚═════╝ ╚═╝  ╚═══╝     ╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝
OAK Protocol — Orion Agnostic Kernel

Layer-0 Security Primitive for Autonomous Agents executing High-Impact Actions
Protocol Maturity Governance Test Status License

Overview

OAK is a domain-agnostic, reality-verification kernel that enables autonomous agents to execute economically significant actions only when real-world events are cryptographically verified and temporally validated.

Core Innovation: Sovereignty of Truth through physics-anchored constraints, multi-nature oracle convergence, and stake-based economic security.

The Problem

Autonomous agents that trigger economic outcomes (payments, minting, actuator control) face a fundamental security challenge: self-reported telemetry can be fabricated. An AI can generate synthetically consistent data that passes naive validation, extracting value without real-world verification.

OAK Solution:

✅ Temporal verification (physics-based speed limits)
✅ Multi-nature oracle convergence (≥2 independent proof sources)
✅ Economic stake/slashing mechanism
✅ On-chain enforcement
Architecture

┌─────────────────────────────────────────────────────────────┐
│                    REALITY VERIFICATION LAYER                │
│  ┌─────────────┐  ┌──────────────┐  ┌─────────────────────┐ │
│  │   Sensor    │  │   Temporal   │  │   Multi-Nature      │ │
│  │   Network   │  │   Logic      │  │   Convergence       │ │
│  │  (Oracles)  │  │ (Physics)    │  │  (≥2 Sources)       │ │
│  └──────┬──────┘  └──────┬───────┘  └──────────┬──────────┘ │
│         └─────────────────┼─────────────────────┘            │
│                           │                                  │
└───────────────────────────┼────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                    GOVERNANCE LAYER (2.0)                    │
│  ┌─────────────┐  ┌──────────────┐  ┌─────────────────────┐   │
│  │   Gnosis    │  │   Timelock   │  │      RBAC Roles     │   │
│  │   Safe 2/3  │→ │   24h Delay  │→ │  (PAUSER/CONFIG/    │   │
│  │             │  │              │  │   TREASURY/FUND)   │   │
│  └─────────────┘  └──────────────┘  └─────────────────────┘   │
└───────────────────────────┼───────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                    KERNEL LAYER (Production)                 │
│              OrionMetabolismV2_2_RBAC.sol                    │
│  ┌────────────────────────────────────────────────────────┐  │
│  │  • Reality Verification    • Economic Metabolism        │  │
│  │  • Chrono-Validation       • Stake/Slash Mechanism    │  │
│  │  • Oracle Convergence      • Reward Distribution      │  │
│  │  • Emergency Pause         • RBAC Governance          │  │
│  └────────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────┘
Key Features

Production-Grade Governance

RBAC: Role-based access control (6 defined roles)
Timelock: 24-hour execution delay for safety
Safe: 2-of-3 multi-sig with hardware wallets
Emergency: Immediate pause capability with multi-sig recovery
Reality Verification

Temporal Logic: Physics-based speed limits prevent impossible events
Oracle Convergence: Minimum 2 proofs from distinct natures (DIGITAL, PHYSICAL, BIOLOGICAL)
Economic Security: Stake-based verification with slashing
Economic Metabolism

Fixed Cost: 0.10 OET per action (predictable pricing)
Distribution: 60% sensors / 20% burn / 20% treasury
Deflationary: Automatic burn mechanism
Quick Start

Installation

git clone https://github.com/arthurvianzo-lgtm/oak-protocol
cd orion_oak
npm install
Environment Setup

cp .env.example .env
# Edit .env with your RPC endpoints and keys
Build & Test

# Compile contracts
npx hardhat compile

# Run test suite
npm test

# Start CLI
npm run oak -- --help
Repository Structure

orion_oak/
├── 📁 contracts/              # Production smart contracts
│   ├── OrionMetabolismV2_2_RBAC.sol   # Core kernel (current)
│   ├── OrionToken.sol                 # OET token
│   └── interfaces/                    # Contract interfaces
│
├── 📁 archive/                # Historical preservation
│   ├── contracts/             # Legacy contract versions
│   └── docs/                  # Phase reports & analysis
│
├── 📁 scripts/                # Operational scripts
│   ├── deploy/                # Deployment scripts
│   ├── operations/            # Balance checks, minting
│   ├── monitoring/            # Telemetry, economic, defense
│   ├── governance/            # Governance tools
│   └── testing/               # Test utilities
│
├── 📁 test/                   # Test suites
│   ├── unit/                  # Unit tests (core, invariant, integration)
│   ├── chaos/                 # Chaos engineering tests
│   └── stress/                # Load testing
│
├── 📁 docs/                   # Documentation hierarchy
│   ├── 01_PROTOCOL/           # Whitepapers, architecture
│   ├── 04_GOVERNANCE/         # Governance documentation
│   ├── 05_OPERATIONS/         # Security operations
│   ├── 06_MONITORING/         # Telemetry systems
│   ├── 07_API/                # SDK, CLI documentation
│   ├── 08_DEVELOPMENT/        # Contributing, quickstart
│   ├── architecture/          # Technical architecture
│   ├── governance/              # Governance model
│   ├── operations/              # Production operations
│   └── security/                # Security documentation
│
├── 📁 src/                    # SDK source
│   ├── sdk/                   # OrionSDK
│   └── tui/                   # Terminal UI
│
├── 📁 bin/                    # CLI entry points
│   ├── oak.js                 # Main CLI
│   └── oak-tui.js             # Terminal UI
│
└── 📄 CURRENT_SYSTEM_STATE.md # Production system reference
Documentation

Getting Started

CONTRIBUTOR_ONBOARDING.md — Complete contributor guide
CURRENT_SYSTEM_STATE.md — Production system reference
docs/08_DEVELOPMENT/DEVELOPER_QUICKSTART.md — Development setup
Architecture & Protocol

docs/architecture/PROTOCOL_ARCHITECTURE.md — Technical architecture
docs/01_PROTOCOL/ARCHITECTURE.md — System overview
docs/01_PROTOCOL/ORION_WHITE_PAPER.md — Whitepaper
Governance & Operations

docs/governance/GOVERNANCE_MODEL.md — Governance model
docs/04_GOVERNANCE/ORION_ECOSYSTEM_ROLES.md — Role definitions
docs/operations/PRODUCTION_OPERATIONS.md — Operations manual
docs/security/SIGNER_SECURITY_STANDARD.md — Signer security
API & Integration

docs/07_API/CLI_MANUAL.md — CLI documentation
src/sdk/index.js — SDK reference
Current System State

Operational Maturity: 94/100 — Production Excellence

Component	Status
Smart Contracts	✅ Audited & Hardened
Governance	✅ RBAC + Timelock + Safe Active
Monitoring	✅ Full Telemetry Operational
Security	✅ SOC Procedures Active
Mainnet Readiness	✅ 94/100 Score
Active Deployment:

Network: Polygon Amoy (testnet)
Mainnet: Ready for deployment
Monitoring: 24/7 operational
See CURRENT_SYSTEM_STATE.md for complete details.

Testing

# Run all tests
npm test

# Unit tests
npx hardhat test test/unit/**/*.test.ts

# Chaos tests
npx hardhat test test/chaos/*.test.ts

# Specific test
npx hardhat test test/unit/core/RBAC.test.ts
Test Coverage:

48+ tests across unit, chaos, and stress categories
RBAC governance validation
Economic metabolism verification
Temporal constraint testing
Emergency procedure validation
CLI Usage

# Main CLI
npm run oak -- --help
npm run oak -- status
npm run oak -- governance queue

# TUI Dashboard
npm run oak:tui
Governance

Current Model: Multi-layer governance with progressive decentralization

Layer 1: RBAC (Operational Roles)
  - PAUSER_ROLE: Emergency pause/unpause
  - CONFIG_ROLE: Sensor configuration
  - TREASURY_ROLE: Treasury management
  - FUND_ROLE: Liquidity injection
  
Layer 2: Timelock (24h delay)
  - All governance operations delayed
  - Cancelation possible during delay
  
Layer 3: Safe (2-of-3 multi-sig)
  - Hardware wallet secured
  - Geographically distributed
  - Emergency procedures tested
See docs/governance/GOVERNANCE_MODEL.md for complete details.

Security

Defense in Depth

Contract Layer: RBAC + Pausable + Reentrancy guards
Governance Layer: Multi-sig + Timelock + Role separation
Economic Layer: Stake requirements + Slashing
Operational Layer: SOC + Monitoring + Incident response
Audit History

Phase 2: RBAC Audit — 92/100
Phase 3.5: Staging Validation — 91/100
Phase 4: Production Audit — 94/100
See docs/security/ for security documentation.

Contributing

We welcome contributions from experienced smart contract developers, security researchers, and protocol engineers.

Read CONTRIBUTOR_ONBOARDING.md
Review docs/08_DEVELOPMENT/CONTRIBUTING.md
Follow security procedures in docs/security/
Security: For security issues, please follow responsible disclosure procedures.

License

MIT License — See LICENSE for details.

Resources

Website: [TBD]
Documentation: See docs/ directory
Discord: [TBD]
Twitter: [TBD]
OAK Protocol — Institutional-grade infrastructure for verified autonomous systems.

Repository Health Score: 94/100 ✅
Last Updated: 14 May 2026
