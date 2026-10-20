# Menu-engineering-Proof-of-concept
Using a fictional dataset of 50 restaurants divided in 5 types (Cafe, casual dining ,fine dining,food stall...) in the year 2024-2025 
Technical Report: Restaurant Menu Engineering (Proof of Concept)


Executive Summary

This Proof of Concept (PoC) applies the Kasavana & Smith Menu Engineering Matrix to evaluate and optimize menu performance across four distinct restaurant concepts (Café, Casual Dining, Food Stall, and Fine Dining). Using a one-year transaction dataset (2024–2025) monitoring daily item-level sales for 50 restaurants, this analysis identifies pricing, volume, and margin discrepancies to unlock hidden profitability.
Data cleanliness was verified using COUNTBLANK and descriptive filters, ensuring an exhaustive sample size with zero missing records.

1. Core Methodology

Menu items were categorized into four groups based on two critical benchmarks:
1. Popularity Index (70% Rule): Items exceeding 1 / N × 70% of total sales mix are classified as High Volume.
   2.   Average Contribution Margin: Items generating a unit margin higher than the concept's weighted average are classified as High Profit.

Spreadsheet Architecture & Exact Formulas

To build this dynamic classification engine without manual data mapping errors, two core layers of Excel programming were engineered:
• Automated Price Extraction (VLOOKUP):
To dynamically pull the accurate unit selling prices for each menu item from external raw data records, the following exact logic structure was deployed:excel
=VLOOKUP(A18, Sheet13!$A$1:$E$2382, 4, FALSE) 
Multi-Criteria Quadrant Classification (Nested IF):
Rather than sorting data fields manually, automated decision trees were embedded directly inside the classification cells. The logical quadrant mapping follows this exact structural blueprint:excel
=IF(J18="High", IF(K18="High", "Star", "Puzzle"), IF(K18="High", "Plowhorse", "Dog"))
The Kasavana & Smith Matrix (Logical Quadrants)


Contribution Margin (J) \ Sales Volume (K)	High Volume ("High")	Low Volume ("Low")
High Profit ("High")	Star	Puzzle
Low Profit ("Low")	Plowhorse	Dog


2. Concept Analysis & Financial Breakdown


Concept A: Café

• Total Volume: 380,311 items sold
• Popularity Threshold: 7.78%
• Average Unit Margin: $9.84

Menu Item	Sales Mix %	Unit Margin ($)	Classification
Beef Rendang	2.0%	$27.17	Puzzle
Cendol	12.0%	$8.74	Plowhorse
Chicken Chop	7.0%	$15.57	Puzzle
Iced Lemon Tea	15.0%	$3.94	Plowhorse
Kaya Toast Set	22.0%	$9.46	Plowhorse
Mushroom Soup	5.0%	$15.93	Puzzle
Nasi Lemak	8.0%	$7.58	Plowhorse
Spaghetti Carbonara	6.0%	$40.14	Puzzle
Teh Tarik	24.0%	$2.64	Plowhorse


Concept B: Casual Dining

• Average Unit Margin: $16.82

Menu Item	Sales Mix %	Unit Margin ($)	Classification
Beef Rendang	1.0%	$37.56	Puzzle
Cendol	13.0%	$9.22	Plowhorse
Char Kway Teow	4.0%	$23.49	Puzzle
Chicken Chop	4.0%	$31.31	Puzzle
Chicken Rice	5.0%	$21.30	Puzzle
Iced Lemon Tea	10.0%	$5.15	Plowhorse
Kaya Toast Set	24.0%	$9.10	Plowhorse
Mushroom Soup	3.0%	$16.71	Puzzle
Nasi Lemak	4.0%	$5.58	Dog
Spaghetti Carbonara	4.0%	$51.46	Puzzle
Teh Tarik	28.0%	$2.89	Plowhorse


Concept C: Food Stall

• Average Unit Margin: $6.69

Menu Item	Sales Mix %	Unit Margin ($)	Classification
Beef Rendang	2.0%	$24.39	Puzzle
Cendol	11.0%	$4.72	Plowhorse
Char Kway Teow	2.0%	$11.90	Puzzle
Chicken Rice	3.0%	$8.15	Puzzle
Kaya Toast Set	20.0%	$6.91	Star
Laksa	3.0%	$7.98	Puzzle
Nasi Lemak	6.0%	$5.41	Dog
Roti Canai	21.0%	$1.68	Plowhorse
Tandoori Chicken	7.0%	$20.20	Puzzle
Teh Tarik	25.0%	$1.56	Plowhorse

Concept D: Fine Dining

• Average Unit Margin: $34.90

Menu Item	Sales Mix %	Unit Margin ($)	Classification
Beef Rendang	7.0%	$71.15	Puzzle
Chicken Chop	16.0%	$63.87	Star
Iced Lemon Tea	32.0%	$7.24	Plowhorse
Mushroom Soup	9.0%	$25.78	Puzzle
Nasi Lemak	24.0%	$14.25	Plowhorse
Spaghetti Carbonara	12.0%	$46.54	Star
3. Strategic Recommendations


High-Volume / Low-Profit (Plowhorses)

• Target Items: Teh Tarik, Kaya Toast, Iced Lemon Tea.
• Actions: Implement supplier renegotiations for core high-turnover ingredients (condensed milk, tea leaves, sandwich bread). For non-traditional beverages like Iced Lemon Tea, execute micro-price increases ($0.15 - $0.25) which go unnoticed by consumers but scale significantly due to high purchase frequency.

Low-Volume / High-Profit (Puzzles)

• Target Items: Beef Rendang, Spaghetti Carbonara, Mushroom Soup.
• Actions: Avoid direct price reductions or monetary discounts, as doing so destroys their main asset: high profitability. Instead, shift volume during high-demand windows (Saturdays and Sundays) using menu psychology (visual highlighting on the first page) and strategic cross-selling bundles.

Cross-Concept Bundling Matrix

• Food Stall / Café: Create a combo tying high-volume items (Roti Canai / Teh Tarik) with the Beef Rendang to increase the meat item's 2% market penetration without undercutting its unit price.
• Fine Dining: Introduce a "Prestige Set" pairing the Mushroom Soup (Puzzle Entry, $25.78 margin) with top-performing Stars like the Chicken Chop or Spaghetti Carbonara. This seamlessly moves clients from single items to structured courses.<img width="960" height="540" alt="Screenshot 2026-10-20 183918" src="https://github.com/user-attachments/assets/4540c7de-0789-43b3-9970-5a1164818328" />
<img width="960" height="540" alt="Screenshot 2026-10-20 183955" src="https://github.com/user-attachments/assets/70d7ea2c-46a4-4bbd-926a-3a561270e388" />

