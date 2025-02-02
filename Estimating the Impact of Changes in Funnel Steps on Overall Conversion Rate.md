---
title: Estimating impact overall conversion rate
created: 2025-01-27
updated: 2025-02-02
description: 
aliases: 
---
When a single step in the funnel improves or deteriorates, it has a cascading effect on the [[overall product conversion rate]]. By recalculating the overall conversion rate with the adjusted step, you can estimate the impact of these changes.

## Steps to Estimate the Impact

1. **Calculate the Current Overall Conversion Rate**

Use the product of conversion rates across all steps in the funnel:

$\text{Overall Conversion Rate} = \prod_{i=1}^{N} \text{Conversion Rate at Step } i$

2. **Apply the Change to the Target Step**

Adjust the [[conversion rate]] of the target step based on the percentage improvement because a [[Conversion Rate Optimization]] strategy or deterioration:

$\text{New Conversion Rate at Step } k = \text{Original Conversion Rate at Step } k \times (1 + \text{Change})$

3. **Recalculate the New Overall Conversion Rate**

Substitute the new conversion rate for the target step into the CR formula:

$\text{New CR}_{overall} = CR_{step1} \times CR_{step2} \times\dots \text{(New) CR}_{stepk} \dots \times CR_{stepN}$

>[!note]- In case a journey splits
> Remember that if a journey splits you must calculate CR separately and weight by the proportion of users taking that path [[Calculating overall product Conversion Rate with split journeys]]

4. **Determine the Impact**
- **Absolute Impact**: 

$\Delta\text{ Impact (absolute)} = \text{New Overall Conversion Rate} - \text{Original Overall Conversion Rate}$

-  **Relative Impact (%)**:
  
  $\text{Relative Impact (\%)} = \left( \frac{\text{New Overall Conversion Rate} - \text{Original Overall Conversion Rate}}{\text{Original Overall Conversion Rate}} \right)$
  
- **New Total Conversions**

Use the new overall conversion rate to estimate total conversions:

$\text{New Total Conversions} = \text{Total Visitors} \times \text{New Overall Conversion Rate}$

>[!attention]
> This formula is just an **estimation**, changes in cohort or flows most likely will have a significant influence in downstream outcomes, where the overall conversion rate can be impacted.
> >[!example]- Example: Changing a CTA on the Signup Page
> >Change: CTA updated from *“Start Free Trial”* to *“Get Started – No Credit Card Required.”*
> >**Downstream Effects:**
> >- Higher signup rate – More users sign up due to reduced friction.
> >- Lower user commitment – Some users may sign up without serious intent.
> >- Higher drop-off in onboarding – Less engaged users abandon early.
> >- Trial-to-paid conversion impact – If value isn’t clear, fewer users upgrade.

### Why Is It Important?

- **Identifies High-Impact Opportunities**: Understanding the potential effect of optimizing or neglecting a single step helps focus resources effectively.
- **Improves Funnel Performance**: Small changes in key steps with low conversion rates can significantly boost overall performance ([[Prioritization of conversion rate optimization]].
- **Quantifies [[ROI]]**: Provides a clear view of how incremental changes contribute to broader business outcomes and provides a clear impact to build a business case.