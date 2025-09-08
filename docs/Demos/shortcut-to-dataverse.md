# Demo 1 - Shortcut to Dataverse

This demo showcases how easy it is to create a shortcut in OneLake to any of the external sources. The emphasis is on the simplicity and efficiency of the process, allowing users to quickly connect to and utilize data from various platforms without the need for complex configurations or data integration processes.

## Pre-Requisites

1. You need to have set-up Dataverse, with the following tables:

    - Customers (CustomerId, )
    - Employees
    - Stores
    - Facilities

    You will then need import data to these tables from the CSV files ([customers.csv](../data/customers.csv), [employees.csv](../data/employees.csv), [stores.csv](../data/stores.csv), [facilities.csv](../data/facilities.csv)) respectively provided in the [`data`](../data) folder.

1. You need to have a Fabric workspace in which you have two folders: `Bronze` and `Silver`.

1. Inside the `Bronze` folder, you need to have a lakehouse created named `StoreOps_Bronze_LH` with Lakehouse Schema enabled. 

## Steps

1. Open the `StoreOps_Bronze_LH` lakehouse and create a shortcut to the tables you set up in Dataverse. To do this, right click on the `dbo` schema in the Lakehouse and select `New table shortcut`.
1. Select **Dataverse** as your external source.
1. Next, select the connection to Dataverse if you already have an existing connection, if not, create a new connection to Dataverse.
1. Next select the tables we want to create shortcuts for these will be the **Customers**, **Employees**, **Stores**, and **Facilities** tables. Select the checkboxes next to this tables inside the **CDS2** directory. Then select **Next**.
1. Optionally rename the shortcuts before creating the shortcuts then select **Create** to create the shortcuts in the Lakehouse.
1. After a few moments, the shortcuts will be created in the Lakehouse and you will be able to see them in the `dbo` schema.

Notice that the shortcuts created have a small table shortcut icon next to them, indicating that they are shortcuts to external data sources.

A complete recording can be found on slide 6 of the [powerpoint presentation](https://aka.ms/AAxubxj).
