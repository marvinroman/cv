---
title: 'Netsuite Record Restructuring'
---

#### Problems
* Customer addresses are not searchable in the system.
* Customers sell homes, how do you transfer a customer's property in the system without altering historical transaction records?
* Can contract and other PDF forms be automatically created?
* How to handle properties that install multiple energy systems but consolidate those stats under a single record?

#### Solution
* Rebuilt record structure to centralize around **Property** record instead of **Customer** record.
* Link back all CRM & Transaction records to the **Property** record.
* Create child **Energy System** records that consolidate onto the **Property** record.
* Build **Utility Data** records that consolidate onto **Energy System** and **Property** records.
* Script up automation for consolidation and propagation of fields across records either in real time or through periodic updates.
* Setup notifications for asynchronous data consolidation completion & prevent browsing from the page until consolidation is complete.
* Automatically validate the address and gather address further address data upon selection on a **Property** record.
* Data migration from old records and automatic creation of new record structure including child records and the links between them.
* Sandbox testing, creating training materials & migration to the production system.

#### Skills used
Suitescript, Javascript, API, ES6, Netsuite Administration, Netsuite Development, ERP / CRM Software