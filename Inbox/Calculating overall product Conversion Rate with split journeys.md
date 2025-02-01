---
title: Calculating overall product Conversion Rate with split journeys
created: 2025-01-31
updated: 2025-02-01
description: 
aliases: 
---

>[!summary]
> Each path's conversion rate must be calculated separately and weighted by the proportion of users taking that path.

## Understanding the Split

When a journey divides into multiple paths (e.g., different user flows, product categories, or actions), calculate the overall conversion rate as a weighted average of the conversion rates of each path.

Each journey consists of step-by-step conversion rates, with users distributing themselves among different paths:

1. Calculate the [[Conversion Rate]] of each journey individually
2. Get the proportion of users taking each journey
3. Weight the CR against the proportion and add them together to get the **Overall conversion rate**

> [!formula] 
>$CR_{\text{overall}} = \sum_{i=1}^{n} (CR_i \times w_i)$
>
>- $CR_{\text{overall}}$  is the overall conversion rate
>$CR_i  is the conversion rate for path  i
>- $w_i$  is the proportion of users taking path  i
> - n  is the total number of paths.


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