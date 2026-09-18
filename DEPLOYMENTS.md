# Arc mainnet deployment evidence

All addresses below are public deployment references. Verify current state on the linked explorer before relying on them.

| Component | Address | Explorer |
|---|---|---|
| StonkRobotics evaluation/mint contract | `0x6a3B12532F8e562f99e3292380e7f69D32e10B32` | https://explorer.arc.io/address/0x6a3B12532F8e562f99e3292380e7f69D32e10B32 |
| ARCROBO token | `0x90554cEaf18BD5545F4be6520a3077D327727297` | https://explorer.arc.io/address/0x90554cEaf18BD5545F4be6520a3077D327727297 |
| ARCROBO / USDC pool | `0xd3e373b283a28407d40fc2791d759a4bb75c25d277f3bcf9863fc6a2af2afe35` | https://explorer.arc.io/address/0xd3e373b283a28407d40fc2791d759a4bb75c25d277f3bcf9863fc6a2af2afe35 |

## Network

- Network: Arc mainnet
- Chain ID: `5042`
- RPC: https://rpc.mainnet.arc.io
- Native USDC address used by the project: `0x3600000000000000000000000000000000000000`

## Contract role

The StonkRobotics contract is an ERC-721 deployment with a Proof-of-Intelligence path. A backend signer issues an EIP-712 voucher after an agent evaluation. The contract checks the voucher fields and records the evaluation score for the minted unit. Voucher nonces are single-use and deadlines are enforced on-chain.

## Token role

ARCROBO is a separate fixed-supply token deployed on Arc and paired with USDC. It is supporting Arc deployment evidence, not a prerequisite for the agent challenge or evaluation workflow. The current token page describes it as an independent project token and does not claim Arc or Circle endorsement.

## Verification note

This file records addresses already used by the live project; it does not represent a new deployment in this repository. No new contract or token is being deployed for this reference repository.
