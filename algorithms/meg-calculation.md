# MunchRun Minimum Earnings Guarantee (MEG) Calculation

## Overview

This document explains how the Minimum Earnings Guarantee (MEG) is calculated for MunchRun drivers. The MEG is designed to provide drivers with a safety net, ensuring they earn a minimum amount per hour while actively delivering on the platform. It also incentivizes high performance through a tiered system and bonuses for active delivery time.

## Goals

*   **Provide a Safety Net:** Guarantee a minimum level of income for drivers, especially during slow periods.
*   **Reward Performance:** Incentivize drivers to maintain high acceptance rates, completion rates, on-time delivery rates, and customer ratings.
*   **Encourage Efficiency:**  Promote efficient order completion through active time bonuses.
*   **Attract and Retain Drivers:** Offer a competitive and attractive earnings structure.

## Hybrid MEG Structure

MunchRun uses a hybrid MEG model that combines two components:

1.  **Base Guarantee:** A minimum hourly rate based on the driver's total online hours, regardless of whether they are on an active delivery.
2.  **Active Time Bonus:** An additional bonus paid for each hour spent actively engaged in a delivery.

**Active Time** is defined as the period from when a driver accepts an order to when they complete the delivery, including:

*   Travel time to the restaurant.
*   Wait time at the restaurant (after the grace period, and where wait-time compensation applies).
*   Travel time to the customer.
*   Time spent at the customer's location to complete the delivery.

## Tiers and Requirements

The MEG is structured in tiers, with each tier offering a different base guarantee and active time bonus. Drivers are assigned to a tier based on their weekly performance.

| Tier      | Acceptance Rate | Completion Rate | On-Time Delivery Rate | Customer Rating | Minimum Hours Online (per week) | Base Guarantee | Active Time Bonus | Total Hourly Guarantee (Active Time) |
| --------- | --------------- | --------------- | --------------------- | --------------- | ------------------------------- | --------------- | ----------------- | --------------------------------- |
| Newcomer  | N/A             | N/A             | N/A                  | N/A             | N/A                             | N/A             | N/A              | N/A                               |
| Bronze    | Minimum 80%     | Minimum 90%     | Minimum 80%          | Minimum 4.5     | Minimum 20                      | $10/hour        | $20/hour          | $30/hour (active)                 |
| Silver    | Minimum 80%     | Minimum 95%     | Minimum 85%          | Minimum 4.7     | Minimum 25                      | $11/hour        | $21/hour          | $32/hour (active)                 |
| Gold      | Minimum 85%     | Minimum 97%     | Minimum 90%          | Minimum 4.8     | Minimum 30                      | $12.5/hour      | $22.5/hour        | $35/hour (active)                 |
| Platinum  | Minimum 90%     | Minimum 99%     | Minimum 95%          | Minimum 4.9     | Minimum 35                      | $14/hour        | $24/hour          | $38/hour (active)                 |

**Note:**

*   **Newcomer Tier:** New drivers start in the Newcomer tier and have no minimum earnings guarantee. They can progress to the Bronze tier after meeting the Bronze requirements for one week.
*   **Minimum Acceptance Rate:**  All drivers must maintain a minimum acceptance rate of 80% to be eligible for any tier above Newcomer and the associated MEG.
*   **Tier Movement:** Drivers can move up one tier per week if they meet the requirements for the next tier. They can be moved down immediately at the end of the week if their performance falls below their current tier's requirements.

## Calculation of MEG

The MEG is calculated at the end of each week (or a shorter period, if applicable) using the following formula:

**Total MEG Top-Up = (Base Guarantee \* Total Online Hours) + (Active Time Bonus \* Active Time Hours) - (Actual Earnings)**

Where:

