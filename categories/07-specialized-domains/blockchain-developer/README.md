# Blockchain Developer Agent

Expert blockchain developer specializing in smart contract development, DApp architecture, and DeFi protocols. Masters Solidity, Web3 integration, and blockchain security with focus on building secure, gas-efficient, and innovative decentralized applications.

## Overview

The Blockchain Developer agent is a senior-level blockchain development specialist with comprehensive expertise across the decentralized technology stack. From smart contract architecture to DApp deployment, this agent delivers production-ready blockchain solutions with emphasis on security, gas optimization, and innovation.

## Expertise Areas

### Smart Contract Development
- **Languages**: Solidity, Rust (Solana/Near), AssemblyScript
- **Frameworks**: Hardhat, Foundry, Truffle, Anchor
- **Standards**: ERC20, ERC721, ERC1155, ERC4626, EIP-2612
- **Patterns**: Proxy upgrades, Diamond pattern, Factory pattern

### DeFi Protocols
- Automated Market Makers (AMM)
- Lending and borrowing protocols
- Yield farming and aggregation
- Staking mechanisms
- Governance systems
- Flash loan implementations
- Liquidation engines
- Price oracle integration

### Security & Auditing
- Reentrancy prevention
- Access control mechanisms
- Integer overflow protection
- Front-running mitigation
- Flash loan attack prevention
- Oracle manipulation protection
- Security tool integration (Slither, Mythril, Echidna)

### Gas Optimization
- Storage packing and layout optimization
- Function optimization techniques
- Loop efficiency improvements
- Batch operations
- Assembly (Yul) for critical paths
- Proxy pattern selection
- Data compression strategies

### Multi-Chain Development
- Ethereum and EVM-compatible chains
- Solana (Rust, Anchor framework)
- Polkadot (Substrate)
- Cosmos SDK
- Near Protocol
- Avalanche subnets
- Layer 2 solutions (Optimism, Arbitrum, zkSync)

## Slash Commands

### `/smart-contract`
Generate a complete smart contract implementation based on your requirements.

**Example Usage**:
```
/smart-contract Create an ERC721 NFT contract with:
- Whitelist minting phase
- Public minting phase
- Royalty support (EIP-2981)
- Revealed metadata with IPFS
- Maximum supply of 10,000
```

**Output Includes**:
- Complete Solidity contract code
- Comprehensive test suite
- Deployment scripts
- Gas optimization analysis
- Security considerations documentation

### `/contract-audit`
Perform a comprehensive security audit of existing smart contracts.

**Example Usage**:
```
/contract-audit Audit the contracts in ./contracts/ directory focusing on:
- Reentrancy vulnerabilities
- Access control issues
- Gas optimization opportunities
- Best practice compliance
```

**Audit Report Includes**:
- Vulnerability assessment (Critical, High, Medium, Low)
- Gas optimization recommendations
- Best practice violations
- Code quality analysis
- Detailed fix recommendations

### `/deploy-contract`
Create deployment scripts and comprehensive deployment guides.

**Example Usage**:
```
/deploy-contract Create deployment for MyToken contract to:
- Ethereum mainnet
- Polygon
- Arbitrum
Include verification and multi-sig setup
```

**Deliverables**:
- Multi-network deployment scripts
- Environment configuration templates
- Contract verification commands
- Post-deployment validation tests
- Deployment checklist

### `/gas-optimize`
Analyze smart contracts and implement gas optimization strategies.

**Example Usage**:
```
/gas-optimize Optimize the DEX contract focusing on:
- Swap function efficiency
- Storage layout optimization
- Batch operation improvements
```

**Optimization Report**:
- Current gas usage baseline
- Optimization recommendations with impact estimates
- Implemented optimizations
- Before/after comparison
- Trade-off analysis

## Use Cases

### 1. DeFi Protocol Development
Build a complete DeFi protocol from scratch:
- Design tokenomics and protocol mechanics
- Implement core smart contracts (pools, vaults, governance)
- Integrate price oracles (Chainlink, Uniswap TWAP)
- Build comprehensive testing suite with mainnet forking
- Conduct security audit and implement fixes
- Deploy with multi-sig governance
- Set up monitoring and alerting

### 2. NFT Project Launch
Launch a production-ready NFT collection:
- Design NFT contract with custom features
- Implement minting mechanisms (whitelist, public, dutch auction)
- Set up IPFS metadata and artwork storage
- Integrate marketplace compatibility (OpenSea, Rarible)
- Build minting website with Web3 integration
- Deploy and verify contracts
- Monitor minting activity and marketplace listings

### 3. Cross-Chain Bridge
Develop a secure cross-chain bridge:
- Design bridge architecture and security model
- Implement lock-and-mint mechanism
- Integrate with message passing protocol (LayerZero, Wormhole)
- Build relayer infrastructure
- Comprehensive security testing
- Deploy across multiple chains
- Set up monitoring and emergency pause mechanisms

### 4. Smart Contract Audit & Optimization
Audit and optimize existing contracts:
- Comprehensive security analysis
- Identify vulnerabilities and attack vectors
- Gas optimization analysis
- Implement recommended fixes
- Retest and validate improvements
- Document security posture

## MCP Servers

### Filesystem
Access and modify local files for contract development, testing, and deployment scripts.

### GitHub
- Version control integration
- Pull request reviews
- Issue tracking for audit findings
- Repository management

### Context7
- Access up-to-date blockchain library documentation
- Solidity language references
- Framework documentation (Hardhat, Foundry)
- Security best practices

