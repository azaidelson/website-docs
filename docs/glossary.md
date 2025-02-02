---
title: Glossary
slug: /reference/glossary
---

### Glossary
### `Eigenlayer`
An Ethereum-based protocol that enables restaking

### `AVS`
Actively Validated Service ~ the term for a service on Eigenlayer

### `Restaking`
Where people reuse collateral to operate ≥ 1 AVS. If this collateral is beacon chain ETH, they are a called a `native restaker`

### `LSP`
Liquid Staking Protocol

### `nLRP`
Native Liquid Restaking Protocol. The Puffer protocol offers native ETH liquid restaking on Eigenlayer

### `pufETH`
The yield bearing token that represents staked ETH in Puffer’s LSP

### `Stakers`
The users who “stake” ETH to the pool to receive pufETH

### `NoOps`
The Puffer nodes that operate an Ethereum validator (and optionally additional AVSs)

### `Guardians`
A committee of Ethereum aligned community members and organizations to assist the protocol as it matures

### `Enclave`
A secure-computing environment capable of running Puffer’s anti-slashing technology

### `Burst Threshold`
Code in our smart contracts that self-caps the pool at 22% marketshare

### `Beacon Chain`
The main component of the Ethereum blockchain responsible for Proof of Stake consensus

### `Beacon Chain Deposit Contract`
The smart contract to which a NoOp must deposit 32 ETH to initiate running a validator node

### `VEM`
Voluntary Exit Message ~ a validator-signed message that will exit the signer when broadcasted to the beacon chain

### `Withdrawal Credentials`
A validator parameter that sets where their consensus rewards and full withdrawal eth are sent. For 0x01 (post-Shapella) withdrawals, the credentials are formatted as `0x01000000000000` ++ `20 byte ethereum address`

### `Consensus Rewards`
AKA partial withdrawals or skimmed rewards. These rewards are generated by Ethereum validators performing their PoS duties

### `Execution Rewards`
The rewards earned by a validator when proposing a block. The rewards are composed of priority fees and MEV: Maximal Extractable Value". This refers to the maximum value that can be extracted from block production in excess of the standard block reward and gas fees by including, excluding, and changing the order of transactions in a block. [source](https://ethereum.org/en/developers/docs/mev/)

### `Full Withdrawal`
The validator’s entire balance that is withdrawn from the beacon chain to the Ethereum address set by the withdrawal credentials

### `Slashing`
Slashing may refer to a loss of funds triggered by either of the following:
1. Misbehavior of validator nodes, such as signing two different blocks for the same beacon slot (AKA double-signing). See [secure-signer](technology/secure-signer) for more info on this kind of slashing
2. A Restaking Operator (ReOp) not fulfilling obligations defined by an AVS

### `Validator Ticket`
An ERC20 token. Each Validator Ticket allows operating a validator on the Puffer Protocol for one day.  


### `Bond`
An amount of pufETH a NoOp must lend to the protocol during the time of running their validator node. They may lose some or all of this bond if they misbehave or are slashed. NoOps may retrieve this bond after proving they have exited their validator node from the beacon chain

### `Puffer Module`
A contract which defines a set of AVSs which NoOps opting into the module will delegate their ETH funds to running. These NoOps will receive corresponding rewards in return by participating in this Puffer Module

### `Restaking Operator`
AKA ReOp: A NoOp that is delegated funds to operate an AVS on behalf of other NoOps, as part of a Puffer Module

### `Secure Signer`
A software developed by Puffer that helps prevent validators from being slashed. It utilizes Trusted Execution Environments (TEEs) such as Intel SGX

### `Proof of Reserves`
This refers to the process by which the protocol proves the amount of ETH backing pufETH, and thus determining the fair exchange ratio between ETH and pufETH

### `Proof of Rewards`
This refers to the process by which NoOps prove and receive the rewards generated as a result of running their validator node