# Power-BI
## Dataflows
Power BI Dataflow is the data transformation component in Power BI. It is a Power Query process that runs in the cloud, independent from Power BI report and dataset, and store the data into CDM: Common Data Model inside Azure Data Lake storage. 
- More consistency between datasets – less chance that different users will make different decisions when preparing data
- Removes the necessity for individual data source prep and provides ETL
![image](https://user-images.githubusercontent.com/67767423/159794214-2866c04a-e7b0-4a17-bd0c-77de926dcc29.png)
![image](https://user-images.githubusercontent.com/67767423/159799292-176ebf70-f154-41d0-b067-aa8266cbe29d.png)
![image](https://user-images.githubusercontent.com/67767423/159799587-5c03c1bf-26a3-414c-afc3-60b0275d5634.png)

## Create a dataflow using linked tables
Creating a dataflow using linked tables enables you to reference an existing table, defined in another dataflow, in a read-only fashion. Some of the reasons you may choose this approach:

- If you want to reuse a table across multiple dataflows, such as a date table or a static lookup table, you should create a table once and then reference it across the other dataflows.

- If you want to avoid creating multiple refreshes to a data source, it's better to use linked tables to store the data and act as a cache. Doing so allows every subsequent consumer to leverage that table, reducing the load to the underlying data source.

- If you need to perform a merge between two tables.
