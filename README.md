# FundMe Smart Contract

A decentralized funding contract that allows users to send ETH while ensuring a minimum USD value, Built with Foundry.

## Contract Details
- **[Etherscan verified contract here](https://sepolia.etherscan.io/address/0x041a65179a37801967cb36049ace4bdd760f06b9#code)**
- Uses Chainlink Price Feeds for accurate ETH/USD conversion
- Implements withdrawal pattern
- Gas-optimized operations
- Comprehensive test suite

## Core Features

- **Funding**: Users can send ETH (minimum $5 USD equivalent)
- **Price Feed Integration**: Real-time ETH/USD conversion via Chainlink
- **Withdrawal**: Only owner can withdraw accumulated funds
- **Gas Optimized**: Implements gas-efficient withdrawal patterns
- **Security**: Owner-only functions, secure fund management

## Built With

- [Foundry](https://book.getfoundry.sh/) - Development framework
- [Chainlink](https://chain.link/) - Price Feed Oracle

## 🚀 Getting Started

### Prerequisites

* [foundry](https://book.getfoundry.sh/getting-started/installation)

### Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/foundry-fund-me
cd foundry-fund-me
```

2. Install dependencies:
```bash
forge install
```

3. Build the project:
```bash
forge build
```

### Running Tests

```bash
# Run all tests
forge test

# Run tests with gas report
forge test --gas-report

# Run a specific test
forge test --match-test testFunctionName

# Run tests with verbosity
forge test -vv
```

## Usage

### Deploy

1. Setup environment variables:
```bash
cp .env.example .env
# Add your RPC_URL and PRIVATE_KEY to .env
```

2. Deploy:
```bash
forge script script/DeployFundMe.s.sol --rpc-url $RPC_URL --private-key $PRIVATE_KEY --broadcast
```

### Interact with Contract

Fund the contract:
```bash
forge script script/Interactions.s.sol:FundFundMe --rpc-url $RPC_URL --private-key $PRIVATE_KEY --broadcast
```

Withdraw funds (only owner):
```bash
forge script script/Interactions.s.sol:WithdrawFundMe --rpc-url $RPC_URL --private-key $PRIVATE_KEY --broadcast
```

## Testing

The project includes:
- Unit tests
- Integration tests
- Forked network tests

### Test Coverage

```bash
forge coverage
```

