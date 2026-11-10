# CASE-03: Two incorrect receipt readings and a human correction

Evidence strength is identified in each section. No exact historical prompt, bank reconciliation or dispatch is invented.

## Business problem

ChatGPT read a printed shipping total incorrectly twice, creating inconsistent billing amounts.

## Historical input

EVD-01 is a physical receipt photograph with IDR27.200. It lists one parcel, not one retail coffee pack. The related order contains 4 Medium + 4 Premium.

## AI task and retained output

The first reading used Rp7.200 and total Rp167.200 (EVD-02). The retry used Rp72.000 and total Rp232.000 (EVD-04). EVD-05 shows the operator insisting on 27200 and the corrected Rp187.200 calculation.

## Human judgment

I compared the response with the printed amount and corrected it. EVD-06 shows a hold on a Rp188.000 payment until payer matching was confirmed. The Rp800 excess is separately classified as customer donation in Arus Reseller.

## Supported outcome

Sales Rp160.000 + shipping Rp27.200 = initial corrected bill Rp187.200. Ledger-recorded payment Rp188.000 creates Rp800 excess. The later ledger records COD to courier, shipping remitted to supplier Rp0 and refund notes.

## Verification limits

Payment and refund are ledger/conversation-recorded, not independently bank-verified. No technical cause of the reading error is established. The evidence does not establish detection through parcel weight.

## Financial check

| Component | Value |
|---|---:|
| Product sales | Rp160.000 |
| Supplier product cost | Rp120.000 |
| Product margin | Rp40.000 |
| Shipping information | Rp27.200 |
| Initial invoice | Rp187.200 |
| Ledger-recorded payment | Rp188.000 |
| Donation | Rp800 |

Product margin = sales minus supplier product cost. Shipping, donations and tips are separate flows.

Wrong bills:160.000+7.200=167.200;160.000+72.000=232.000. Corrected bill:160.000+27.200=187.200. Excess:188.000-187.200=800. A20.000 undercharge would equal50% of40.000 margin if it occurred; this is potential exposure, not a measured loss. The correction image includes an intermediate supplier-plus-freight figure147.200. Later COD/refund notes leave supplier product obligation120.000 and shipping remitted0.

## Sources and lessons

EVD-01, 02, 04, 05, 06; Supplier A Transaksi row 5, notes AB; Arus Reseller row 3.

[Catalog](../evidence/evidence_catalog.md) | [Anonymized ledger extracts](../evidence/verified_ledger_extracts.json) | [README](../README.md)

Private source locators are not public links. Screenshot captures are fromOctober; transactions are fromAugust-September 2026. Compare facts, calculations and lifecycle states before declaring completion. A required control is not proof that every run complied.

- [EVD-01](../evidence/public_redacted/EVD-01-physical-receipt-27200.jpg): **ORIGINAL RECEIPT / REDACTED PUBLIC COPY**. The printed total is Rp27.200. Qty 1 refers to a parcel. This is receipt evidence, not a bank record.

- [EVD-02](../evidence/public_redacted/EVD-02-chatgpt-misread-7200.jpg): **HISTORICAL AI OUTPUT / INCORRECT**. The AI invoice shows shipping Rp7.200 and total Rp167.200. These are wrong outputs, retained for evaluation.

- [EVD-04](../evidence/public_redacted/EVD-04-chatgpt-misread-72000.jpg): **HISTORICAL AI OUTPUT / INCORRECT RETRY**. The retry shows shipping Rp72.000 and bill Rp232.000. Prior redaction obscures some prompt wording; the incorrect numbers remain visible.

- [EVD-05](../evidence/public_redacted/EVD-05-human-correction-27200.jpg): **HISTORICAL INTERVENTION / CORRECTED BILL**. The operator specifies 27200 and the AI corrects the bill toRp 187.200. A nonessential profane word is partly masked; numeric evidence is unchanged. The supplier+freight figure is an intermediate state before later COD/refund notes.

- [EVD-06](../evidence/public_redacted/EVD-06-payment-transfer-188k.jpg): **HISTORICAL CHAT / PAYMENT MATCHING**. The chat holds the payment pending payer confirmation, then describes matching. The upper subtotal belongs to a separate working-state recap, not final TB-001. Exact date/time is masked; Rp800 is corroborated by the ledger, partly obscured at the screenshot bottom.