### Memory
- Store blockchain project context
- Track development progress
- Remember security considerations
- Maintain deployment configurations

## Integration with Other Agents

### Security Auditor
Collaborate on comprehensive security audits, vulnerability assessments, and penetration testing of smart contracts.

### Frontend Developer
Support Web3 integration, wallet connections (MetaMask, WalletConnect), and transaction handling in frontend applications.

### Backend Developer
Work together on blockchain indexing (The Graph), event monitoring, and off-chain data synchronization.

### DevOps Engineer
Guide on deployment infrastructure, node setup, monitoring solutions, and CI/CD for smart contract testing.

### QA Expert
Assist with testing strategies including fuzzing, invariant testing, fork testing, and gas profiling.

### Architect Reviewer
Collaborate on system design, contract architecture, upgrade patterns, and scalability solutions.

### Fintech Engineer
Partner on DeFi implementations, tokenomics design, financial protocol mechanics, and regulatory compliance.

### Legal Advisor
Coordinate on regulatory compliance, token classification, and smart contract legal considerations.

## Development Workflow

### 1. Architecture Phase
- Gather requirements and constraints
- Design contract architecture
- Plan security measures
- Estimate gas costs
- Define upgrade strategy
- Document architectural decisions

### 2. Implementation Phase
- Write smart contracts following best practices
- Implement comprehensive test suite
- Optimize gas usage
- Run security analysis tools
- Write detailed documentation
- Create deployment scripts

### 3. Testing Phase
- Unit tests (100% coverage target)
- Integration tests
- Fork tests against mainnet
- Fuzzing tests (Echidna, Foundry)
- Invariant tests
- Gas profiling

### 4. Audit Phase
- Internal security review
- Run automated analysis (Slither, Mythril)
- External audit (if required)
- Implement audit findings
- Retest and verify fixes

### 5. Deployment Phase
- Deploy to testnet (Goerli, Sepolia)
- Verify contracts on Etherscan
- Test on testnet
- Deploy to mainnet
- Set up monitoring
- Transfer ownership to multi-sig

### 6. Maintenance Phase
- Monitor contract activity
- Respond to incidents
- Plan and execute upgrades
- Optimize based on usage patterns

## Best Practices

### Security First
- Every contract assumes adversarial environment
- Defense in depth approach
- Fail-safe defaults
- Emergency pause mechanisms
- Multi-sig for critical operations

### Testing Excellence
- 100% code coverage minimum
- Test both success and failure cases
- Edge case testing
- Fuzzing for unexpected inputs
- Fork testing for complex integrations

### Gas Optimization
- Optimize for common operations
- Use events instead of storage where possible
- Pack storage variables
- Use libraries for common code
- Consider L2 deployment for gas-intensive apps

### Documentation
- NatSpec comments for all public functions
- Architecture decision records
- Deployment guides
- Emergency procedures
- User guides for contract interaction

## Getting Started

1. **Initialize your blockchain project**
   ```
   I need to build a DeFi lending protocol on Ethereum
   ```

2. **Get architecture review**
   ```
   Review the architecture of my smart contracts in ./contracts/
   ```

3. **Generate smart contract**
   ```
   /smart-contract Create a staking contract with:
   - ERC20 reward tokens
   - Lock periods (30, 90, 180 days)
   - Early withdrawal penalties
   - Emergency withdraw function
   ```

4. **Audit existing contracts**
   ```
   /contract-audit Perform security audit on MyDeFiProtocol.sol
   ```

5. **Optimize for gas**
   ```
   /gas-optimize Reduce gas costs for the swap function in DEX.sol
   ```

6. **Deploy to production**
   ```
   /deploy-contract Deploy MyProtocol to Ethereum mainnet and Polygon
   ```

## Quality Checklist

Every blockchain project delivered meets these standards:

- ✅ 100% test coverage achieved
- ✅ Gas optimization applied thoroughly
- ✅ Security audit passed completely
- ✅ Slither/Mythril clean verified
- ✅ Documentation complete accurately
- ✅ Upgradeable patterns implemented (if required)
- ✅ Emergency stops included properly
- ✅ Standards compliance ensured (ERC, EIP)

## Example Projects

### DeFi Yield Vault
A complete ERC4626-compliant yield vault with automated strategy execution, gas-optimized operations, and comprehensive security measures.

### NFT Marketplace
A secure NFT marketplace supporting ERC721 and ERC1155 with royalty enforcement, escrow system, and gas-efficient batch operations.

### Governance DAO
A decentralized autonomous organization with token-weighted voting, proposal execution, timelock mechanisms, and multi-sig security.

### Cross-Chain Token Bridge
A secure bridge for transferring tokens between Ethereum and Polygon using lock-and-mint mechanism with validator network.

## Resources

### Security Tools
- Slither: Static analysis
- Mythril: Symbolic execution
- Echidna: Fuzzing
- Manticore: Symbolic execution
- Certora: Formal verification

### Development Tools
- Hardhat: Development environment
- Foundry: Testing framework
- Remix: Online IDE
- OpenZeppelin: Contract libraries
- Tenderly: Monitoring and debugging

### Testing Networks
- Goerli: Ethereum testnet
- Sepolia: Ethereum testnet
- Mumbai: Polygon testnet
- Fuji: Avalanche testnet

## Support

For optimal results:
- Provide clear requirements and constraints
- Share existing contract code for audits
- Specify target blockchain networks
- Define security and gas budget priorities
- Include compliance requirements

The Blockchain Developer agent is designed to deliver production-ready, secure, and efficient blockchain solutions that push the boundaries of decentralized technology.
