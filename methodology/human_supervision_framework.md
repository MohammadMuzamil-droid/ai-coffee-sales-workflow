# Human supervision and evidence strength

## Consistent gate map

These are documented controls, not a claim that every historical transaction passed all gates.

| Gate | Control | Demonstration and limit |
|---|---|---|
|1 Commercial/invoice|Check quantities, price threshold, supplier floor and required fields.|CASE-01/02 arithmetic; stock/dispatch not independently documented.|
|2 Shipping|Source-grounded tariff and payment method; no unsupported estimate.|27.200 physical receipt; correct lifecycle/COD treatment.|
|3 Output QA|Compare extracted figures and recompute item totals.|Two wrong readings and human correction; Sastra current audit arithmetic with uncertain original actor.|
|4 Closing|Eligibility, separate flows, read-back and reconciliation.|TB-001 source conflict remains;205.800 is ledger-derived.|

## Evidence labels

Original historical evidence is retained screenshot/receipt content, with redaction/crop disclosed. Ledger-supported observations are recorded values/status/notes, not automatically bank events. Derived calculations have inputs/formulas. Owner reports are attributed without inventing receipts. Reconstructions are new illustrations, not verbatim recovered prompts. Interpretations remain distinct from established causes. Missing external evidence means not independently verified.

## Reasoning shown

CASE-03 corrects an AI reading against the printed receipt and holds uncertain payment matching. CASE-04 checks supplier cost per item instead of accepting an aggregate. CASE-05 compares row-level math with a contradictory report without changing originals.

No experiment establishes the technical cause of reading errors or detection via parcel weight. No speedup, benchmark, accuracy rate or universal control-compliance claim is made.

## Completion boundary

WRITE -> READ-BACK -> RECONCILIATION is source SOP. On partial failure/mismatch: STOP / PERLU REKONSILIASI. A design rule is not a receipt of each write. Bank/courier execution remains human controlled. No independent bank/physical stock verification is claimed.

[Workflow](../architecture/workflow_pipeline.md) | [README](../README.md)
