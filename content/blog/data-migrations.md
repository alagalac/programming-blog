---
title: "Data Migrations"
date: 2018-04-25
tags: ["Software Thoughts"]
summary: "Data migrations are one of the most complex and potentially dangerous
operations which can be done in software development."
---

Data migrations are one of the most complex and potentially dangerous operations
which can be done in software development. It is very important to put in the
upfront effort to ensure that they go smoothly.

## The ETL Process

One well established pattern to carry out data migrations is called ETL;
Extract, Transform, and Load.

![etl](/img/etl.png)

## Extract

In the extraction phase the objective is to extract the raw data provided by the
third party into a location where it can be freely manipulated.

Usually this is done by uploading the raw data as strings into a staging table
in a database. The staging table should match the structure of the source
database.

At this point non-contextural data validation should occur. This is validation
to ensure that the data is in the expected shape.

Some common checks to be carried out on the extracted data:

- Does the data within the bounds of any field constraints in the target
database.
- Is the data complete. Are there any fields or records missing?
- Does the data extracted match the data sent by the third party?

## Transform

In the transformation phase the data is transformed from the extraction staging
tables into transformed staging tables. The transformed staging tables should
match the data structures in the target database.

Some common transformations include:

- Cleaning up any junk data.
- Filtering out any unnecessary data.
- Calculating any required figures.
- Generating any surrogate keys.
- Joining and Splitting data between tables.

At this point contextual data validation can occur. This is validation to ensure
that the data complies with the relevant business rules, and that it will
integrate with the existing data. It should be checked that no foreign key
constraints will be violated.

## Load

In the load phase, the data is loaded from the transformation staging tables to
the target database.

As a part of this stage it is important to have a robust reconciliation process
in place. This process should be able to compare the extracted data to the
loaded data ad pick up any differences. It should be automated.