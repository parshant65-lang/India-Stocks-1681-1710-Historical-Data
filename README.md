# India-Stocks-1681-1710-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 1681 to 1710)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-1681-1710-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (1681 to 1710)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 1681 | `MOLBIO` | Molbio Diagnostics Limited | `MOLBIO.NS` |
| 1682 | `MOLDTECH` | Mold-Tek Technologies Limited | `MOLDTECH.NS` |
| 1683 | `MOLDTKPAC` | Mold-Tek Packaging Limited | `MOLDTKPAC.NS` |
| 1684 | `MOMSBELIEF` | Rays of Belief Limited | `MOMSBELIEF.NS` |
| 1685 | `MONARCH` | Monarch Networth Capital Limited | `MONARCH.NS` |
| 1686 | `MONEYBOXX` | Moneyboxx Finance Limited | `MONEYBOXX.NS` |
| 1687 | `MONEYVIEW` | Moneyview Limited | `MONEYVIEW.NS` |
| 1688 | `MONTECARLO` | Monte Carlo Fashions Limited | `MONTECARLO.NS` |
| 1689 | `MORARJEE` | Morarjee Textiles Limited | `MORARJEE.NS` |
| 1690 | `MOREPENLAB` | Morepen Laboratories Limited | `MOREPENLAB.NS` |
| 1691 | `MOSCHIP` | Moschip Technologies Limited | `MOSCHIP.NS` |
| 1692 | `MOTISONS` | Motisons Jewellers Limited | `MOTISONS.NS` |
| 1693 | `MOTOGENFIN` | The Motor & General Finance Limited | `MOTOGENFIN.NS` |
| 1694 | `MPDL` | MPDL Limited | `MPDL.NS` |
| 1695 | `MPIMANIPAL` | Manipal Payment and Identity Solutions Limited | `MPIMANIPAL.NS` |
| 1696 | `MPSLTD` | MPS Limited | `MPSLTD.NS` |
| 1697 | `MSL` | Mangalam Seeds Limited | `MSL.NS` |
| 1698 | `MSPL` | MSP Steel & Power Limited | `MSPL.NS` |
| 1699 | `MSTCLTD` | Mstc Limited | `MSTCLTD.NS` |
| 1700 | `MTEDUCARE` | MT Educare Limited | `MTEDUCARE.NS` |
| 1701 | `MTNL` | Mahanagar Telephone Nigam Limited | `MTNL.NS` |
| 1702 | `MUFIN` | Mufin Green Finance Limited | `MUFIN.NS` |
| 1703 | `MUFTI` | Credo Brands Marketing Limited | `MUFTI.NS` |
| 1704 | `MUKANDLTD` | Mukand Limited | `MUKANDLTD.NS` |
| 1705 | `MUKESHB` | Mukesh Babu Financial Services Limited | `MUKESHB.NS` |
| 1706 | `MUKKA` | Mukka Proteins Limited | `MUKKA.NS` |
| 1707 | `MUKTAARTS` | Mukta Arts Limited | `MUKTAARTS.NS` |
| 1708 | `MUNJALAU` | Munjal Auto Industries Limited | `MUNJALAU.NS` |
| 1709 | `MUNJALSHOW` | Munjal Showa Limited | `MUNJALSHOW.NS` |
| 1710 | `MURUDCERA` | Murudeshwar Ceramics Limited | `MURUDCERA.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream MOLBIO 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-1681-1710-Historical-Data/main/MOLBIO/1m/2026/10/MOLBIO_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
