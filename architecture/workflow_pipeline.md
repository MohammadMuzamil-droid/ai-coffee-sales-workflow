# Documented workflow architecture

This preserves the owner's source SOP design. It is not proof of autonomous deployment or compliance in every historical run.

## Routing and source hierarchy

Project Instructions route tasks; Decision Log holds rules; each supplier Workflow holds SOP/literal output formats; each supplier ledger holds final state. Chat/screenshots are evidence or confirmation.

Identify supplier using products, sizes, prices, evidence and context, not name or amount alone. Ambiguous supplier or evidence outside chat authority: PERLU KONFIRMASI and STOP write.

Evidence -> route supplier -> read relevant existing rows -> interpret entire sequence -> match revisions/duplicates -> calculate -> batch affected writes -> read back -> reconcile -> qualified result or STOP.

## Execution tiers and safeguards

- Routine: targeted read/write/read-back on relevant active cells.
- Conditional: retrieve only applicable special rules, price snapshots or formats.
- Heavy: closing/material disputes require full relevant rules/ledgers and PRE-COMMIT.
- Finish interpretation before write; do not repeatedly write temporary decisions.
- One event across ledgers is one logical bookkeeping unit. This is not a claim of database transaction rollback. Partial failure or mismatch means STOP / PERLU REKONSILIASI.

## Independent lifecycle states

Customer payment, supplier remittance, invoice eligibility and closing are distinct. Sastra's default event order is not a mandatory dependency. Supplier payment is neither a prerequisite to invoice eligibility nor an automatic trigger for closing.

Supplier A COD excludes shipping from customer product transfer; transferred shipping is a separate supplier obligation unless supported deposit/payment reconciliation resolves it. Sastra non-COD normally means shipping advanced by Sastra. Evidence overrides defaults. Do not import Supplier A deposit/donation rules into Sastra automatically.

## Native header snapshot

Native Supplier A header read 14October 2026 has32 fields, including later Premium TOPLES fields. It is not the exact schema of each historical PDF export or proof that older outputs populated32 fields. Sedekah belongs in Arus Reseller.

| Position | Native field |
|---:|---|
| 1 | Tanggal |
| 2 | Pelanggan |
| 3 | Medium pcs |
| 4 | Premium pcs |
| 5 | Total pcs |
| 6 | Alamat Pengiriman |
| 7 | Ekspedisi/Jenis |
| 8 | Penjualan Produk |
| 9 | Ongkir |
| 10 | Metode Bayar Ongkir |
| 11 | Ongkir Disetor ke Supplier A |
| 12 | Sumber Pembayaran Ongkir |
| 13 | Status Ongkir ke Supplier A |
| 14 | Ongkir Wajib Ditransfer Sekarang |
| 15 | Tips Admin Supplier A |
| 16 | Setoran Medium |
| 17 | Setoran Premium |
| 18 | Setoran Produk |
| 19 | Total Setoran Supplier A |
| 20 | Diskon Reseller |
| 21 | Laba Kotor Produk |
| 22 | Laba Setelah Diskon |
| 23 | Laba Reseller |
| 24 | Status |
| 25 | Waktu Pembayaran |
| 26 | Periode Tutup Buku |
| 27 | Waktu Tutup Buku |
| 28 | Catatan |
| 29 | Kelengkapan Data |
| 30 | Premium TOPLES pcs |
| 31 | Setoran Premium TOPLES |
| 32 | Harga Jual Premium TOPLES/pcs |

## Closing

Select only eligible transactions. Check quantities, supplier cost, status, duplicates, existing periods, deposit pairs and reseller flows in PRE-COMMIT. Stop on conflicts before commit. Read back all affected writes and reconcile before completion.

[Methodology](../methodology/human_supervision_framework.md) | [Catalog](../evidence/evidence_catalog.md)
