# CASE-01: Order to invoice: preserving the original billing state

Evidence strength is identified in each section. No exact historical prompt, bank reconciliation or dispatch is invented.

## Business problem

An informal order needed an itemized bill, a separate supplier allocation, and an explicit shipping payment method.

## Historical input

The historical invoice card records 2 Medium + 2 Premium. The original WhatsApp inquiry is not retained in the public package.

## AI task and retained output

ChatGPT generated the itemized card visible in EVD-03. It shows product subtotal Rp80.000, shipping Rp12.800 and TOTAL BAYAR Rp92.800.

## Human judgment

My workflow requires checking quantities, pricing and shipping method before use. The retained evidence proves the invoice output and ledger values; it does not prove physical stock inspection or that this exact card was dispatched.

## Supported outcome

The ledger records supplier obligation Rp60.000 and product margin Rp20.000. Later COD/refund notes describe a subsequent state; they must not replace the initial Rp92.800 invoice.

## Verification limits

No historical SeaBank payment instruction, greeting or call-to-action is visible in this card. Dispatch and refund are not independently verified by bank or delivery receipts.

## Financial check

| Component | Value |
|---|---:|
| Product sales | Rp80.000 |
| Supplier product cost | Rp60.000 |
| Product margin | Rp20.000 |
| Shipping information | Rp12.800 |
| Initial invoice | Rp92.800 |

Product margin = sales minus supplier product cost. Shipping, donations and tips are separate flows.

### Reconstruction for illustration only

> Prepare2 Medium and2 Premium packs; show shipping separately.

This request is reconstructed from the ledger, not an original WhatsApp input. The original EVD-03 invoice is80.000+12.800=92.800. Later COD/refund notes cannot be retroactively presented as the original invoice. Sending of this exact card is not established.

## Sources and lessons

Supplier A Transaksi row 2; EVD-03.

[Catalog](../evidence/evidence_catalog.md) | [Anonymized ledger extracts](../evidence/verified_ledger_extracts.json) | [README](../README.md)

Private source locators are not public links. Screenshot captures are fromOctober; transactions are fromAugust-September 2026. Compare facts, calculations and lifecycle states before declaring completion. A required control is not proof that every run complied.

- [EVD-03](../evidence/public_redacted/EVD-03-invoice-2med-2prem.jpg): **HISTORICAL AI OUTPUT / INITIAL INVOICE**. The card shows subtotal Rp80.000 plus shipping Rp12.800. It does not prove dispatch, bank verification or a later COD invoice.
