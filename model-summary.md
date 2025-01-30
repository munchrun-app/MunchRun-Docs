# MunchRun Business Model Summary

**Last Updated:** January 30, 2025

**Status:** Active

**Purpose:** This document provides a comprehensive overview of the MunchRun business model, outlining its key components, revenue streams, cost structure, driver compensation model, and strategies for growth and sustainability.

**Guiding Principles:**

*   **Fairness:** Equitable treatment of drivers and restaurants.
*   **Transparency:** Open communication about fees, algorithms, and business practices.
*   **Sustainability:** Building a financially viable and operationally efficient platform.
*   **Local Focus:** Prioritizing and supporting independent Melbourne restaurants.
*   **Driver Empowerment:** Providing drivers with tools and information to maximize their earnings and control their work.
*   **Community Building:** Fostering a strong and engaged community of customers, drivers, and restaurants.

**Key Features and Strategies:**

## 1. Restaurant Partnerships:

*   **Zero Commission Model:** MunchRun does not charge restaurants any commission on orders.
*   **Transparent Customer-Facing Fee:** A small, clearly displayed "Fair Service Fee" (markup) is added to each menu item. This fee is paid by the customer and covers platform operating costs, driver payments, and marketing.
    *   **Standard Restaurants:** 4.5% fee.
    *   **PRO Restaurants:** 3.5% fee.
    *   **Non-Partnered Restaurants:** 5.5% fee.
    *   **Select Items:** Lower fee (e.g., 50% reduction) on specific high-demand items, negotiated with restaurants.
*   **PRO Subscription:** Restaurants can opt for a PRO subscription ($99/month or $149/month, depending on promotion) to reduce the customer-facing fee to 3.5%, and gain increased visibility and other perks.
*   **One-Time Onboarding Fee:** A $200 onboarding fee for new restaurants covers setup, training, and the provided Android tablet (currently waived as promotional offer).
*   **Large Order Bonus:** For orders over $100, a 1% fee is applied and split equally (33%) between the restaurant, driver, and MunchRun.
*   **Restaurant Control:**
    *   Order Throttling: Restaurants can pause or limit incoming delivery orders.
    *   Driver Blocking: Restaurants can block specific drivers.
    *   Real-Time Adjustments: Restaurants can adjust order ready times and other settings.
    *   POS Integration: Integration with popular restaurant POS systems is planned.

## 2. Driver Compensation:**

*   **Dynamic Pricing:** Delivery fees calculated dynamically based on:
    *   Base Fee: $3.50 - $4.50 (varies by time and demand).
    *   Distance Fee: $0.60 - $0.80/km (beyond an initial radius of 1.5-2 km).
    *   Time Multiplier: Off-Peak (1x), Shoulder (1.1x - 1.2x), Peak (1.3x - 1.6x).
    *   Demand Multiplier: Low (1x), Medium (1.05x - 1.15x), High (1.2x - 1.35x).
*   **Hybrid Dynamic Minimum Earnings Guarantee (MEG):**
    *   Tiered system (Newcomer, Bronze, Silver, Gold, Platinum) with varying levels of base hourly guarantee and active time bonus.
    *   **Newcomer:** No base guarantee.
    *   **Bronze:** $10/hour base guarantee + $20/hour active time bonus ($30/hr for active time).
    *   **Silver:** $11/hour base guarantee + $21/hour active time bonus ($32/hr for active time).
    *   **Gold:** $12.50/hour base guarantee + $22.50/hour active time bonus ($35/hr for active time).
    *   **Platinum:** $14/hour base guarantee + $24/hour active time bonus ($38/hr for active time).
    *   **Eligibility:** 80% minimum acceptance rate, plus tier-specific KPIs (Completion Rate, On-Time Delivery, Customer Rating, Hours Online).
    *   **Peak Hours Only:** MEG applies only during designated peak hours (e.g., Lunch 11 AM - 2 PM, Dinner 5 PM - 9 PM).
    *   **Capped MEG Slots:** Limited number of drivers can claim MEG in each zone during peak hours, allocated based on tier and sign-up time.
    *   **Tier Movement:** Upward movement limited to one tier per week; downward movement immediate upon falling below tier requirements at the end of the week.
