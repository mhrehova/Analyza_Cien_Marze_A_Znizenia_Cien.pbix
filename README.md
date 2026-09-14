# Analyza_Cien_Marze_A_Znizenia_Cien.pbix
dashboard_analyza
# E-commerce Power BI Dashboard – Pricing & Margin Analysis

Power BI dashboard postavený nad relačným e-commerce datasetom, zameraný na analýzu cien, marží a vrátených objednávok.

## Dataset

Zdrojový dataset (`ecommerce_relational.xlsx`) obsahuje šesť prepojených tabuliek:

- **Categories** – kategórie produktov
- **Customers** – zákazníci
- **Date** – dátumová tabuľka pre časové analýzy
- **Products** – produktový katalóg
- **Orders** – objednávky (vrátane stavu objednávky, napr. "Vrátená")
- **Order Details** – jednotlivé položky objednávok

V druhej verzii datasetu boli do tabuľky **Order Details** doplnené vypočítané stĺpce:

- `OriginalPrice`, `DiscountPct`, `SalePrice`, `Cost`, `LineTotal`
- `MarginEUR`, `MarginPct`
- `ReturnReason` (dôvod vrátenia)

a do tabuľky **Orders** stĺpec `TotalMargin`. Všetky sú počítané pomocou Excel vzorcov (VLOOKUP, SUMIF), nie ako pevné hodnoty.

## Štruktúra dashboardu

Dashboard má päť stránok:

1. **Overview** – celkový prehľad výkonnosti
2. **Product Insights** – analýza produktov
3. **Customer Insights** – analýza zákazníkov
4. **Pricing and Margin Analysis** – analýza cien a marží
5. **Orders and Returns** – objednávky a vrátenia (na základe `Orders.Status` a `Order Details.ReturnReason`)

## Kľúčové DAX metriky

- Total Revenue
- Total Cost
- Total Margin €
- Margin % (počítané pomocou `SUMX` a `DIVIDE`)
- Total Orders
- Avg Order Value
- Markdown Loss €
- Return Rate

## Screenshoty

<img width="1597" height="901" alt="Dashboard_Prehlad" src="https://github.com/user-attachments/assets/28298b22-239f-48bc-847c-e0fc61777d06" />
<img width="1582" height="885" alt="Dashboard_Analyza_Produktov" src="https://github.com/user-attachments/assets/76aae09e-b841-46e0-a53c-30730fa4487f" />
<img width="1596" height="892" alt="Dashboard_Cenotvorba_Marza" src="https://github.com/user-attachments/assets/9115bcd4-4fa4-4d50-95fb-190fd41170be" />
<img width="1592" height="892" alt="Dashboard_Objednavky_Vratenia" src="https://github.com/user-attachments/assets/7005d75c-7be1-4eec-b5ad-9a4009f9e70d" />



*(nahraď obrázky vlastnými screenshotmi zo stránok dashboardu – ulož ich do priečinka `images/` v repozitári)*

## Použité nástroje

Power BI Desktop · Power Query · DAX · Excel (príprava a výpočty v zdrojovom datasete)
