# Platform quickstart

The data platform is an integrated environment build on a modern, scalable and extensible data lakehouse which offers researchers and developers a workplace tailored to:

* data exploration and analysis
* AI and tools development 
* business intelligence, visualization and sharing of data and insights

## Architecture

The platform is mainly composed by the following:
 
* a data lakehouse (Apache Iceberg  + Nessie + S3 storage)
* a query engine for SQL (Trino)
* a dynamic workspace engine (Coder)

Users can access either data directly, via Iceberg or Trino, or leverage a customizable, personal workspace with a Python REPL (Jupyter) to execute custom code.


## Components: Data Lakehouse

The data lakehouse is a scalable, fast and secure platform for large datasets. While individual data chunks are stored as parquet files over an S3 bucket, a logical data **table** is managed as a coeherent, cohesive and consistent representation via Apache Iceberg.
At any time, users can read, export and modify data inside tables preserving ACID requirements, and leverage *point-in-time* consistency to obtain time travel to any snapshot of the table, regardless of the size.

A *catalogue* stores the information about every *table* registered in the platform, with details for :
* name, owner, history
* schema
* ownership

Authorized users can inquire the catalogue to discover *metadata* about tables, and the move to a query engine to read the *content* (ie data).


## Components: Query engines

The data stored in the lakehouse is accessible via query engines which support 2 access models:

* SQL queries
* Programmatic access via client libraries (Python, Scala, Java)

Users can access the same data via any of the supported methods.
See the example notebooks to find out the details.


## Components: Workspaces

The platform supports dynamic workspaces dedicated to users: customizable interactive enviroments to let developers and researchers perform computation with the perimeter of the platform.

While all the data is accessible externally, given the large size of datasets it may be unfeasible to perform computation outside due data transfer costs or because of the time required to download samples. By using a cloud environment, users can directly access data in the lakehouse.


### Quickstart

New users can quickly start exploring and working on datasets by creating a personal environment and then exploring the examples.

Steps:

1. Access the platform and log in
2. Create a workspace by defining a dedicated, personal environment with a fixed set of hardware resources (cpu, ram and disk space)
3. Access the Jupyter instance 

    * via web browser, by clicking the button: zero install, use the browser
    * via local environment: VS Code or PyCharm supported, requires configuration
    * via SSH: install the agent and then launch SSH to connect to the cloud machine

4. Explore the examples to understand how to access the catalogue and datasets


