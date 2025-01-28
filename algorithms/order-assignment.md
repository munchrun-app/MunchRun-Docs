# MunchRun Order Assignment Algorithm
## Overview

This document outlines the algorithm used by MunchRun to assign delivery orders to drivers. The primary goals of this algorithm are to:

*   **Prioritize Platinum Tier Drivers:** Reward top-performing drivers by giving them preferential access to orders.
*   **Minimize Driver Idle Time:**  Ensure that drivers are actively engaged and earning.
*   **Ensure Fast Delivery Times:**  Match orders with drivers who can deliver them efficiently.
*   **Fair Distribution of Orders:** Distribute orders fairly among drivers, taking into account performance and availability.

## Algorithm Logic

The algorithm follows these steps when a new order is received:

### 1. Order Request Received

When a customer places a new order, the system gathers the following information:

*   **Restaurant Location:** Latitude and longitude of the restaurant.
*   **Customer Location:** Latitude and longitude of the customer's delivery address.
*   **Order Size:** Estimated weight and/or volume of the order (for vehicle type matching).
*   **Order Value:** Total value of the order (for large order bonus calculation).
*   **Time of Order:** Timestamp when the order was placed.

### 2. Filter Eligible Drivers

The algorithm first filters the pool of available drivers based on the following criteria:

*   **Online and Available:** Only drivers who are currently logged into the app and marked as "available" are considered.
*   **Vehicle Type Match:** If applicable, the driver's vehicle type must be suitable for the order size (e.g., large orders might require a car).
*   **Geographic Radius:**  Drivers within an initial radius around the restaurant are considered. This radius is dynamically adjusted based on:
    *   **Driver Availability:**  A larger radius is used if there are few available drivers.
    *   **Demand:** A smaller radius is used during periods of high demand to prioritize speed.
    *   **Driver Tier:** Platinum drivers might have a slightly larger initial radius during periods of low demand.

### 3. Prioritize Drivers Based on Tier and Performance

Drivers are prioritized based on their tier and real-time performance metrics:

#### a. Platinum Tier Drivers

*   **Highest Priority:** Platinum drivers who meet *all* Platinum KPI thresholds *at the time of the order assignment* are given the highest priority.
*   **Real-time KPI Check:** The system verifies that the driver is currently meeting the minimum requirements for acceptance rate, completion rate, on-time delivery rate, and customer rating.
*   **Prioritization within Platinum:** If multiple Platinum drivers are eligible, they are prioritized based on:
    1.  **Shortest Idle Time:** The driver who has been waiting for an order the longest is prioritized.
    2.  **Proximity to Restaurant:** If idle times are similar, the driver closest to the restaurant is prioritized.
*   **Exclusive Offer Window:** Platinum drivers receive a short, exclusive window (e.g., 15-30 seconds) to accept the order before it's offered to lower tiers.

#### b. Gold Tier Drivers

*   If no Platinum drivers are available or all decline the offer, the algorithm moves to Gold tier drivers.
*   **Real-time KPI Check:**  Drivers must be meeting all Gold tier KPI thresholds at the time of assignment.
*   **Prioritization within Gold:** Similar to Platinum, drivers are prioritized based on shortest idle time and then proximity to the restaurant.

#### c. Silver, Bronze, and Newcomer Tiers

*   The algorithm continues down the tiers (Silver, Bronze, then Newcomer) if no drivers in the higher tiers are available or accept the order.
*   The same prioritization logic (idle time, then proximity) is applied within each tier.

#### d. No Tier Drivers

*   As a last resort, drivers who are not yet in a tier or have fallen below Bronze requirements are considered.
*   They are prioritized based on idle time and then proximity to the restaurant.

### 4. Offer the Order

*   **Sequential Offering:** The order is offered to the highest-priority driver first.
*   **Timeout:** The driver has a short period (e.g., 30-60 seconds) to accept the order.
*   **Rejection/Timeout:** If the driver rejects the order or the timer expires, the algorithm moves to the next driver on the priority list.
*   **Acceptance:** Once a driver accepts the order, it is assigned to them, and they are removed from the pool of available drivers.

### 5. Dynamic Adjustments

The algorithm dynamically adjusts its parameters based on real-time conditions:

*   **Expanding Radius:** If no driver within the initial radius accepts the order within a certain timeframe, the search radius is gradually expanded.
*   **Tier Relaxation:**  If no drivers in higher tiers are available or accepting orders, the algorithm might temporarily relax the real-time KPI check for lower tiers to ensure timely order fulfillment. This is done cautiously and with predefined thresholds.
*   **Demand-Based Adjustments:** During periods of very high demand (e.g., peak lunch or dinner rush), the algorithm might further adjust parameters to prioritize speed and efficiency over strict tier adherence. This could involve a larger initial radius or offering orders to multiple drivers simultaneously.

## Factors Considered in the Algorithm

*   **Driver Tier:** Platinum, Gold, Silver, Bronze, Newcomer.
*   **Real-time KPI Metrics:** Acceptance rate, completion rate, on-time delivery rate, customer rating.
*   **Proximity:** Distance between the driver and the restaurant (calculated using the Haversine formula or a similar method).
*   **Idle Time:** Time since the driver's last completed or rejected order.
*   **Availability:** Driver's online/offline status.
*   **Vehicle Type:**  Matching the order size to the appropriate vehicle.
*   **Order Value:** Used to determine eligibility for the large order bonus.

## Pseudocode

```
function assignOrder(order) {
  drivers = getAvailableDrivers(order.restaurantLocation, order.vehicleType);

  if (drivers.length > 0) {
    // Adjust radius based on demand and driver availability
    radius = calculateInitialRadius(order, drivers);

    platinumDrivers = filterDriversByTierAndKPIs(drivers, "Platinum", radius);
    if (platinumDrivers.length > 0) {
      bestDriver = findMostIdleAndClosestDriver(platinumDrivers, order.restaurantLocation);
      offerOrder(bestDriver, order, 30); // 30-second exclusive window
      return;
    }

    goldDrivers = filterDriversByTierAndKPIs(drivers, "Gold", radius);
    if (goldDrivers.length > 0) {
      bestDriver = findMostIdleAndClosestDriver(goldDrivers, order.restaurantLocation);
      offerOrder(bestDriver, order);
      return;
    }
    // ... (Repeat for Silver, Bronze, Newcomer)
  }

  // No suitable driver found within the initial radius
  expandSearchRadius();
  if (noDriverFound)
  {
    relaxTierRequirements();
  }
}

function filterDriversByTierAndKPIs(drivers, tier, radius) {
  // Filter drivers by tier, check if they meet all KPIs in real-time, and are within radius
  return drivers.filter(driver => driver.tier === tier && driver.meetsKPIs(tier) && isWithinRadius(driver.location, order.restaurantLocation, radius));
}

function findMostIdleAndClosestDriver(drivers, location) {
  // Sort drivers by idle time (descending) and then by distance to location (ascending)
  drivers.sort((a, b) => {
    if (a.idleTime !== b.idleTime) {
      return b.idleTime - a.idleTime; // Prioritize most idle
    }
    distanceA = calculateDistance(a.location, location);
    distanceB = calculateDistance(b.location, location);
    return distanceA - distanceB; 
  });
  return drivers[0];
}

function offerOrder(driver, order, timeout = 60) {
  // Send order offer to driver with an optional timeout (default 60 seconds)
  // ...
}

function calculateInitialRadius(order, drivers){
    // Adjust radius based on demand and driver availability
}

function isWithinRadius(driverLocation, restaurantLocation, radius){
    // Check if driver is within radius of restaurant
}

function calculateDistance(location1, location2){
    // Calculate distance between two locations using Haversine formula or similar
}
```

## Future Improvements

*   **Predictive Dispatching:** Implement machine learning models to predict future demand and pre-emptively assign orders to drivers.
*   **Order Batching:** Optimize order batching to group orders from nearby restaurants or with close delivery locations, improving efficiency and reducing driver mileage.
*   **Automated Anomaly Detection:**  Use machine learning to detect unusual patterns in driver behavior that might indicate fraud or attempts to game the system.

## Transparency

We are committed to transparency in our algorithm. Drivers will have access to information about how the algorithm works and the factors that influence order assignment through the driver app and the Driver Onboarding Guide.

## Conclusion

This document provides a detailed overview of the MunchRun order assignment algorithm. The algorithm is designed to be dynamic and adaptable, and it will be continuously monitored and improved based on real-world data and feedback from drivers, restaurants, and customers. By prioritizing Platinum drivers, minimizing idle time, and ensuring fair distribution of orders, we aim to create a food delivery platform that is both efficient and equitable.