*   **Wait Time Compensation:** Drivers are compensated for excessive wait times at restaurants: $0.20/min after 5-minute grace period, $0.50/min after 20 minutes (paid by the restaurant).
*   **Efficiency Bonuses:**
    *   $2 bonus for deliveries completed under 30 minutes.
    *   $5 bonus for completing 3 or more deliveries within a 2-hour window.
*   **Large Order Bonus:** Drivers receive 33% of a 1% fee on orders over $100.
*   **100% of Tips:** Drivers keep all customer tips.
*   **Driver Pay Source:** Driver pay (delivery fees, bonuses) comes directly from the customer-paid delivery fees. MunchRun's revenue (from the "Fair Service Fee") is *not* used to pay drivers directly, except when a driver's earnings fall below the MEG threshold for their tier. In those cases, MunchRun provides a top-up to meet the guarantee.

## 3. Driver Order Assignment Algorithm:**

*   **Prioritization:** Platinum > Gold > Silver > Bronze > Newcomer (only if meeting real-time KPI thresholds).
*   **Within Tier:**
    1.  Shortest idle time (drivers waiting longest).
    2.  Closest proximity to the restaurant.
*   **Platinum Exclusive Window:** 30-second exclusive window for available and eligible Platinum drivers to accept orders before they are offered to lower tiers.
*   **Dynamic Radius Adjustment:** Initial search radius expands based on demand and driver availability (smaller radius for high demand, larger for low demand).
*   **Tier Skipping:** If no drivers from a higher tier are available, online, meet the real-time KPI requirements, or accept the order within their exclusive window (if applicable), the algorithm will immediately proceed to the next eligible tier.
*   **Tier Relaxation:** Real-time KPI checks for lower tiers may be temporarily relaxed if no higher-tier drivers are available or accepting orders.

## 4. Driver Unassignment Policy:**

*   **Driver-Initiated:** Drivers can unassign orders before pickup through the app, but it impacts their acceptance rate.
*   **Frequency Limits:** Limits on unassignments per day/week (e.g., 1-2 without penalty beyond acceptance rate impact).
*   **Reasons Required:** Drivers must select a reason for unassigning (e.g., long wait time, order too large, personal emergency).
*   **Post-Pickup:** Unassignment disabled after pickup confirmation (tied to geofencing and restaurant confirmation).
*   **Wait Time:** Unassignment allowed without penalty after waiting for longer than the designated wait time limit, so long as the driver has notified the restaurant of the delay.

## 5.  Fraud Prevention:

*   **Driver Side:**
    *   GPS tracking and verification for wait time claims.
    *   Mandatory photo proof for "Leave at Door" deliveries.
    *   Geofencing to confirm restaurant arrival and order pickup.
    *   Monitoring for patterns of excessive unassignments, late deliveries, or unusual routes.
    *   Detection of GPS spoofing and other fraudulent activities.
*   **Customer Side:**
    *   Monitoring for frequent claims of non-delivery or missing items.
    *   Requiring photo proof from drivers for "Leave at Door" deliveries.
    *   Secure payment gateway with fraud prevention measures.
*   **Restaurant Side:**
    *   Auditing menu prices to prevent artificial inflation.
    *   Monitoring for fake orders or manipulation of driver wait times.

## 6. Customer Communication:**

*   **Transparent Fees:** Clearly display the "Fair Service Fee" (markup) to customers during checkout, with an explanation of its purpose:
    > "This small fee helps us pay drivers fairly, operate the platform, and ensure restaurants receive 100% of their listed menu price. Unlike other apps, we don't allow hidden markups or charge restaurants hefty commissions."
