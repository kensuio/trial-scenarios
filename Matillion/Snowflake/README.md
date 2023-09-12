# Data Heroes Quest Scenarios

## Overview
`Data_Heroes_Quest_Scenarios.json` can be imported into a Matillion for Snowflake instance in order to generate 4 common scenarios.

## Prerequisites
- Snowflake Schema for Testing
  * Permissions to Read/Write/Create Tables
- Matillion Project for Testing
  * It is recommended that a dedicated Project be created for this purpose.
  * Default Environment for project should reference the testing schema

## Scenario Descriptions
This section outlines the high-level behavior of each scenario within the Matillion job structure. Each scenario is designed to demonstrate specific features or challenges related to Data Observability and how they can be managed using Kensu.

**Scenario 1: Begin the Data Journey**

This scenario creates and populates Snowflake tables using a series of Matillion jobs. The primary objective is to demonstrate how lineage and metrics are observed within Kensu.

**Scenario 2: NULL Rows not Allowed!**

In this scenario, NULL values are introduced into a column that should not contain NULLs, showcasing the data quality monitoring capabilities of Kensu.

**Scenario 3: Catching Sneaky Schema Changes**

This scenario introduces a schema change to a table and explores its downstream implications, emphasizing the importance of schema management and observability.

**Scenario 4: Stop Rule Breakers in Their Tracks!**

Practice using the Kensu Circuit Breaker to halt job execution when an upstream rule has been violated. This scenario illustrates the real-time monitoring and control features of Kensu.

## Importing Scenario File into Matillion

1. **Save** `Data_Heroes_Quest_Scenarios.json` to a local directory.
2. **Open Matillion**: Log in to your Matillion instance.
3. **Navigate to Project**: Go to the project where you want to create the scenario jobs.
4. **Import File**: 
    - Go to `Project` > `Import`
    - Choose `From File` and select the `Data_Heroes_Quest_Scenarios.json`.
5. **Configuration**: 
    - Go to `Project` > `Manage Environment Variables`
    - Enter Variable values per table below.
6. **Validation**: Open the `Data_Heroes_Quest` job and follow instructions within job note

| Variable Name | Value Description                      | Example                                     |
|--------------|----------------------------------------|---------------------------------------------|
| KENSU_HUB_URL | URL provided for Kensu HUB access      | `https://kt-12345-hub.kensuapp.com/api/v1/` |
| KENSU_HUB_USER | Username provided for Kensu HUB Access | `kensukt12345`                              |
| KENSU_HUB_PASSWORD     | Password provided for HUB Connection   | `blue-brown-bolus-engine-english`           |


## Matillion Jobs created by Import
The Following Matillion Jobs are created within the project that `Data_Heroes_Quest_Scenarios.json` is imported into.
```plaintext
Data_Heroes_Quest  
├── -> Begin the Data Journey  
│   ├── Dynamic Starting Point
│   │   └── Dynamic Orders and Products
│   └── Migrate and Transform
│       └── Dynamic Orders and Products
│           ├── Inventory_Tracking_Data
│           ├── Product_Inventory
│           ├── Inventory_Finance_Calculations
│           └── CATEGORY_IMPACT_MODEL
├── Absent_Customers
│   └── Inventory_Finance_Calculations
├── Mistakes Happen - Schema Change
│   └── Product_Inventory
└── Stop_The_Spread
    └── PRODUCT_IMPACT_MODEL
```

## Snowflake Tables created by Import
The Following Snowflake Tables are created within the default schema, database, Warehouse for the environment of the project that `Data_Heroes_Quest_Scenarios.json` is imported into.
- PRODUCTS
- ORDER_ITEMS
- INVENTORY_EVENTS
- INVOICES
- SHIPPING_RECORDS
- LINE_ITEM_METRICS
- LINE_ITEM_PRODUCT_DATA
- PRODUCT_DRILL_DOWN
- CATEGORY_IMPACT_MODEL
