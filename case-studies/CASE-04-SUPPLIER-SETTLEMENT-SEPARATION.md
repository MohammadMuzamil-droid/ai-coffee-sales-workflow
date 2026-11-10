# CASE-04: Sastra: item-level validation and separate payment states

Evidence strength is identified in each section. No exact historical prompt, bank reconciliation or dispatch is invented.

## Business problem

A second supplier has a different product catalog and shipping policy. Its obligations must not inherit Supplier A rules or be confused with a different remittance batch.

## Historical input

SC-20260928-004 contains four different 250g items. Native Detail Pesanan supplies the historical item prices; Master Harga has 48 entries across 100g, 250g, 500g and 1kg.

## AI task and retained output

ChatGPT-assisted administration is the workflow context. The retained ledger note labels the old Rp337.000/Rp34.000 aggregate as incorrect and records an audit correction. A historical transcript proving who produced or corrected that old aggregate at order time is not supplied.

## Human judgment

The supported review is item-by-item arithmetic and supplier routing. This release QA recomputes 43.000 + 48.000 + 88.000 + 146.000 = Rp325.000. It does not attribute the later forensic correction to an undocumented historical action by me.

## Supported outcome

Sales Rp371.000 - supplier product cost Rp325.000 = margin Rp46.000. Shipping Rp34.000 less subsidy Rp10.000 = Rp24.000. Related supplier obligation Rp349.000. Historical source status: MENUNGGU PEMBAYARAN.

## Verification limits

The separate 16 September remittance Rp219.000 concerns two earlier orders (Rp54.000 + Rp165.000), not settlement of the 28 September order. Bank settlement of the latter is not established.

## Financial check

| Component | Value |
|---|---:|
| Product sales | Rp371.000 |
| Supplier product cost | Rp325.000 |
| Product margin | Rp46.000 |
| Shipping information | Rp24.000 |
| Related supplier obligation | Rp349.000 |

Product margin = sales minus supplier product cost. Shipping, donations and tips are separate flows.

| Historical item, 250g x1 | Sales | Supplier | Margin |
|---|---:|---:|---:|
| Robusta Premium | Rp49.000 | Rp43.000 | Rp6.000 |
| Robusta Peaberry | Rp54.000 | Rp48.000 | Rp6.000 |
| Arabika Honey Sumbing | Rp100.000 | Rp88.000 | Rp12.000 |
| Arabika Luwak Specialty | Rp168.000 | Rp146.000 | Rp22.000 |

Supplier 43.000+48.000+88.000+146.000=325.000;371.000-325.000=46.000. Shipping34.000-10.000 subsidy=24.000;325.000+24.000=349.000. The note says KOREKSI AUDIT: old 337.000/34.000 was corrected. It does not establish original actor/timing.

Earlier 16 September:43.000+11.000=54.000;146.000+19.000=165.000;54.000+165.000=219.000. These belong to different orders.

## Sources and lessons

Sastra Transaksi row 5; Detail Pesanan rows 5-8; Master Harga; Workflow Sastra.

[Catalog](../evidence/evidence_catalog.md) | [Anonymized ledger extracts](../evidence/verified_ledger_extracts.json) | [README](../README.md)

Private source locators are not public links. Screenshot captures are fromOctober; transactions are fromAugust-September 2026. Compare facts, calculations and lifecycle states before declaring completion. A required control is not proof that every run complied.
