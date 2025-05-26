# A mid-size manufacturer struggles to keep the right amount of finished-goods inventory on hand. Stock-outs on high-revenue products hurt sales, while excess inventory ties up cash and warehouse space.
Goal: Use raw transactions, sales, and open-order data to find the SKUs that matter most and prescribe the cheapest, service-level-safe replenishment rules for each class of items.


# Solution Approach
Data wrangling:
Merge the three files → master table with demand frequency, total demand, unit economics.
ABC analysis:
Rank SKUs by revenue contribution; label A (≈ 15 %), B (≈ 25 %), C (≈ 60 %).
Policy selection & sizing:
A-items: continuous review (s, Q) with safety stock.
B-items: compare periodic policies (R, S) vs. (R, Q) and pick the lower-cost option.
Cost comparison:
Simulate one year of operations → show that (R, S) beats (R, Q) for B-items by ∼ $1.6 k per month.
