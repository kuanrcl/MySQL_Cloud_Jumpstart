# Using Oracel Data Science with MDS

## Deploy Oracle Data Science

* Create a compartment
* Create users/groups
* Create policies to use Data Science
* allow group QubixDataScientists to manage data-science-family in compartment QubixSlovenia-DataScience for QubixDataScientists-manage-access
* allow group QubixDataScientists to use virtual-network-family in compartment QubixSlovenia-DataScience for QubixDataScientists-manage-network-access
* allow service datascience to use virtual-network-family in compartment
* create VCN
* Create a Data Science Project and a Notebook session

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
