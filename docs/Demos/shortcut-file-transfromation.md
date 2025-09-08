# Demo 2 - Shortcut File Transformations

This demo showcases how easy it is to create a managed table in Fabric from csv files stored in a shortcut supported source. The emphasis is to showcase the simplicity to create the managed table from the csv files using shortcuts without the need for complex pipelines to do the transformation and how dynamic the process is, in that if the data changes in the external source the managed table is updated automatically.

## Pre-Requisites

1. An Azure Storage Account provisioned on Azure with the following container:

- `prdt-reviews`

1. Upload all the csv files from the [`data/product_reviews/az-storage`](/data/product_reviews/az-storage) folder to the `prdt-reviews` container.

## Steps

1. In the same Fabric workspace, navigate to the `StoreOps_Bronze_LH` lakehouse (continuing from Demo 1). Create a new shortcut for the product review CSV files by right-clicking on the `dbo` schema in the Lakehouse explorer and selecting **New table shortcut**.
1. Select **Azure Blob Storage** as the external source for your shortcut.
1. Choose your existing connection to the Azure Storage Account (or create a new one if needed). Navigate to the `prdt-reviews` container that contains the product review CSV files you previously uploaded (files from [`data/product_reviews/az-storage`](/data/product_reviews/az-storage)) and select **Continue**.
1. Fabric will automatically detect the CSV file format and suggest a transformation from CSV to Delta format. Configure the header setting by selecting "use first row as column headers" and click **Next**.
1. Review the shortcut name (rename if desired) and proceed to create it. This initiates the managed table creation process, which converts and consolidates all CSV files into a single Delta table.
1. Once the process begins, you'll receive a notification prompting you to track the progress. Select **Manage shortcut** from the notification card to monitor the transformation. Wait for the status to show "Success", then refresh the Lakehouse schema to see the new table.
1. Locate the newly created managed table (automatically generated from the shortcut transformation) and run a T-SQL query to preview the data and verify the transformation completed successfully.
1. To demonstrate the automatic synchronization feature, add a new CSV file to the `prdt-reviews` container. Upload the [product_reviews_5.csv](/data/product_reviews/product_reviews_5.csv) file to Azure Blob Storage using either the Azure Portal or Azure Storage Explorer.
1. Return to Fabric, right-click on the shortcut, and select **Manage shortcut** to monitor the process. Observe that Fabric automatically detects the file change and triggers an incremental transformation—no manual refresh, notebooks, or pipelines required.
1. Once the transformation completes successfully, refresh the managed table and verify that the row count has increased (for example, from 411 to 512 rows after adding the new file), confirming that the new data was automatically appended.

Notice that the shortcut-driven transformation keeps the managed table in sync with the container contents—new, changed, or removed CSV files are reflected without additional orchestration.

A complete recording can be found on slide 8 of the [powerpoint presentation](https://aka.ms/AAxubxj).
