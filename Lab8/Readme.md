# Using Oracel Data Science with MDS

## Deploy Oracle Data Science

* Create a compartment
* Create users/groups
* Create policies to use Data Science

```
allow group QubixDataScientists to manage data-science-family in compartment QubixSlovenia-DataScience for QubixDataScientists-manage-access
allow group QubixDataScientists to use virtual-network-family in compartment QubixSlovenia-DataScience for QubixDataScientists-manage-network-access
allow service datascience to use virtual-network-family in compartment
```

* Create VCN
* Create a Data Science Project and a JupyterLab Notebook session

## Basic Configuration

1. Setup your OCI and API Key to access OCI resources by creating the OCI ``config`` file in the terminal session

[ds-1](img/DS-1.jpg)

2. There are preinstalled connectos that allow you to work with MDS
* cx-Oracle: A Python extension module that enables access to Oracle Database.
* sqlite3: Provides an sqlite3 driver.
* ipython-sql: Adds JupyterLab magic (%sql or %%sql) to connect to various databases and issue SQL commands directly in a notebook cell.
* mysql-connector-python: A self-contained Python driver for communicating with MySQL servers.
* SQLAlchemy: The Python SQL toolkit and Object Relational Mapper that gives application developers the full power and flexibility of SQL.

3. Create a JupyterLab notebook to connect to MDS

```
import mysql.connector

cnx = mysql.connector.connect(user='admin', password='MySQL8.0',
                              host='10.0.1.6',
                              database='employees')
query = ("SELECT * from employees")
cursor = cnx.cursor()
cursor.execute(query)
rows = cursor.fetchall()
for row in rows:
   print(row)
```
