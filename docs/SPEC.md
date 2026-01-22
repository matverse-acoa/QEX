# QEX Security & Governance Specification (Official)

## Scope
This specification formalizes QEX as a **hybrid quantum-classical-algebraic framework** for antifragile security and governance. It defines the normative decision model, evidence requirements, post-quantum trust primitives, and FailQuantum thermodynamic cost integration.

## 1. Normative Decision Kernel (PBSE)
All actions are mediated by a governance kernel that evaluates admissibility:

```
Decision(action) ∈ {ALLOW, BLOCK, SILENCE, ESCALATE}
```

**Default**: Fail-closed. Actions without complete evidence or metrics are rejected or escalated.

## 2. Evidence & Ledger Requirements
Every critical action produces a receipt with the following properties:

- Deterministic hash of decision inputs.
- Merkle root linkage to the event chain.
- Timestamped record stored append-only.
- Optional post-quantum signatures for long-term integrity.

**Property**:

```
Action ⇒ Evidence ⇒ Verifiability
```

## 3. Metrics & Decision Scoring
Decision admissibility uses multi-objective metrics combining coherence, latency, risk, and cost.

- **Ψ (Coherence Index)**: completeness, consistency, traceability.
- **Θ (Latency Index)**: operational latency budget.
- **CVaR (Tail Risk)**: extreme-risk sensitivity.
- **FailQuantum Cost (FQ)**: thermodynamic penalty for state transitions.

A generic admissibility score:

```
Score = f(Ψ, Θ, CVaR, FQ)
```

Decision thresholds are policy-defined and must be auditable.

## 4. Post-Quantum Trust (PQC)
QEX integrates post-quantum primitives for long-term integrity:

- **KEM**: ML-KEM / Kyber class algorithms.
- **Signatures**: ML-DSA / Dilithium class algorithms.

Receipts and ledger entries can be PQC-signed to resist quantum adversaries and harvest-now/decrypt-later attacks.

## 5. FailQuantum Algebra (Thermodynamic Cost)
FailQuantum models failure aggregation and energetic irreversibility.

**State model**:

```
F = E − T·S
```

**Cost of composition**:

```
ΔF = F(a ⨂ b) − (F(a) + F(b))
```

Where:

- `E` = energy
- `S` = entropy
- `T` = effective temperature

This penalty is incorporated into decision scoring to prevent entropic escalation and enforce energy-aware governance.

## 6. Temporal Security Model
QEX treats security as a three-timeframe discipline:

- **Past**: forensic audit and replay.
- **Present**: live validation and enforcement.
- **Future**: adversarial simulation and risk forecasting.

```
Threat(t) = PastEvidence + LiveSignals + PredictedRisk
```

## 7. Antifragility Guarantees
QEX governance is designed to improve under stress by:

- Preferring provable actions over heuristic actions.
- Penalizing thermodynamically costly transitions.
- Recording all failures for iterative hardening.

## 8. Compliance and Auditability
All security and governance decisions are required to be:

- Deterministic.
- Reproducible.
- Independently verifiable.
- Signed and hash-linked for tamper evidence.
