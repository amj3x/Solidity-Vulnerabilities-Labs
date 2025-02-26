# Solidity Smart Contract Vulnerablities Labs
This repository contains some labs and their solutions demonstrating various smart contract vulnerabilities found in the real DeFi world. Each lab provides a hands-on challenge to understand and exploit one (somtimes more) security flaw in Solidity-based contracts. 

## What’s Inside?
- **Reentrancy Attacks**.

- **Unbounded Gas Consumption**.

- **Storage Collision in Proxies**.

- **Vault Inflation Attacks** - Ispired by EIP-4626, with a twist.

- **Unsafe Downcasting** - The Integer Overflow of the newer versions of Solidity.
  
- And more...

## Labs Structure
```
├── src/
│   ├── VulnName1/
│   │    ├── Target.sol     # The contract with the vulnerable code
│   │    ├── Exploit.sol    # If Applicable, Sometimes we won't need this file     
│   ├── VulnName2/        
│   .
|   .
│
├── test/   
│   ├── VulnName1/
│   │    ├── Target.t.sol   # These are not part of the lab, just tests to make sure the contract is working as intended
│   │    ├── Exploit.t.sol  # This is where our exploit happens, we simulate the exploitation by running tests
│   ├── VulnName2/  
│   .
│   .
│    
├── script/                 # These are not part of the lab, we will just use scripts sometimes to help with simulating deployment
│
```

## How to Use
***Prerequesties*** : Make Sure you have foundry installed.



1. Clone the repository: 
  ```bash
  git clone https://github.com/amj3x/Solidity-Vulnerabilities-Labs.git
  cd Solidity-Vulnerabilities-Labs
  ```
2. Install dependencies: 
  ```bash
  forge install
  ```
3. To run a solution; let's take reentrancy as an example, run the following command:
  ```bash
  $ forge test --mt testReentrancyAttack -vvv    
  [⠊] Compiling...
  No files changed, compilation skipped

  Ran 1 test for test/Reentrancy/ExploitReentrancy.t.sol:ExploitReentrancyTest
  [PASS] testReentrancyAttack() (gas: 681040)
  Logs:
    Attacker balance before attack:  1000000000000000000
    Attacker balance after attack:   2000000000000000000
  ```

***Happy Hacking!!***
 
