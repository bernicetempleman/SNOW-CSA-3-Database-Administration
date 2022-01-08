# SNOW-CSA-3-Database-Administration

Database Administration

## Data Schema
The schema map displays the details of tables and their relationships in a visual manner, allowing administrators to view and easily access different parts of the database schema.

The schema map can also be printed directly from a browser.

- referenced by
- referencing
- extended by
- extended
- 
https://docs.servicenow.com/bundle/rome-platform-administration/page/administer/table-administration/concept/c_SchemaMapForTables.html

## Application/Access Control
https://docs.servicenow.com/bundle/rome-platform-administration/page/administer/security/concept/c_SNCAccessControl.html

## CMDB

-A configuration management database (CMDB) is a central repository that acts as a data warehouse, storing information about your IT environment and it is a purpose-built database for configuration management.

With the ServiceNow Configuration Management Database (CMDB) application, you can build logical representations of assets, services, and the relationships between them that comprise the infrastructure of your organization. Details about these components are stored in the CMDB which you can use to monitor the infrastructure, helping ensure integrity, stability, and continuous service operation.

Use core features such as CMDB Health, CMDB Identification and Reconciliation, and CMDB CI Lifecycle Management to monitor and detect health issues, reconcile data integrity issues, and manage data life cycle.

- Baseline CMDB
CMDB baseline provides capabilities that help you understand and control the changes that have been made to your configuration items (CIs) in the CMDB.

You can create a baseline, which is a snapshot of your configuration items in the CMDB. You can review the changes that have been made to that configuration item since a previous baseline. Multiple baselines may be created and the system tracks the changes that have been made per baseline.
Creating a baseline captures the attributes of the CI as well as all first-level relationships for the CI. Any changes to the base CI or to any related CIs are captured and displayed. Newly created CIs are not automatically added to a baseline.

Associate a configuration item with a task, a change or change task, and to propose changes to the CI after the change is complete. You can record changes, and these changes are not applied to the CI immediately but are delayed until the change is complete.
When the change is complete, you can choose to apply the proposed changes which makes all changes previously proposed and associates the changes with the task.
https://docs.servicenow.com/bundle/rome-servicenow-platform/page/product/configuration-management/concept/c_BaselineCMDB.html#c_BaselineCMDB

- CI
It is important to manage the relationship between assets and associated CIs. Assets are tracked with the Asset Management application, which focuses on the financial aspects of owning property. Configuration items are stored in the CMDB, which is used to track items and make them available to users.

When an asset has a corresponding configuration item, the asset record and the configuration item record are kept synchronized with two business rules.

Update CI fields on change (on the Asset [alm_asset] table)
Update Asset fields on change (on the Configuration Item [cmdb_ci] table)
Note: Assets and CIs can be synchronized only if they are logically mapped.
https://docs.servicenow.com/bundle/rome-it-asset-management/page/product/asset-management/concept/c_ManagingAssets.html

- CI relationships

https://docs.servicenow.com/bundle/rome-servicenow-platform/page/product/configuration-management/concept/c_ITILConfigurationManagement.html

## Import Sets
https://docs.servicenow.com/bundle/rome-platform-administration/page/administer/import-sets/concept/c_ImportDataUsingImportSets.html