*   **Dine-in Price Comparison:** Show the restaurant's dine-in price alongside the MunchRun price to highlight the absence of hidden markups.
*   **"PRO Restaurant" Badge:** Highlight restaurants with PRO subscriptions and lower markups with a special badge.
*   **In-App Messaging:** Provide clear and timely updates to customers about order status, driver assignment, and any potential delays.
*   **Feedback Mechanisms:** Encourage customers to rate drivers and restaurants and provide feedback on their delivery experience.

## 7. Pre-Volume Financial Strategies:**

*   **"Support Local" Fee:** 2% customer opt-out fee (with clear ethical messaging) to generate revenue.
*   **Restaurant Subsidies:** Offer free onboarding to early adopters who promote MunchRun.
*   **Weekend "Surge" Markup:** 1% weekend markup (transparently communicated as a "Weekend Local Support Fee").
*   **Hyper-Local Launch:** Focus on a single, dense area like Fitzroy or Carlton for initial launch.
*   **"Feed Your Team" Campaign:** Target offices for pre-ordered group lunches, offering discounts for bulk orders.
*   **Driver Deposit System:** Refundable $50 deposit for drivers to access the platform (waived after 50 deliveries). This also covers the cost of the thermal bag.
*   **Sponsorships:** Seek sponsorships from ethical brands for in-app promotions.
*   **Cap Guaranteed Hours:** Limit the number of drivers who can claim the MEG during peak hours.
*   **Prepaid Credits:** Offer bonus credits for customers who prepay (e.g., 20% bonus).
*   **Negotiate Deferred Payments:** With tech partners like POS integrators.
*   **"Crisis Mode" Contingency:** Transparent plan to temporarily suspend MEG if necessary, with retroactive repayment once financially stable.

## 8. Technology Stack:

*   **Backend:** Node.js with Express.js or Python with Django/Flask.
*   **Database:** PostgreSQL or MySQL.
*   **Cloud:** AWS, Google Cloud, or Azure.
*   **Customer App:** React Native or Flutter.
*   **Driver App:** React Native or Flutter.
*   **Restaurant Dashboard:** React or Vue.js.
*   **Real-time:** Socket.IO or Firebase.
*   **Payments:** Stripe or PayPal.
*   **Mapping:** Google Maps Platform or Mapbox.
*   **Push Notifications:** Firebase Cloud Messaging (FCM) or Apple Push Notification Service (APNs).
*   **SMS:** Twilio or Nexmo.
*   **Email:** SendGrid, Mailgun, or Amazon SES.
*   **Analytics:** Google Analytics or Firebase Analytics.

**Revenue Model:**

1.  **Customer-Facing "Fair Service Fee" (Markup):**
    *   **Standard Restaurants:** 4.5% fee added to each menu item.
    *   **PRO Restaurants:** 3.5% fee added to each menu item.
    *   **Non-Partnered Restaurants:** 5.5% fee added to each menu item.
    *   **Select Items:** Lower fee (e.g., 50% reduction) on specific high-demand items, negotiated with restaurants.
    *   **Transparency:** Clearly displayed to customers as a "Fair Service Fee" with a tooltip explaining that it replaces the high commissions charged by other platforms, allowing restaurants to keep 100% of their listed menu price. Also, that it covers operating costs and driver pay including the MEG.

2.  **Restaurant PRO Subscription:**
    *   $99-$149/month subscription fee for restaurants (depending on promotions).
    *   **Benefits:** Reduced customer-facing markup (3.5%), increased visibility in the app, potential marketing support.

3.  **Large Order Fee:**
    *   1% fee on orders over $100.
    *   Split equally (33%) between the restaurant, driver, and MunchRun.

4.  **Restaurant Onboarding Fee:**
    *   One-time $200 fee for new restaurants (currently waived).
    *   Covers setup, training, and the provided Android tablet.

