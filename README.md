# zkSync Era audit details
- $1,100,000 total maximum award pot, including **$##,###** gas optimizations pot
- Join [C4 Discord](https://discord.gg/code4rena) to register
- Submit findings [using the C4 form](https://code4rena.com/contests/2023-10-zksync/submit)
- [Read our guidelines for more details](https://docs.code4rena.com/roles/wardens)
- Starts October 2, 2023 20:00 UTC 
- Ends October 20:00 UTC 

How the &#36;1,100,000 maximum pot works:
- Contest minimum pot is &#36;330,000 (including **&#36;##k** gas optimization pot).
- If ANY valid medium severity issue is found, contest pot increases to &#36;770,000.
- If ANY valid high severity issue is found, contest pot increases to &#36;1,100,000.

## Automated Findings / Publicly Known Issues

Automated findings output for the audit can be found [here](https://github.com/code-423n4/2023-10-zksync/bot-report.md) within 24 hours of audit opening.

*Note for C4 wardens: Anything included in the automated findings output is considered a publicly known issue and is ineligible for awards.*


# Overview

# **zkSync Protocol Overview & Documentation**

zkSync Era is a fully-fledged Layer-2 scaling solution, combining a set of smart contracts on Ethereum mainnet and zkEVM for enabling Ethereum virtual machine-compatible smart contract execution.

This repository contains comprehensive documentation and code related to the Smart Contracts, VM, and zk-circuits sections of the zkSync Era Protocol. Below is a high-level summary of each section along with relevant documentation links. Please refer to these before and during the audit for a thorough understanding of the protocol.

## **📁 Sections**

### **1. Smart Contracts Section**

Relevant Documentation:

- **[System Contracts/Bootloader Description](https://github.com/code-423n4/2023-10-zksync/blob/main/docs/Smart%20contract%20Section/System%20contracts%20bootloader%20description%20(VM%20v1%204%200).md)**
- **[zkSync Era Fee Model](https://github.com/code-423n4/2023-10-zksync/blob/main/docs/Smart%20contract%20Section/zkSync%20fee%20model.md)**
- **[Handling L1→L2 Ops on zkSync](https://github.com/code-423n4/2023-10-zksync/blob/main/docs/Smart%20contract%20Section/Handling%20L1%E2%86%92L2%20ops%20on%20zkSync.md)**
- **[Batches & L2 Blocks on zkSync](https://github.com/code-423n4/2023-10-zksync/blob/main/docs/Smart%20contract%20Section/Batches%20%26%20L2%20blocks%20on%20zkSync.md)**
- **[Elliptic Curve Precompiles](https://github.com/code-423n4/2023-10-zksync/blob/main/docs/Smart%20contract%20Section/Elliptic%20curve%20precompiles.md)**
- **[Handling Pubdata in Boojum](https://www.notion.so/Handling-pubdata-in-Boojum-07dd1bd2ec9041faab21898acd24334e?pvs=21)**

### **2. VM Section**

The VM section is related to the zkSync Era Virtual Machine.

- **[ZkSync Era Virtual Machine Primer](https://github.com/code-423n4/2023-10-zksync/blob/main/docs/VM%20Section/ZkSync%20Era%20Virtual%20Machine%20primer.md)**
    - This primer is designed to provide auditors with a foundational understanding of the zkSync Era Virtual Machine. It offers insights into the operational mechanics and integral components of EraVM, serving as an essential guide for those seeking to explore the zkSync EraVM environment.
- **[zkSync Era: The Equivalence Compiler Documentation](https://github.com/code-423n4/2023-10-zksync/blob/main/docs/VM%20Section/compiler-equivalence-docs/zkSync%20Era%20-%20The%20Equivalence%20Compiler%20Documentation.md)**
    - The document describes how zkSync Solidity compiler represents high-level programming language constructions into low-level EraVM instruction set, how to use unique features without extending Solidity language with new syntax and why system contracts are needed.
- **[EraVM Formal specification](https://github.com/code-423n4/2023-10-zksync/blob/main/docs/VM%20Section/spec.pdf)**
    - This document is a highly technical and detailed specification, providing an in-depth exploration of the zkSync protocol and its underlying architecture. It’s a comprehensive resource for those who desire a deeper and more formal understanding of the protocol's design and functionalities. While it’s not a required read for understanding the basic structure and operations of the protocol, it is an invaluable resource for those wishing to delve into the finer details and theoretical underpinnings of zkSync.

### **3. Circuits Section**

Circuit Documentation:

- **How does ZK work? (high level)**
   - [Intro to zkSync’s ZK](https://github.com/code-423n4/2023-10-zksync/blob/main/docs/Circuits%20Section/Intro%20to%20zkSync%E2%80%99s%20ZK.md)
   - [ZK Terminology](https://github.com/code-423n4/2023-10-zksync/blob/main/docs/Circuits%20Section/ZK%20Terminology.md)
   - [Getting Started](https://github.com/code-423n4/2023-10-zksync/blob/main/docs/Circuits%20Section/Getting%20Started.md)
- **Examples and Tests**
   - [Circuit Testing](https://github.com/code-423n4/2023-10-zksync/blob/main/docs/Circuits%20Section/Circuit%20testing.md)
- **Advanced**
   - [Boojum gadgets](https://github.com/code-423n4/2023-10-zksync/blob/main/docs/Circuits%20Section/Boojum%20gadgets.md)
   - [Circuits](https://www.notion.so/Circuits-c2e39db21b4446aa8f06318ae404d34f?pvs=21)
   - [Boojum function: check_if_satisfied](https://github.com/code-423n4/2023-10-zksync/blob/sampkaML/Circuits%20Section/Boojum%20function%20check_if_satisfied.md)

## **🚨 Audit & Code Freeze**

Be advised that a code freeze will be in effect for the duration of the audit to ensure a level playing field. All participants are required to review and adhere to the final versions of contracts and documentation added in this repository at least 48 business hours prior to the audit start time.

## **🚀 Getting Started for Auditors**

- Ensure to go through each section and related documents thoroughly.
- Keep in mind the overall working of the zkSync protocol while reviewing individual components.
- Review the code and documentation with a focus on security, correctness, and optimization, particularly concerning gas consumption.

## **📢 Communication**

For any clarifications, doubts, or discussion, please contact Code4rena staff, and we will address your concerns promptly.

## Links

- **Documentation:** https://era.zksync.io/docs/
- **Website:** https://zksync.io/
- **Twitter:** https://twitter.com/zksync
- **Discord:** https://join.zksync.dev/


# Scope

[ ⭐️ SPONSORS: add scoping and technical details here ]

- [ ] In the table format shown below, provide the name of each contract and:
  - [ ] source lines of code (excluding blank lines and comments) in each *For line of code counts, we recommend running prettier with a 100-character line length, and using [cloc](https://github.com/AlDanial/cloc).* 
  - [ ] external contracts called in each
  - [ ] libraries used in each

*List all files in scope in the table below (along with hyperlinks) -- and feel free to add notes here to emphasize areas of focus.*

| Contract | SLOC | Purpose | Libraries used |  
| ----------- | ----------- | ----------- | ----------- |
| [contracts/folder/sample.sol](contracts/folder/sample.sol) | 123 | This contract does XYZ | [`@openzeppelin/*`](https://openzeppelin.com/contracts/) |

| Contract | SLOC | Purpose | Libraries used |  
| ----------- | ----------- | ----------- | ----------- |
| [era-zkevm_circuits/src/base_structures](era-zkevm_circuits/src/base_structures) | 1971 | Structures for circuits | |
| [era-zkevm_circuits/src/code_unpacker_sha256](era-zkevm_circuits/src/code_unpacker_sha256) | 704 | Unpacks code into memory | |
| [era-zkevm_circuits/src/demux_log_queue](era-zkevm_circuits/src/demux_log_queue) | 868 | Demultiplexes logs into their appropriate circuits | |
| [era-zkevm_circuits/src/ecrecover](era-zkevm_circuits/src/ecrecover) | 1342 | Ecrecover precompile | |
| [era-zkevm_circuits/src/fsm_input_output](era-zkevm_circuits/src/fsm_input_output) | 352 | Validates the outputs of one circuit match the inputs of the next | |
| [era-zkevm_circuits/src/keccak_round_function](era-zkevm_circuits/src/keccak_round_function) | 531 | Keccak hash function | |
| [era-zkevm_circuits/src/linear_hasher](era-zkevm_circuits/src/linear_hasher) | 224 | Creates commitment using Keccak | |
| [era-zkevm_circuits/src/log_sorter](era-zkevm_circuits/src/log_sorter) | 798 | Sorts logs by timestamp | |
| [era-zkevm_circuits/src/main_vm](era-zkevm_circuits/src/main_vm) | 7673 | Main VM circuit | |
| [era-zkevm_circuits/src/ram_permutation](era-zkevm_circuits/src/ram_permutation) | 657 | Circuit for RAM reads+writes | |
| [era-zkevm_circuits/src/sort_decommitment_requests](era-zkevm_circuits/src/sort_decommitment_requests) | 1358 | Sort code decommitments | |
| [era-zkevm_circuits/src/storage_application](era-zkevm_circuits/src/storage_application) | 686 | Circuit related to storage | |
| [era-zkevm_circuits/src/storage_validity_by_grand_product](era-zkevm_circuits/src/storage_validity_by_grand_product) | 1670 | Sort storage access | |
| [era-zkevm_circuits/src/tables](era-zkevm_circuits/src/tables) | 206 | Lookup Tables | |

## Out of scope

*List any files/contracts that are out of scope for this audit.*

- era-zkevm_circuits/src/recursion
- era-zkevm_circuits/src/scheduler

## Attack ideas (Where to look for bugs)
*List specific areas to address - see [this blog post](https://medium.com/code4rena/the-security-council-elections-within-the-arbitrum-dao-a-comprehensive-guide-aa6d001aae60#9adb) for an example*


## Scoping Details 
[ ⭐️ SPONSORS: please confirm/edit the information below. ]

```
- If you have a public code repo, please share it here:  N/A
- How many contracts are in scope?:   TODO
- Total SLoC for these contracts?:  TODO
- How many external imports are there?:  TODO
- How many separate interfaces and struct definitions are there for the contracts within scope?:  TODO
- Does most of your code generally use composition or inheritance?:   Yes
- How many external calls?:   TODO
- What is the overall line coverage percentage provided by your tests?: TODO
- Is this an upgrade of an existing system?: Yes
- Check all that apply (e.g. timelock, NFT, AMM, ERC20, rollups, etc.): timelock, rollups, zk circuits
- Is there a need to understand a separate part of the codebase / get context in order to audit this part of the protocol?:   No
- Please describe required context:   ZK rollup
- Does it use an oracle?:  No
- Describe any novel or unique curve logic or mathematical models your code uses: No
- Is this either a fork of or an alternate implementation of another project?: No
- Does it use a side-chain?: No
- Describe any specific areas you would like addressed: Missing constraints, logical errors, malicious input for zk circuit or bootloader
```

# Tests

*Provide every step required to build the project from a fresh git clone, as well as steps to run the tests with a gas report.* 

*Note: Many wardens run Slither as a first pass for testing.  Please document any known errors with no workaround.* 
