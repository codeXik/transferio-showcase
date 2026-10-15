# Transferio — showcase

Windows desktop app that prepares voucher and chart-of-accounts files for moving accounting data from Zirve to Luca, two widely used Turkish accounting systems.

**Website:** [skynonlabs.com/transferio](https://skynonlabs.com/transferio.html) · [Türkçe](README.tr.md)

> Showcase only; source code is private.

| | |
|---|---|
| ![Detection](images/01-tespit.webp) | ![Year and period](images/02-yil-donem.webp) |
| ![Company](images/03-firma-secimi.webp) | ![Ready](images/04-hazirlandi.webp) |
| ![Notifications](images/06-bildirimler.webp) | ![Luca tracking](images/14-luca-islem-takip.webp) |

## How it works

```mermaid
flowchart LR
  Z[(Zirve SQL, read-only)] --> T[Transferio 5-step wizard]
  T --> O[Luca-ready voucher packages + logs + period summaries]
  O --> L[Luca import]
```

- **Read-only by design:** never writes to the database or touches Zirve files; output goes to a separate folder.
- **Real pre-flight checks:** host, SQL server, database connection, company data files, template, output folder and licence are actually tested before you start.
- **Safe packaging:** vouchers split into 50-voucher packages with debit/credit balance checks.
- Free for a single company; bulk preparation in Pro.

© 2026 Skynon Labs Ltd. All rights reserved. · hello@skynonlabs.com