5.  **"Support Local" Fee (Opt-Out):**
    *   2% fee added to each order, presented to customers as an optional way to support local businesses and drivers.
    *   Ethically designed with clear messaging and an easy opt-out option.

6.  **Weekend "Surge" Markup:**
    *   1% markup added to orders on Fridays, Saturdays, and Sundays.
    *   Transparently communicated to customers as a "Weekend Local Support Fee."

7.  **Advertising Packages (Future):**
    *   Tiered advertising packages for restaurants to boost their visibility within the app.

**Financial Projections (Illustrative - First 12 Months):**

*   **Assumptions:**
    *   Month 1-6: 50 restaurants, 10 orders/day/restaurant, $40 average order value, 100 drivers.
    *   Month 7-12: 100 restaurants, 15 orders/day/restaurant, $40 average order value, 200 drivers.
    *   Blended "Fair Service Fee": 4.4% (mix of Standard, PRO, and Non-Partnered).
    *   PRO adoption: 10% of restaurants.
    *   "Support Local" fee opt-in rate: 70%.
    *   MEG utilization: 20% of driver hours during peak periods.
    *   Average driver active time: 50% during peak hours.

| Metric                     | Launch Phase (Monthly Avg. - Months 1-6) | Growth Phase (Monthly Avg. - Months 7-12) |
| -------------------------- | ---------------------------------------- | ------------------------------------------ |
| **Gross Merchandise Value (GMV)** | $600,000                                 | $1,800,000                               |
| **Revenue Streams:**       |                                          |                                            |
| - Fair Service Fee (4.4%) | $26,400                                 | $79,200                                   |
| - PRO Subscriptions        | $495                                    | $990                                      |
| - Large Order Fee (MunchRun Share) | $600                                | $1800                                    |
| - Support Local Fee (70% opt-in) | $8,400                               | $25,200                                  |
| - Weekend Surge (1%)       | $2,100                                 | $6,300                                   |
| - Onboarding Fees          | $0 (Waived initially)                    | $0 (Waived initially)                      |
| **Total Revenue**          | **$37,995**                              | **$113,490**                               |
| **Expenses:**             |                                          |                                            |
| - Driver Pay (Delivery Fees) |  $54,000                               | $162,000                                  |
| - Driver Pay (MEG Top-Ups) | $2,000 (estimated)                       | $6,000 (estimated)                         |
| - Driver Pay (Bonuses)     | $12,000                                 | $36,000                                  |
| - Restaurant Payout (Large Order Share) | $200                            | $600                                   |
| - Technology (Cloud, APIs) | $5,000                                  | $5,000                                    |
| - Staff (Lean Team)        | $40,000                                 | $40,000                                   |
| - Payment Processing (2.9% + $0.30/order) | $8,700                            | $26,100                                  |
| - Marketing                | $10,000                                 | $10,000                                   |
| - Other Expenses           | $5,000                                  | $5,000                                    |
| **Total Expenses**         | **$136,900**                              | **$290,700**                               |
| **Net Profit/Loss**        | **-$98,905**                             | **-$177,210**                              |

**Key Observations:**

*   **Early Stage Losses:** The financial projections indicate that MunchRun will likely experience losses in the early stages, particularly before achieving significant order volume. This highlights the need for careful cost management and potentially seeking external funding.
*   **Importance of "Support Local" Fee:** The "Support Local" fee, even at a modest 2% with a 70% opt-in rate, contributes significantly to revenue.
*   **Driver Costs:** Driver pay, including delivery fees, MEG top-ups, and bonuses, represents a substantial portion of expenses.
*   **Hybrid MEG Impact:** The hybrid MEG, with its lower base guarantee and focus on active time bonuses, helps to mitigate costs compared to a pure total time guarantee.
*   **Path to Profitability:**  The model demonstrates a path to profitability as order volume increases and fixed costs are spread across a larger revenue base
