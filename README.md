# multi_schema_example
Please keep in mind the following:
1. This is a Liquibase Oracle project but can easily become another database platform with some adjustments to the scripts.
2. The liquibase.properties will need to be completed with the right information for the different properties.
3. Prior to running the "update_prefixed_multi_schemas.sh" script make sure to do the following:<br />
  a. please keep in mind that Liquibase will combine a schema list by a fixed list.<br />
  b. Or by parsing the schemanames from the filenames (if uncommenting line 5).<br />
  c. This example is using a master changelog "main.xml" with an includeAll tag pointing to a folder SQLFILES containing the SQL files.<br />
  D. Each SQL file (also a formatted SQL changelog) will need to have a context changeset attribute with the specific schema name associated with the SQL script, so    Liquibase will know to what schema it should maintain the tracking tables for.