*   **Base Guarantee:** The driver's tier's hourly base guarantee rate.
*   **Total Online Hours:** The total number of hours the driver was logged into the app and available to receive orders during the period.
*   **Active Time Bonus:** The driver's tier's hourly active time bonus rate.
*   **Active Time Hours:** The total number of hours the driver spent actively engaged in deliveries during the period.
*   **Actual Earnings:** The driver's total earnings from delivery fees, tips, large order bonus, and wait time compensation during the period.

**If Actual Earnings are greater than or equal to the Total MEG, the driver receives their Actual Earnings, and no top-up is applied.**

**If Total MEG is greater than Actual Earnings, the driver receives a top-up to bring their earnings up to the Total MEG amount.**

## Example Scenarios

**Scenario 1: Busy Period (Gold Tier)**

*   Driver Tier: Gold
*   Online Hours: 40 hours
*   Active Time: 30 hours
*   Delivery Earnings (fees, tips, bonuses): $1100

**Calculations:**

*   Base Guarantee: $12.50/hour \* 40 hours = $500
*   Active Time Bonus: $22.50/hour \* 30 hours = $675
*   Total MEG: $500 + $675 = $1175
*   Actual Earnings: $1100

**Result:** The driver's actual earnings ($1100) are less than the calculated Total MEG ($1175). They receive their actual earnings plus a top up to their active time guarantee.

**Total Payout:** $1100 (Actual Earnings) + $75 (MEG Top-up) = $1175

**Scenario 2: Slow Period (Bronze Tier)**

*   Driver Tier: Bronze
*   Online Hours: 25 hours
*   Active Time: 5 hours
*   Delivery Earnings (fees, tips, bonuses): $60

**Calculations:**

*   Base Guarantee: $10/hour \* 25 hours = $250
*   Active Time Bonus: $20/hour \* 5 hours = $100
*   Total MEG: $250 + $100 = $350
*   Actual Earnings: $60

**Result:** The driver's actual earnings ($60) are less than the calculated Total MEG ($350). They receive a top-up to reach the guarantee.

**Total Payout:** $60 (Actual Earnings) + $290 (MEG Top-up) = $350

**Scenario 3: Ineligible for MEG (Bronze Tier)**

*   Driver Tier: Bronze
*   Online Hours: 25 hours
*   Active Time: 5 hours
*   Delivery Earnings (fees, tips, bonuses): $60
    *   Acceptance Rate: 75%

**Calculations:**

*   Base Guarantee: $10/hour \* 25 hours = $250
*   Active Time Bonus: $20/hour \* 5 hours = $100
*   Total MEG: $250 + $100 = $350
*   Actual Earnings: $60

**Result:** The driver's acceptance rate is below the minimum 80% requirement. They are **ineligible** for the MEG top-up.

**Total Payout:** $60 (Actual Earnings)

## Tier Movement Examples

**Example 1: Moving Up**

*   A **Newcomer** driver achieves the following in their first week:
    *   Acceptance Rate: 92%
    *   Completion Rate: 98%
    *   On-Time Delivery Rate: 96%
    *   Customer Rating: 4.9
    *   Hours Online: 28 hours
*   They have met the requirements for **Gold**, but they can only move up **one tier at a time**.
*   The driver will be promoted to **Bronze** for the following week.

**Example 2: Moving Down**

*   A **Silver** driver achieves the following in a week:
    *   Acceptance Rate: 85%
    *   Completion Rate: 96%
    *   On-Time Delivery Rate: 83%
    *   Customer Rating: 4.6
    *   Hours Online: 30 hours
*   Their On-Time Delivery Rate and Customer Rating have fallen below the **Silver** requirements.
*   The driver will be moved down to **Bronze** for the following week.

**Example 3: Staying in the Same Tier**

*   A **Gold** driver achieves the following in a week:
    *   Acceptance Rate: 87%
    *   Completion Rate: 98%
    *   On-Time Delivery Rate: 92%
    *   Customer Rating: 4.85
    *   Hours Online: 32 hours
*   They have met the requirements to maintain their **Gold** tier status.
*   The driver will remain in the **Gold** tier for the following week.
