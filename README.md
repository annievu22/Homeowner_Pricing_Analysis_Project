# 📉 Homeowner Insurance Pricing & Claims Optimization

![Language](https://img.shields.io/badge/Language-Excel-16A085)
![Tool](https://img.shields.io/badge/Methodology-Actuarial%20Pricing%20Model-F39C12)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)
![Domain](https://img.shields.io/badge/Domain-Insurance-red)

> A comprehensive Excel-based actuarial project that evaluates homeowner policy attributes, applies credibility-adjusted loss cost analysis, and recommends pricing discounts to improve competitiveness and maintain profitability.

---

## 1. Overview

This project applies actuarial pricing methods to analyze claim experience from a national homeowner insurance portfolio. Using Excel, it evaluates how certain policy features (like roof type, sensors, and deductible levels) impact losses, to recommend actuarially sound discounts. The analysis blends client-specific data with credibility theory to ensure pricing accuracy and fairness.

---

## 2. Business Objectives

### 2.1. Business Problem

Homeowner insurers face challenges in balancing competitive pricing with profitability, particularly as certain property features (e.g., roof material, sensors, and deductible levels) impact loss behavior. Insurers risk overcharging safe policyholders without actuarially sound adjustments or underpricing high-risk segments, leading to loss ratio volatility and reduced market competitiveness.

> **Key questions addressed:**
>
> * Which homeowner features (roof, sensors, deductible, etc.) correlate with favorable or unfavorable loss experience?
> * How can we adjust for credibility when segment volumes vary widely?
> * What discount structure can match risk while maintaining revenue neutrality?
> * How does our portfolio compare against benchmark competitors in terms of pricing and loss ratio?

### 2.2. Business Impact & Insights

* Misaligned discount structures can lead to adverse selection and policyholder churn.  
* Competitor analysis reveals the insurer offers below-market incentives for key safety features such as water sensors, upgraded roofing, and monitored alarm systems.  
* Risk-adjusted pricing, informed by loss ratio credibility, enables fairer premium structures and improved customer retention.  
* A refined discount strategy—balanced with portfolio-wide revenue offsets—can position the insurer to grow market share while maintaining profitability.

---

## 3. Data Sources

This project utilizes a structured Excel workbook containing policy-level premium data, claim records, feature definitions, and industry benchmarks to support actuarial pricing and risk analysis for homeowner’s insurance.

**Workbook Overview:**

| Sheet Name              | Description |
|-------------------------|-------------|
| Discount Definitions | Lists base and feature discount levels across water sensors, alarm types, and roof types. |
| Premiums              | Contains exposure volumes and earned premiums by feature combinations, used for weighting and offsetting. |
| Losses and LAE        | Provides total incurred losses and loss adjustment expenses (LAE) by feature combination. |
| Claim Counts          | Offers frequency-level data for credibility adjustment calculations. |
| Competitor Information| Summarizes market-average discounts and share for Apples, Bananas, and Avocado. |
| Company Expenses      | Details internal cost structure, including a 28.8% expense ratio used in break-even calculations. |

**Key Fields:**

* Incurred Loss & LAE (\$)
* Claim Frequency
* Earned Premium (\$)
* Exposure Volume
* Discount Factor Benchmarks
* Base Assumptions
* Expense Ratio

### 🔗 Dataset Workbook Links

- **Google Drive Download:**  
  [📁 View Dataset (Google Drive)](https://docs.google.com/spreadsheets/d/1rAK6jleev0WOZRv-2HkR1nuUvUNK3_v4/edit?usp=sharing&ouid=115534730882318352678&rtpof=true&sd=true)

---

## 4. Methodology & Excel Analysis

This section outlines the Excel-based workflow used to analyze policyholder data, apply actuarial models, and generate premium discount recommendations based on risk-adjusted loss experience.

## 4.1. Key Assumptions

- **Loss Ratio Interpretation:**  
  A loss ratio below 0.6 indicates strong profitability, while values between 0.6 and 1.0 suggest lower profitability. Ratios under 0.5 may indicate potential overpricing.

- **Credibility Weighting:**  
  For segments with low claim volumes, we assume observed loss ratios may be distorted by random variation. Credibility blending is used to ensure more stable, reliable results.

- **Premium-Based Weighting:**  
  Portfolio weights are calculated using earned premiums to preserve revenue neutrality across proposed discounts, following best practices in actuarial pricing.

- **Claim Cost Stability:**  
  Historical claim costs by feature are assumed to be reflective of future experience, with adjustments for inflation and trend where appropriate.

- **Feature Effectiveness:**  
  Safety features such as water sensors, alarms, and hail-resistant roofing are expected to continue delivering meaningful loss mitigation benefits, justifying continued discounting.


### 4.2. Analytical Approach

- Evaluated Loss Cost (per exposure) for each homeowner feature.
- Applied credibility weighting to smooth small segment results.
- Benchmarked against industry competitors for competitive positioning.
- Proposed breakeven discounts to align with adjusted loss costs.
- Offset base rates to preserve total written premium across the portfolio.

### 4.3. Actuarial Modeling Methodology

- **Credibility Weighting:** Adjusts observed loss ratio based on claim volume. 
> Z = √(Claim Count : 1082)

- **Adjusted Loss Ratio (Adj LR):** Blends client-specific and total loss experience.
> Adj LR = Z x Case LR + (1 - Z) x Total LR  

- **Feature Discount Factor:** Relativity used to suggest fair pricing for each feature tier.
> Feature Factor = Feature Adj LR : Base Adj 
  
- **Breakeven Discount:** Ensures discount maintains expected profitability.  
> Discount = 1 - (Feature Adj LR + Expense Ratio)

- **Offset Base Rate Calculation:** Normalizes the portfolio post-discount, keeping total revenue stable.

---

## 5. Key Findings

## 5.1. Misaligned Discounts with Industry Benchmarks

Pickles provides lower discounts for key safety features compared to market averages, making its pricing less attractive to risk-averse policyholders.

- Water Sensor: 6% (Pickles) vs. **16%** (Market)
- Alarm Type 4: 8% (Pickles) vs. **25%** (Market)
- Roof Type 3: 7% (Pickles) vs. **13%** (Market)

Since these discounts are much lower than the market average, safer homeowners may be drawn to competitors offering better incentives. This puts the company at risk of losing profitable, low-risk customers and ultimately weakens its market position.

![Discount Misalignment Chart](https://github.com/annievu22/Homeowner_Pricing_Analysis_Project/blob/main/Homeowner%20Pricing%20Project%20-%20Key%20Findings/Finding%201.png)


## 5.2. Loss Ratio Improvement from Safety Feature Upgrades

Loss ratios are consistently lower for homes with upgraded safety features, demonstrating a strong relationship between discounts and actual risk reduction.

- Water Sensor: 0.61 → 0.56  
- Roof Type 1 vs. Type 2/3: 0.63 → 0.57  
- Alarm Type 1 vs. Type 4: 0.64 → 0.58

The consistent performance of upgraded features shows a strong link between safety improvements and reduced claims. Offering more competitive discounts would reward low-risk behavior, promote retention, and improve pricing accuracy.

![Credibility Loss Ratios](https://github.com/annievu22/Homeowner_Pricing_Analysis_Project/blob/main/Homeowner%20Pricing%20Project%20-%20Key%20Findings/Finding%202.png)

## 5.3. Discount Levels Below Break-even Thresholds**

The current discounts fall far short of the break-even levels needed to match the risk-reducing effect of safety features, indicating missed pricing opportunities.

- Water Sensor: 6% (Pickles) vs. **22%** (Break-even)
- Roof Type 3: 7% (Pickles) vs. **21%** (Break-even)
- Alarm Type 4: 8% (Pickles) vs. **21%** (Break-even)

By offering discounts far below break-even levels, the company ends up overpricing its safest customers. Aligning discounts with actual risk reduction would support customer acquisition while maintaining overall profitability.

![Base Rate Offset](https://github.com/annievu22/Homeowner_Pricing_Analysis_Project/blob/main/Homeowner%20Pricing%20Project%20-%20Key%20Findings/Finding%203.png)

## 5.4. Final Discount Recommendations:

* **Water Sensors – 19% Discount (Factor 0.81):**  
  Affordable and widely adoptable, water sensors reduce water-related claims by up to 40%. The proposed 19% discount is above break-even and encourages adoption among cost-conscious homeowners.

* **Alarm Systems:**  
  - **Local Alarm (Type 2) – 21% Discount (Factor 0.79):**  
    Designed for price-sensitive customers, this discount exceeds the market average and supports switching behavior based on savings.
  - **High-Tech Local Alarm (Type 3) – 15% Discount (Factor 0.85):**  
    Attracts customers who seek a balance of value and service, with moderate price sensitivity and strong retention.
  - **Monitored High-Tech Alarm (Type 4) – 15% Discount (Factor 0.85):**  
    Targets higher-income, low-churn segments that prioritize reliability over aggressive pricing, preserving profit margins.

* **Roof Types:**  
  - **Hail-Resistant Shingles (Type 2) – 17% Discount (Factor 0.83):**  
    Popular in hail-prone regions, this feature significantly lowers risk and appeals to homeowners investing in durable roofing.
  - **Solar Panel Roofs (Type 3) – 12% Discount (Factor 0.88):**  
    Supports sustainable, long-term homeowners who are typically low-risk and retention-friendly, just below the 13% market average.

* **Base Rate Offset – 1.099 (9.9% Increase):**  
  Ensures revenue neutrality across the portfolio while enabling the implementation of updated risk-aligned discounts.

![Final Discount Summary](https://github.com/annievu22/Homeowner_Pricing_Analysis_Project/blob/main/Homeowner%20Pricing%20Project%20-%20Key%20Findings/Final%20Results.png)

These discount factors were carefully chosen to attract profitable customer segments, reduce churn, and maintain pricing sustainability while remaining competitive in the homeowner insurance space.

---

## 6. Final Conclusion

This project showcases how Excel can serve as a powerful tool for actuarial pricing analysis, allowing analysts to develop credible, market-aligned discount recommendations without requiring advanced programming or external software. Through credibility weighting, competitor benchmarking, and break-even modeling, we designed a pricing structure that aligns with customer risk and enhances market competitiveness.

**Key Takeaways:**

- Loss ratio credibility improves discount accuracy and reduces the impact of low-claim-volume noise
- Competitor benchmarking highlights strategic gaps and ensures pricing decisions are market-relevant
- Breakeven discount analysis supports sustainable premium reduction for low-risk policyholders

**Future Enhancements:**

- Integrate time series data or inflation adjustments to track evolving claim trends
- Add dynamic dashboards to improve stakeholder communication and scenario testing
- Expand the model to include geographic and demographic segmentation for more refined targeting

Overall, this project reflects practical actuarial thinking and the ability to derive strategic pricing recommendations from structured Excel models, strengthening risk-aligned decision-making for homeowner insurance products.
