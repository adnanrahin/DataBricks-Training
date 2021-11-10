#### What is Databricks?

Databricks is known as the Data and AI company. It is a Software-As-A-Service company that makes big data and AI easier for organizations to manage,  enabling data-driven innovation in all enterprises. To put it simply, the Databricks Lakehouse Platform empowers everyone on a data science team to work together, in one secure platform, from the minute data is ingested into an organization through when it’s cleaned up, analyzed, and used to inform business decisions. 

##### Data Warehouses
Data warehouses have been powering business intelligence (BI) decisions for around 30 years. Throughout history, data warehouse technologies have evolved in response to changes in the scale and nature of data relevant to decision-makers and the rise of the internet and other technological innovations.

Data warehouses generally follow a set of guidelines to design systems controlling the flow of data used in decision-making. They are designed to optimize data queries, prevent conflicts between concurrently running queries, support structured data, and make the assumption that data entered is unlikely to change with high frequency. 

Because data warehouses originally were developed using on-premises technology to drive BI decisions, they have had some pain points in adapting to the modern data atmosphere. The proliferation of smart devices and web-based commerce has increased both the volume and the variety of data. Data warehouses traditionally rely on proprietary data formats, which do not support video, image, or free text files. This leads to limited support for machine learning workloads. 

Traditional data warehouse technologies force users to invest in enough compute power and storage to handle their peak user traffic. With the exponential growth many companies have seen in their data in recent years, this design can become extremely expensive.

##### Data Lake

Data lakes have only come into widespread use over the last decade, driven by huge increases in the variety and volume of data and powered by technological advances to store and process data cheaply and efficiently. Data lakes are often defined in opposition to data warehouses: while a data warehouse delivers clean, structured data for BI analytics, a data lake allows an organization to permanently and cheaply store data of any nature in any format - in fact, data lakes allow both structured and semi-structured data to be stored alongside unstructured data like video, images, free text, and log files. 

Unlike in data warehouses, data storage and compute are not coupled in data lake design. This has led to several technologies that have evolved around working with data stored in data lakes. Apache Spark, for example, the compute engine used by Databricks, can run analytic queries, extract-transform-load, and machine learning workloads over enormous quantities of data stored in data lakes. 

For all their strengths, data lakes have not eliminated the need for data warehouses. For BI analytics, most companies continue to load the relevant data from their data lake into a data warehouse, and it is here that most analysts execute queries and generate reports. Also, because all of an organization's data lands in a data lake, they can quickly become what is known as a data swamp - a poorly maintained data lake that is difficult to navigate and query. 

##### Data Lakehouse 

###### Data lakehouses have the following key features:

1. Transaction support to ensure that multiple parties can concurrently read or write data

2. Data schema enforcement to ensure data integrity (writes to a table are rejected if they do not match the table’s schema)

3. Governance and auditioning mechanisms to make sure you can see how data is being used 

4. BI support so that BI tools can work directly on source data - this reduces data staleness.

5. Storage is decoupled from compute, which means that it is easier for your system to scale to more concurrent users and data sizes.

6. Openness - Storage formats used are open and standard. Plus, APIs and various other tools make it easy for team members to access data directly.

7. Support for all data types - structured, unstructured, semi-structured

8. End-to-end streaming so that real-time reporting and real-time data can be integrated into data analytics processes just as existing data is

9. Support for diverse workloads, including data engineering, data science, machine learning, and SQL analytics - all on the same data repository.


#### Databricks Lakehouse Platform for Data Engineering: Delta Lake 

As mentioned in the previous section, when data arrives into the Lakehouse Platform, it lands into your organization’s open data lake. By adding Delta Lake to that open data lake, you achieve the "Lakehouse" part of the platform. In other words, the Lakehouse is essentially an open data lake with Delta Lake placed on top of it. 

Delta Lake is an open-source storage layer that brings data reliability to data lakes. When we talk about data reliability, we refer to the accuracy and completeness of your data. In other words, Delta Lake working in conjunction with a data lake is what lays the foundation for your Lakehouse - that combination guarantees that your data is what you need for your use-cases via:

1. ACID transactions, which are database transaction properties that guarantee data validity. With ACID transactions, you don’t have to worry about missing data or inconsistencies in your data from interrupted or deleted operational transactions because changes to your data are performed as if they are a single operation. 

2. Indexing, which is a way to get an unordered table (which might be inefficient to query) into an order that will maximize the efficiency of your queries

3. Table access control lists (ACLs), or governance mechanisms that ensure that only users who should have access to data can access it

4. Expectation-setting, which refers to the ability for you to configure Delta Lake based on your workload patterns and business needs

With Delta Lake, data engineers can architect pipelines for continuous data flow and refinement using Delta’s architectural model, shown in the image below. It allows data engineers to build pipelines that begin with raw data as a “single source of truth” from which everything flows. Subsequent transformations and aggregations can be recalculated and validated to ensure that business-level aggregate tables are still reflective of the underlying data, even as downstream users refine the data and introduce context-specific structure.