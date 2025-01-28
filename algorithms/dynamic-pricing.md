# MunchRun Dynamic Pricing Algorithm

## Overview

MunchRun uses a dynamic pricing algorithm to calculate delivery fees for customers. This algorithm adjusts prices in real-time based on a variety of factors to ensure fair compensation for drivers, incentivize driver availability during peak periods, and remain competitive within the Melbourne food delivery market.

## Goals

*   **Fair Driver Compensation:** Ensure drivers are adequately compensated for their time and effort, especially during high-demand periods.
*   **Competitive Customer Pricing:** Offer delivery fees that are attractive and competitive within the market.
*   **Demand Management:**  Use pricing to balance supply and demand, encouraging more drivers to be online during peak times.
*   **Transparency:**  Provide clear and transparent pricing to both customers and drivers.

## Factors Affecting Delivery Fee

The delivery fee presented to the customer is calculated using the following components:

1.  **Base Fee:**
    *   A fixed starting fee for each delivery.
    *   Range: $3.50 - $4.50.
    *   The base fee may vary slightly depending on the time of day and overall demand.

2.  **Distance-Based Fee:**
    *   Calculated per kilometer (km) for the distance traveled beyond an initial radius from the restaurant.
    *   Initial Radius: 1.5 km or 2 km (configurable). No charge is applied within this radius.
    *   Rate: $0.60 - $0.80/km (configurable).
    *   Distance Calculation: The distance is calculated as the most efficient driving route between the restaurant and the customer's location using a mapping service API (e.g., Google Maps Distance Matrix API, Mapbox Directions API).

3.  **Time Multiplier:**
    *   A multiplier applied based on the time of day to account for predictable variations in demand and traffic.
    *   **Off-Peak:** 1x (no multiplier) - Typically weekdays outside of lunch and dinner rush.
    *   **Shoulder:** 1.1x - 1.2x -  Transition periods before and after peak hours (e.g., late morning, mid-afternoon).
    *   **Peak:** 1.3x - 1.6x -  High-demand periods, such as lunch and dinner rush hours on weekdays and weekends.
    *   These multipliers and the exact time ranges for each period will be adjusted based on data analysis and observed demand patterns.

4.  **Demand Multiplier:**
    *   A multiplier applied based on real-time demand and driver availability in a specific area.
    *   **Low Demand:** 1x (no multiplier)
    *   **Medium Demand:** 1.05x - 1.15x
    *   **High Demand:** 1.2x - 1.35x (or higher in exceptional circumstances, such as major events or extreme weather)
    *   The demand multiplier is calculated dynamically based on factors such as the number of active orders, the number of available drivers, and the order volume in a particular geographic zone.

**Formula:**

```
Delivery Fee = Base Fee + (Distance-Based Fee * (Distance - Initial Radius)) * Time Multiplier * Demand Multiplier
```

**Example Calculation:**

Let's say a customer places an order:

*   **Base Fee:** $4.00
*   **Distance:** 6 km
*   **Initial Radius:** 2 km
*   **Distance-Based Fee:** $0.70/km
*   **Time Multiplier:** 1.4x (Peak)
*   **Demand Multiplier:** 1.1x (Medium Demand)

**Calculation:**

```
Delivery Fee = $4.00 + ($0.70/km * (6 km - 2 km)) * 1.4 * 1.1
             = $4.00 + ($0.70/km * 4 km) * 1.4 * 1.1
             = $4.00 + $2.80 * 1.4 * 1.1
             = $4.00 + $4.31
             = $8.31
```

**Transparency:**

*   **Customer App:** The customer app will clearly display the breakdown of the delivery fee, showing the base fee, distance-based fee, and any applicable multipliers before the customer confirms the order.
*   **Driver App:** Drivers will see the estimated earnings for each order, including the breakdown of the delivery fee components, before accepting the order.

## Data Used for Dynamic Pricing

The dynamic pricing algorithm uses the following data:

*   **Real-time Data:**
    *   Number of active orders
    *   Number of available drivers (by tier and location)
    *   Driver locations (latitude, longitude)
    *   Order locations (restaurant and customer)
    *   Time of day
    *   Day of the week
    *   Traffic conditions (from mapping service API)
    *   Special events (festivals, holidays, etc.)
    *   Weather conditions

*   **Historical Data:**
    *   Order volume patterns
    *   Driver availability patterns
    *   Delivery times
    *   Impact of past price adjustments

## Algorithm Adjustments and Optimization

*   The dynamic pricing algorithm will be continuously monitored and adjusted to optimize for:
    *   Driver earnings
    *   Customer prices
    *   Order fulfillment rates
    *   Delivery times
*   A/B testing will be used to evaluate the effectiveness of different parameter values and algorithm variations.
*   Machine learning models may be incorporated in the future to improve demand prediction and pricing accuracy.

## Implementation Details

*   The dynamic pricing algorithm will be implemented as a core component of the MunchRun backend system.
*   It will interact with other modules, such as the order management system, driver management system, and the mapping service API.
*   The algorithm will be designed to be scalable and efficient, capable of handling a large volume of orders and real-time data updates.

