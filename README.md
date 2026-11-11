# ApexLogix: Logistics Performance Analysis

ApexLogix moves freight across a network of Nigerian hubs. Revenue holds steady month to month, but a large share of shipments still arrive late. This analysis finds out where reliability is lost, who it affects, and what is worth fixing first.

**Period:** January 2024 – December 2025

---

## The Question

Management needed answers to 25 operational questions across service levels, last-mile delivery, customers, drivers, fleet and pricing. The goal was not more reporting. It was to know **where to act**.

## The Approach

1. **Load and validate** the raw tables in PostgreSQL, confirming row counts and keys.
2. **Clean and enrich in SQL** using joins, CTEs and window functions. Every analytical field (transit time, SLA status and so on) is derived in SQL, never added to the source files.
3. **Publish reusable views** for shipment detail, driver scorecards, lane performance and monthly executive metrics.
4. **Model and visualise in Power BI** on top of those views, so the dashboard and the SQL tell the same story.

## How the Dashboard Is Built

Seven pages, each tied to a decision.

| Page | The decision it supports |
|---|---|
| Executive Overview | Is the business on track, and which lanes are hurting it? |
| Service & SLA | Are premium services actually performing better? |
| Last Mile & Attempts | Why do deliveries fail, and are those failures avoidable? |
| Customers | Is lateness concentrated in a few accounts or spread widely? |
| Drivers | Who sets the standard, and who needs support? |
| Fleet | Is the right vehicle doing the right work? |
| Network & Pricing | Does price reflect service, distance and weight? |

## What It Revealed

**Premium service is not delivering premium reliability.**
Express and Same Day perform only marginally better than Economy on time, yet they are priced well above it. Customers are paying for speed the network does not consistently provide.

**Lateness is a network problem, not a lane problem.**
No single lane or customer explains it. Late deliveries are spread across a large part of the customer base, so fixing one account will not move the overall result.

**Most failed deliveries are preventable before the truck leaves.**
Payment issues, unavailable customers, wrong addresses and access problems account for nearly every failure. Damage is the smallest cause. These are confirmation and data problems, not driving problems.

**Reliability depends on the driver.**
There is a wide gap between the strongest and weakest drivers, even on similar work. That points to practice and coaching, not just infrastructure.

**The fleet is unevenly used.**
Bikes are close to fully utilised while heavy trucks sit mostly idle, which suggests the vehicle mix does not match the shipment mix.

**Weight does not drive transit time.**
Heavier parcels do not move noticeably slower, so transit delays come from process and routing rather than load.

**Reliability does not improve with the calendar.**
Monthly on-time performance moves within a narrow band. There is no seasonal recovery to wait for.

## Tools

PostgreSQL · DBeaver · SQL (CTEs, window functions, views) · Power BI · DAX

## Author

**Daniel Joseph Unwujoh**
Data Analyst & Business Intelligence Consultant
