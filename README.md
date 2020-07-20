# demote.0.01
demote version 0.01

Project Goals
1. Column definitions and variable statements
2. Normalize instance usage, cost, and get an average cost per instance family hour by region
3. Cascade the average cost per instance hour to calculate a normalized cost for EC2, total cost by account
4. Put total cost into QuickSight and create a standard view for daily cost updates
5. Key Metric calculations: Coverage, Utilization, Total effective discount rate.

Documentation:
1. 01_demote is to create the data table that is referenced from all other queries.  This dataset will be set as 'demote_cust_0.01' in this definition 'cust' will be a unique identifier for the customer held as the customer secret key.  For our variable definitions it will be 'regan'.
2. 02_demote is to get the average cost per ec2 instance hour and effectively allocate the expense to the accounts where the expense was incurred.  








Queries:
0. demote_customer_ingest what the customer's data is stored as in their account
1. demote_regan_01 is bringing in the c&u report from the customer's s3 account
2. demote_regan_02 - query to calculate three different columns:
    - total cost per instance family by region, family, usage types (regan_ec2_cost)
    - normalized usage (regan_normalized_usage)
    - average cost per normalized instance hour (regan_avg_ec2_cost)
3.
