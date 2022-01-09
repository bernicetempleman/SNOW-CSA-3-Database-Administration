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

Import Sets is a powerful tool used to import data from various data sources, and then map that data into ServiceNow tables.

The Import Sets table acts as a staging area for records imported from a data source.

Note: Data should not be imported in extremely large chunks. Creating an extremely large import set can cause delays and system outages.
![image](https://user-images.githubusercontent.com/12488769/148668060-925531f0-197f-453f-a50a-1da15f7d5d4e.png)

## Transform MAP
A Transform Map is a set of field maps that determine the relationships between fields in an Import Set and fields in an existing ServiceNow table (such as Incidents or Users)


Once defined, existing Transform Maps can be reused for mapping data from an import set to a ServiceNow table


Every import operation to a ServiceNow production table requires at least one transform map that will be associated with an Import Set

![image](https://user-images.githubusercontent.com/12488769/148668077-f19b0281-5640-4ca7-bc01-490a0ee926c2.png)

System Import Set- Steps
Load Data: Data source records are references imported data or location to retrieve data from.


Create Transform Map: is used to specify how data uploaded into an Import Set should be transferred onto production tables. 


Run Transform: Transform map scripts allow for customization of import operations using a robust programming interface that can be used to introduce advanced logic. 

## Load Data
![image](https://user-images.githubusercontent.com/12488769/148668110-21a9cdaa-62b7-46bb-aa29-e45addc01f29.png)

## Transform Map
![image](https://user-images.githubusercontent.com/12488769/148668116-5c080ef4-8af8-43b3-8700-036ff399eb62.png)

### Mapping Assist
![image](https://user-images.githubusercontent.com/12488769/148668126-6ca24d39-16fd-4e76-89f0-dd50793c3ccb.png)

![image](https://user-images.githubusercontent.com/12488769/148668132-911d4519-eaf6-43dd-ac9a-f6b563b69b18.png)

### Coalesce

### Choice Action
- create:  creates a new reference field record if a matching record does not exist.
- ignore: ignores new records in the reference field and completes processing of all other fields in the transform map.
- reject: stops the transform for the entire record.

Note: The field map only displays the Choice action field for reference fields.

## Run Transform
![image](https://user-images.githubusercontent.com/12488769/148668141-668bdeb4-e11f-4ed6-9852-388da624fe03.png)

![image](https://user-images.githubusercontent.com/12488769/148668143-072afa90-4a4d-43a5-9b30-f2137290ff7b.png)








https://docs.servicenow.com/bundle/rome-platform-administration/page/administer/import-sets/concept/c_ImportDataUsingImportSets.html
