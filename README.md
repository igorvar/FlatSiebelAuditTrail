# FlatSiebelAuditTrail
Siebel Audit Trail is supported only at the level of one BC. In a situation where you need to track the change of children, you need to view the Audit Trail for each of them and there is no possibility to see them at the parent level.
The proposed BS based on data from vanilla Audit Trail creates a table containing data on the changes of the parent and his children.
The archive contains 3 objects:
1. Table
2. BC based on the table
3. BS

BC should be added to the BO Audit Trail.
The BS contains the Refresh function, which takes 2 arguments: the name of the parent BC and Id of the row for which data is needed.
The function deletes all previous data about this row from the table and adds new ones on the basis of Audit Trail.
