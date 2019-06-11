---
title: "Tesla API Fleet Report"
---
#### Problem
* Tesla's fleet report to its dealers lacked critical information & was too slow in adding new systems.
* Customer's systems would go down without any notification being sent to the dealer or customer.
#### Solution
* Found some rudimentary documentation of Tesla's API endpoints found by fellow developers and some of the specs.
* Found a Git repo with a valid Client Key & Secret to be able to generate valid OAuth requests.
* Created a daily pull for all customer's systems through the API & generate a full fleet report with charge status and system health status.
* Created notifications based on expected charge thresholds or battery status.