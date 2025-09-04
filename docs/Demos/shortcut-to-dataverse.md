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

1. Inside the `Bronze` folder, you need to have a lakehouse created named `StoreOps_Bronze_LH`. 


## Steps
Follow the steps as detailed in the demo video on slide 6
