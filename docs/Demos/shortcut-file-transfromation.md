# Demo 2 - Shortcut File Transformations

This demo showcases how easy it is to create a managed table in Fabric from csv files stored in a shortcut supported source. The emphasis is to showcase the simplicity to create the managed table from the csv files using shortcuts without the need for complex pipelines to do the transformation and how dynamic the process is, in that if the data changes in the external source the managed table is updated automatically.

## Pre-Requisites

1. An Azure Storage Account provisioned on Azure with the following container:

- `prdt-reviews`

1. Upload all the csv files from the [`data/product_reviews/az-storage`](../data/product_reviews/az-storage) folder to the `prdt-reviews` container.

## Steps

Follow the steps as detailed in the demo video on slide 8