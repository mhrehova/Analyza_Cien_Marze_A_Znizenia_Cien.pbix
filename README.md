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


![Overview](images/Dashboard_Prehlad.png)
![Pricing and Margin Analysis](images/Dashboard_Cenotvorba_Marza.png)
![Orders and Returns](images/Dashboard_Objednavky_Vratenia.png)

*(nahraď obrázky vlastnými screenshotmi zo stránok dashboardu – ulož ich do priečinka `images/` v repozitári)*

## Použité nástroje

Power BI Desktop · Power Query · DAX · Excel (príprava a výpočty v zdrojovom datasete)
