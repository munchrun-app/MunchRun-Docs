# MunchRun Driver Pay Calculations

## Overview

This document outlines how driver pay is calculated on the MunchRun platform. We believe in fair and transparent compensation for our drivers, and this document provides a detailed breakdown of all the components that contribute to a driver's total earnings.

## Components of Driver Pay

MunchRun driver pay is based on a combination of factors designed to reward drivers for their time, effort, and performance. These include:

1.  **Delivery Fee:**
    *   **Base Fee:** A fixed amount paid for each completed delivery.
    *   **Distance-Based Fee:** Compensation calculated per kilometer driven beyond a set radius from the restaurant.
    *   **Time Multiplier:** A multiplier applied based on the time of day (e.g., Off-Peak, Shoulder, Peak).
    *   **Demand Multiplier:** A multiplier applied based on real-time demand and driver availability in a specific area.

2.  **Hybrid Minimum Earnings Guarantee (MEG):**
    *   A tiered system that guarantees a minimum level of earnings per hour, consisting of a base hourly rate and an active time bonus. **The MEG is applied as a top-up only if a driver's earnings from delivery fees, tips, and other bonuses fall below the guaranteed minimum for their tier.**

3.  **Large Order Bonus:**
    *   An additional bonus paid for delivering orders with a total value exceeding $100.

4.  **Wait Time Compensation:**
    *   Compensation for time spent waiting at restaurants beyond a grace period.

5.  **Tips:**
    *   Drivers receive 100% of tips given by customers.

## 1. Delivery Fee Calculation

The delivery fee for each order is calculated using the following formula:

**Delivery Fee = Base Fee + (Distance-Based Fee \* (Distance - Initial Radius)) \* Time Multiplier \* Demand Multiplier**

**Where:**

*   **Base Fee:** $3.50 - $4.50 (varies based on time of day and demand).
*   **Initial Radius:** 1.5 km or 2 km (no distance charge applied within this radius).
*   **Distance-Based Fee:** $0.60 - $0.80/km (charged for the distance traveled beyond the initial radius).
*   **Distance:** The total driving distance from the restaurant to the customer's location, calculated using the most efficient route.
*   **Time Multiplier:**
    *   Off-Peak: 1x
    *   Shoulder: 1.1x - 1.2x
    *   Peak: 1.3x - 1.6x
*   **Demand Multiplier:**
    *   Low Demand: 1x
    *   Medium Demand: 1.05x - 1.15x
    *   High Demand: 1.2x - 1.35x (or higher in exceptional circumstances)

**Example:**

*   Base Fee: $4.00
*   Distance: 7 km
*   Initial Radius: 2 km
*   Distance-Based Fee: $0.70/km
*   Time Multiplier: 1.4x (Peak)
*   Demand Multiplier: 1.2x (High Demand)

**Calculation:**

```
Delivery Fee = $4.00 + ($0.70/km * (7 km - 2 km)) * 1.4 * 1.2
             = $4.00 + ($0.70/km * 5 km) * 1.4 * 1.2
             = $4.00 + $3.50 * 1.4 * 1.2
             = $4.00 + $5.88
             = $9.88
```

## 2. Hybrid Minimum Earnings Guarantee (MEG)

The MEG ensures drivers earn a minimum amount per hour, based on their performance tier. It consists of two parts:

*   **Base Guarantee:** A minimum hourly rate based on the driver's total online hours, regardless of whether they are on an active delivery.
*   **Active Time Bonus:** An additional amount paid for each hour spent actively engaged in a delivery.

**Active Time** is defined as the period from when a driver accepts an order to when they complete the delivery, including:

*   Travel time to the restaurant.
*   Wait time at the restaurant (after the grace period, and where wait-time compensation applies).
*   Travel time to the customer.
*   Time spent at the customer's location to complete the delivery.

**MEG Tiers:**

| Tier      | Acceptance Rate | Completion Rate | On-Time Delivery Rate | Customer Rating | Minimum Hours Online (per week) | Base Guarantee | Active Time Bonus | Total Hourly Guarantee (Active Time) |
| --------- | --------------- | --------------- | --------------------- | --------------- | ------------------------------- | --------------- | ----------------- | --------------------------------- |
| Newcomer  | N/A             | N/A             | N/A                  | N/A             | N/A                             | N/A             | N/A              | N/A                               |
| Bronze    | Minimum 80%     | Minimum 90%     | Minimum 80%          | Minimum 4.5     | Minimum 20                      | $10/hour        | $20/hour          | $30/hour (active)                 |
| Silver    | Minimum 80%     | Minimum 95%     | Minimum 85%          | Minimum 4.7     | Minimum 25                      | $11/hour        | $21/hour          | $32/hour (active)                 |
| Gold      | Minimum 85%     | Minimum 97%     | Minimum 90%          | Minimum 4.8     | Minimum 30                      | $12.5/hour      | $22.5/hour        | $35/hour (active)                 |
| Platinum  | Minimum 90%     | Minimum 99%     | Minimum 95%          | Minimum 4.9     | Minimum 35                      | $14/hour        | $24/hour          | $38/hour (active)                 |

**MEG Calculation:**

The MEG top-up is calculated at the end of each week (or a shorter period, if applicable) using the following formula:

**MEG Top-Up = (Base Guarantee \* Total Online Hours) + (Active Time Bonus \* Active Time Hours) - (Actual Earnings)**

Where:

