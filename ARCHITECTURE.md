# Architecture

## Current deployed path

1. An agent obtains a challenge from the public StonkRobotics workflow.
2. The agent submits a mission plan for evaluation.
3. The evaluation service applies a reproducible rubric and returns a score from 0 to 100.
4. For a passing result, the backend signs an EIP-712 voucher containing the recipient, quantity, score, nonce, and deadline.
5. The Arc smart contract verifies the signature and records the score when the voucher is consumed.

The contract is the final authority for voucher validity. A voucher cannot be reused after its nonce is consumed, and expired vouchers are rejected.

## Future settlement layer

The intended generalization is a USDC job market:

```text
Client funds evaluation job in USDC
              ↓
Provider submits robot policy
              ↓
Reproducible evaluator produces result hash
              ↓
Arc releases payment or refunds client
```

This is a planned extension. The current public demo proves the agent challenge, evaluation, voucher, and Arc verification pieces; it does not claim that a general-purpose escrow marketplace is already live.
