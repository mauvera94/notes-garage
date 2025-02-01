---
title: Calculating overall product Conversion Rate with split journeys
created: 2025-01-31
updated: 2025-01-31
description: 
aliases: 
---

## Understanding the Split

When a journey divides into multiple paths (e.g., different user flows, product categories, or actions), calculate the overall conversion rate as a weighted average of the conversion rates of each path.

Each journey consists of step-by-step conversion rates, with users distributing themselves among different paths. 


## Example 

Consider the following funnel:

- **Step 1:** Landing Page → Product Page (CR = 40%)
- **Path A:** Adds to Cart (CR = 50%) → Checkout (CR = 60%) → Purchase (CR = 80%)
- **Path B:** Direct Checkout (CR = 30%) → Purchase (CR = 90%)

User distribution:

- 60% of users follow **Path A**
- 40% of users follow **Path B**

### Calculating Conversion for Each Path

To determine the conversion rate for each path, multiply the sequential step conversion rates:

- **Path A total CR** = 40% × 50% × 60% × 80% = 9.6%
- **Path B total CR** = 40% × 30% × 90% = 10.8%

## Weighting by Traffic Share

The overall conversion rate accounts for the proportion of users taking each path:

$CR_{\text{overall}} = (9.6\% \times 60\%) + (10.8\% \times 40\%)$

$CR_{\text{overall}} = 5.76\% + 4.32\% = 10.08\%$

## Key Takeaways

- The overall conversion rate is not a simple multiplication of one set of steps when dealing with multiple journeys.
- Instead, each path's conversion rate must be calculated separately and weighted by the proportion of users taking that path.

---
## References
