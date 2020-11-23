# Using Oracel Data Science with MDS

## Deploy Oracle Data Science

* Create a compartment
* Create users/groups
* Create policies to use Data Science
** allow group QubixDataScientists to manage data-science-family in compartment QubixSlovenia-DataScience for QubixDataScientists-manage-access
** allow group QubixDataScientists to use virtual-network-family in compartment QubixSlovenia-DataScience for QubixDataScientists-manage-network-access
** allow service datascience to use virtual-network-family in compartment
* create VCN
* Create a Data Science Project and a Notebook session
