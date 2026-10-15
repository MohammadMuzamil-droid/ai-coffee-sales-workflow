# CASE-05: Closing QA: separate derived results from conflicted reports

Evidence strength is identified in each section. No exact historical prompt, bank reconciliation or dispatch is invented.

## Business problem

Supplier obligations and reseller earnings were conflated in a historical closing report. Intermediate AI summaries could be mistaken for final accounting states.

## Historical input

TB-001 has six transactions in native Transaksi rows 2-7. The source closing summary still shows Rp620.000 as gross/net reseller profit and zero donation, conflicting with row-level arithmetic and Arus Reseller.

## AI task and retained output

ChatGPT generated historical closing summaries. EVD-07/08 show an intermediate six-transaction TB-002 draft; these screenshots are retained as failure/process evidence, not final settlement instructions.

## Human judgment

The original workflow specifies pre-commit checks, eligible transaction selection, read-back and reconciliation. This release QA independently totals the native rows and explicitly retains the original conflict rather than editing source ledgers.

## Supported outcome

TB-001:20 Medium+21 Premium=41 packs; sales Rp825.000; supplier Rp620.000; product margin Rp205.000; donation Rp800; tips Rp0. Ledger-derived reseller result Rp205.800.

## Verification limits

Rp205.800 is not independently bank-reconciled profit. The cause of the source inconsistency is unknown. TB-002 later native state has14 transactions and differs from the earlier six-transaction snapshot.

## Financial check

| Component | Value |
|---|---:|
| Product sales | Rp825.000 |
| Supplier product cost | Rp620.000 |
| Product margin | Rp205.000 |
| Donation | Rp800 |
| Tips | Rp0 |
| Ledger-derived result | Rp205.800 |

Product margin = sales minus supplier product cost. Shipping, donations and tips are separate flows.

## TB-001 independent row totals

| Source row | Medium | Premium | Sales | Supplier | Margin |
|---|---:|---:|---:|---:|---:|
| 2 | 2 | 2 | Rp80.000 | Rp60.000 | Rp20.000 |
| 3 | 10 | 0 | Rp150.000 | Rp100.000 | Rp50.000 |
| 4 | 2 | 14 | Rp380.000 | Rp300.000 | Rp80.000 |
| 5 | 4 | 4 | Rp160.000 | Rp120.000 | Rp40.000 |
| 6 | 2 | 0 | Rp30.000 | Rp20.000 | Rp10.000 |
| 7 | 0 | 1 | Rp25.000 | Rp20.000 | Rp5.000 |

20+21=41;825.000-620.000=205.000;205.000+800-0=205.800. Shipping87.500 is period information, shipping remitted0. Prices are summed as historically recorded; newer rules are not applied retroactively.

## Preserved source conflict

Laporan Tutup Buku E9 shows supplier 620.000. K3:L3 calls620.000 gross profit; K4:L4 shows donation 0; L14 calls620.000 net profit. Arus Reseller row 3 records800 forTB-001. These conflicting observations are retained; cause unknown. Original records were not changed.

## TB-002 warning and later state

**EVD-07/08 are intermediate drafts, NOT validated final closing records. Do not use them as settlement instructions.** The public crop does not visibly contain the subsequent warning, 'Hasil tadi belum valid dan jangan dijadikan acuan setoran'. The warning here is editorial context, not fabricated image content.

| Metric | Earlier draft | Later native ledger |
|---|---:|---:|
| Transactions |6|14|
| Medium /Premium |16 /25|21 /66|
| Packs |41|87|
| Sales |Not established here|Rp1.925.000|
| Supplier cost |Rp660.000|Rp1.530.000|
| Margin |Rp175.000|Rp395.000|
| Donation |Rp0|Rp70.000|
| Tips |Rp20.500|Rp20.500|
| Derived result |Rp154.500|Rp444.500|

Draft175.000-20.500=154.500; later 1.925.000-1.530.000=395.000;395.000+70.000-20.500=444.500. The later state is ledger-supported, not independently bank-reconciled.

## Sources and lessons

Yek Ali Transaksi rows 2-7; Laporan Tutup Buku E9, K3:L3, K4:L4, L14; Arus Reseller row 3; EVD-07/08.

[Catalog](../evidence/evidence_catalog.md) | [Anonymized ledger extracts](../evidence/verified_ledger_extracts.json) | [README](../README.md)

Private source locators are not public links. Screenshot captures are fromOctober; transactions are fromAugust-September 2026. Compare facts, calculations and lifecycle states before declaring completion. A required control is not proof that every run complied.

- [EVD-07](../evidence/public_redacted/EVD-07-closing-report-tb002.jpg): **INTERMEDIATE DRAFT / NOT FINAL**. NOT a validated final report. The draft shows 6 transactions, supplierRp 660.000 and reseller resultRp 154.500. The later ledger has14 transactions. Do not use this image as settlement instructions.

- [EVD-08](../evidence/public_redacted/EVD-08-reseller-margin-tips.jpg): **INTERMEDIATE DRAFT / NOT FINAL**. NOT a validated final report. Rp175.000 minus tipsRp 20.500 =Rp154.500 describes the earlier draft. The public image does not display the later invalid-result warning; this caption supplies the essential limitation, not a fabricated screenshot annotation.