*   **Base Guarantee:** The driver's tier's hourly base guarantee rate.
*   **Total Online Hours:** The total number of hours the driver was logged into the app and available to receive orders during the period.
*   **Active Time Bonus:** The driver's tier's hourly active time bonus rate.
*   **Active Time Hours:** The total number of hours the driver spent actively engaged in deliveries during the period.
*   **Actual Earnings:** The driver's total earnings from delivery fees, tips, large order bonus, and wait time compensation during the period.

**Important:**

*   **The MEG is a top-up, not an addition.**  If a driver's **Actual Earnings** from delivery fees, tips, and bonuses are **greater than or equal to the calculated Total MEG** (Base Guarantee + Active Time Bonus), they will receive their **Actual Earnings**, and **no top-up is applied.**
*   **The MEG is only applied if Actual Earnings are less than the Total MEG.** In this case, the driver receives a top-up to bring their earnings up to the guaranteed minimum for their tier.

**Example Scenarios:**

**Scenario 1: Busy Period (Gold Tier)**

*   Driver Tier: Gold
*   Online Hours: 40 hours
*   Active Time: 30 hours
*   Delivery Earnings (fees, tips, bonuses): $1250
*   Wait Time Compensation: $50

**Calculations:**

*   Base Guarantee: $12.50/hour \* 40 hours = $500
*   Active Time Bonus: $22.50/hour \* 30 hours = $675
*   Total MEG: $500 + $675 = $1175
*   Actual Earnings: $1250 + $50 = $1300

**Result:** The driver's Actual Earnings ($1300) are **greater** than the Total MEG ($1175). **No top-up is applied.**

**Total Payout:** $1300 (Actual Earnings)

**Scenario 2: Slow Period (Bronze Tier)**

*   Driver Tier: Bronze
*   Online Hours: 25 hours
*   Active Time: 5 hours
*   Delivery Earnings: $60
*   Tips: $15
*   Large Order Bonus: $0
*   Wait Time Compensation: $0

**Calculations:**

*   Base Guarantee: $10/hour \* 25 hours = $250
*   Active Time Bonus: $20/hour \* 5 hours = $100
*   Total MEG: $250 + $100 = $350
*   Actual Earnings: $60 + $15 = $75

**Result:** The driver's Actual Earnings ($75) are **less** than the Total MEG ($350). They receive a top-up.

**Total Payout:** $75 (Actual Earnings) + $275 (MEG Top-Up) = $350

**Scenario 3: Ineligible for MEG (Bronze Tier)**

*   Driver Tier: Bronze
*   Online Hours: 25 hours
*   Active Time: 5 hours
*   Delivery Earnings: $60
*   Tips: $15
    *   Acceptance Rate: 75%

**Calculations:**

*   Base Guarantee: $10/hour \* 25 hours = $250
*   Active Time Bonus: $20/hour \* 5 hours = $100
*   Total MEG: $250 + $100 = $350
*   Actual Earnings: $60 + $15 = $75

**Result:** The driver's acceptance rate is below the minimum 80% requirement. They are **ineligible** for the MEG top-up.

**Total Payout:** $75 (Actual Earnings)

## 3. Large Order Bonus

*   For orders with a total value exceeding $100, a 1% large order fee is applied.
*   Drivers receive 33% of this fee as a bonus.
*   **Example:** For a $150 order, the large order fee is $1.50. The driver receives $0.50 as a bonus.

## 4. Wait Time Compensation

*   Drivers are compensated for excessive wait times at restaurants exceeding a 5-minute grace period.
*   **Compensation Rate:**
    *   $0.20 per minute for minutes 6-20.
    *   $0.50 per minute after 20 minutes.
*   **Maximum Wait Time Compensation:** Capped at 50% of the order value (excluding delivery fee).
*   **Example:** A driver waits 25 minutes for an order with a value of $40.
    *   Compensation: ($0.20/minute \* 15 minutes) + ($0.50/minute \* 5 minutes) = $3.00 + $2.50 = $5.50
    *   Cap: 50% of $40 = $20 (cap is not exceeded in this case).

## 5. Tips

*   Drivers receive 100% of all tips provided by customers through the MunchRun app.
*   Tips are not included in the MEG calculation.

## Payment Schedule

*   Drivers are paid weekly via direct deposit to their nominated bank account.
*   The payment cycle runs from \[Day] to \[Day], and payments are processed on \[Day].
*   Funds typically arrive in driver accounts within \[Number] business days after processing.

## Viewing Earnings

*   Drivers can view a detailed breakdown of their earnings in the MunchRun Driver app.
*   The earnings section shows:
    *   Delivery fees (base fee, distance-based pay, time/demand multipliers)
    *   Tips
    *   Bonuses (Large Order Bonus, Active Time Bonus)
    *   Wait time compensation
    *   MEG top-ups (if applicable)
    *   Historical earnings data

## Important Notes

*   **Taxes:** Drivers are responsible for managing their own tax obligations as independent contractors.
*   **ABN:** All drivers must have a valid Australian Business Number (ABN).
*   **Policy Changes:** MunchRun reserves the right to modify the driver pay structure and MEG calculations. Drivers will be notified of any changes in advance.

## Conclusion

This document provides a comprehensive overview of how driver pay is calculated on the MunchRun platform. We are committed to fair and transparent compensation, and we believe this model rewards drivers for their hard work, dedication, and performance. If you have any questions, please refer to the Driver FAQ in the app, or contact MunchRun Driver Support.
