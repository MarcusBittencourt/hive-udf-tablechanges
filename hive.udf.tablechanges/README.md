https://blog.matthewrathbone.com/2013/08/10/guide-to-writing-hive-udfs.html

%> mvn assembly:single
%> hive
hive> ADD JAR target/hive-extensions-1.0-SNAPSHOT-jar-with-dependencies.jar;
hive> CREATE TEMPORARY FUNCTION tablechanges as 'hive.udf.tablechanges.Executor';
hive> select * from tablechanges(table1, table4comparision);