# MunchRun Customer Pricing

## Overview

This document explains how pricing works for customers on the MunchRun platform. We are committed to transparent pricing and believe in providing a fair and affordable service while supporting local restaurants and ensuring fair compensation for our drivers.

## Pricing Components

The total price you see when ordering through MunchRun consists of the following:

1.  **Menu Prices:** These are the prices set by the restaurant for each food and beverage item.
2.  **Markup:** A small, transparent markup (2-3%) is added to each menu item. This markup is clearly displayed in the app and is collected by MunchRun to cover operational costs, including driver compensation. This allows us to have a zero-commission model for restaurants.
3.  **Delivery Fee:**  This fee covers the cost of delivering your order and is calculated dynamically based on several factors.
4.  **Large Order Fee:** A 1% fee applied to orders with a total value over $100.
5.  **Service Fee:**  MunchRun does not charge a service fee.
6.  **GST:**  Applicable taxes, such as GST, are included in the menu prices.

## Delivery Fee Calculation

The delivery fee is calculated dynamically using the following factors:

**1. Base Fee:**

*   A fixed starting fee for each delivery, typically ranging from $3.50 to $4.50.
*   The base fee may vary slightly depending on the time of day and overall demand.

**2. Distance-Based Fee:**

*   Calculated per kilometer (km) for the distance traveled beyond an initial radius from the restaurant.
*   **Initial Radius:** 1.5 km or 2 km (configurable). No distance charge is applied within this radius.
*   **Rate:** $0.60 - $0.80/km (configurable).
*   **Distance Calculation:** The distance is calculated as the most efficient driving route between the restaurant and your delivery location.

**3. Time Multiplier:**

*   A multiplier applied based on the time of day to account for predictable variations in demand and traffic.
*   **Off-Peak:** 1x (no multiplier) - Typically weekdays outside of lunch and dinner rush.
*   **Shoulder:** 1.1x - 1.2x - Transition periods before and after peak hours (e.g., late morning, mid-afternoon).
*   **Peak:** 1.3x - 1.6x - High-demand periods, such as lunch and dinner rush hours on weekdays and weekends.

**4. Demand Multiplier:**

*   A multiplier applied based on real-time demand and driver availability in your area.
*   **Low Demand:** 1x (no multiplier)
*   **Medium Demand:** 1.05x - 1.15x
*   **High Demand:** 1.2x - 1.35x (or higher in exceptional circumstances)

**Formula:**

```
Delivery Fee = Base Fee + (Distance-Based Fee * (Distance - Initial Radius)) * Time Multiplier * Demand Multiplier
```

**Example:**

*   Base Fee: $4.00
*   Distance: 6 km
*   Initial Radius: 2 km
*   Distance-Based Fee: $0.70/km
*   Time Multiplier: 1.4x (Peak)
*   Demand Multiplier: 1.1x (Medium Demand)

**Calculation:**

```
Delivery Fee = $4.00 + ($0.70/km * (6 km - 2 km)) * 1.4 * 1.1
             = $4.00 + ($0.70/km * 4 km) * 1.4 * 1.1
             = $4.00 + $2.80 * 1.4 * 1.1
             = $4.00 + $4.31
             = $8.31
```

The delivery fee for this order would be $8.31.

## Large Order Fee

*   A 1% fee is applied to orders with a total value over $100 (after the markup is added).
*   This fee is distributed among the restaurant (33%), the driver (33%), and MunchRun (33%).
*   **Example:** For a $120 order, the large order fee is $1.20.

## Transparent Markup

*   MunchRun adds a small markup (2-3%) to each menu item. This markup is clearly displayed next to the item price in the app.
*   The markup allows us to operate without charging commission fees to restaurants, enabling them to keep a larger share of their earnings.
*   It also contributes to ensuring fair driver compensation, including the Minimum Earnings Guarantee.

## No Service Fee

*   Unlike some other food delivery platforms, MunchRun does **not** charge a separate service fee on orders.
*   We believe in transparent pricing, and the markup on menu items allows us to cover our costs without additional service fees.

## Taxes

*   All menu prices displayed on the MunchRun platform are inclusive of GST.

## Payment Methods

*   MunchRun accepts all major credit cards and debit cards.
*   All payments are processed securely through our payment gateway.

## Promotions and Discounts

*   MunchRun may periodically offer promotions and discounts. These will be clearly displayed in the app.
*   Promotional codes can be entered during checkout.

## Tipping

*   You have the option to tip your driver directly through the app after your order is delivered.
*   100% of your tip goes to the driver.

## Refunds and Cancellations

*   Please refer to our [Refund and Cancellation Policy](Link to Refund and Cancellation Policy) for detailed information on how refunds and cancellations are handled.

## Conclusion

MunchRun is committed to providing a transparent and affordable food delivery service that benefits customers, restaurants, and drivers. We believe our pricing model is fair and sustainable, and we are constantly working to improve our platform and provide the best possible experience for our users.