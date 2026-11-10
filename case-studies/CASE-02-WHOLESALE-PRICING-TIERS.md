# CASE-02: Wholesale pricing without reducing supplier obligations

Evidence strength is identified in each section. No exact historical prompt, bank reconciliation or dispatch is invented.

## Business problem

A mixed order qualifies for wholesale pricing only at 20 combined Medium and Premium packs. The reseller must absorb the discount.

## Historical input

The native ledger records 10 Medium + 10 Premium. Any inquiry or sample invoice text here is a reconstruction from that row, not a retained historical chat.

## AI task and retained output

The supported calculation applies Medium Rp13.000 and Premium Rp23.000, while supplier costs remain Rp10.000 and Rp20.000. A sample prompt illustrates this delegation; the ledger alone does not prove every intermediate AI action.

## Human judgment

The review criterion is both threshold and supplier floor: 20 combined packs qualify, customer sales are Rp360.000, supplier obligation is Rp300.000, product margin is Rp60.000.

## Supported outcome

Payment time is recorded as 25 August 2026, 20:34:48 WIB; closing is 28 August 2026, 21:58:30 WIB, TB-003. These are different lifecycle events. Shipping Rp18.000 is recorded COD to courier.

## Verification limits

This is a ledger-supported pricing episode, with no public original inquiry, dispatched invoice, stock audit or independent bank reconciliation.

## Financial check

| Component | Value |
|---|---:|
| Product sales | Rp360.000 |
| Supplier product cost | Rp300.000 |
| Product margin | Rp60.000 |
| Shipping information | Rp18.000 |

Product margin = sales minus supplier product cost. Shipping, donations and tips are separate flows.

10x13.000+10x23.000=360.000; supplier 10x10.000+10x20.000=300.000; margin20x3.000=60.000. Normal retail400.000 minus wholesale360.000=40.000 discount absorbed by reseller.

### Reconstruction for illustration only

> Check combined quantity first. Apply wholesale only from 20 regular packs. Protect the supplier floor.

This is a current explanatory instruction, not a recovered verbatim historical prompt or dispatched invoice.

## Sources and lessons

Supplier A Transaksi row 27; Log business rules section 2.

[Catalog](../evidence/evidence_catalog.md) | [Anonymized ledger extracts](../evidence/verified_ledger_extracts.json) | [README](../README.md)

Private source locators are not public links. Screenshot captures are fromOctober; transactions are fromAugust-September 2026. Compare facts, calculations and lifecycle states before declaring completion. A required control is not proof that every run complied.
