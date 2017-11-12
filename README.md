# Multiple-Ways-Create-DataFrame
#created using the Dataframe Api
>spark -shell --packages com.packages.databricks:spark-csv_2.10:1.4.0
scala> val df1=sqlContext.read.format("com.databricks.spark.csv").option("header","false").option("infraschema","true").load("/user/cloudera/ola.csv")
scala> df1.registerTempTable("Table");
scala> val afm = sqlContext.sql("select * from Table").show()
