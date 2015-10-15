Databricks Code Assignment: External GroupBy
==============================================

Run Test:
------------------------------------
This project is developed with Eclipse.

``GroupByMap.java``: process the input. If all the input data can be processed in memory,
it will return the result directly. Otherwise, it will save partial results to temp files.

``GroupByReduce.java``: Similar to Reduce in MapReduce, it will process partial results in
temp files, and output the final result to a temp file. Then, a FileIterator is returned.

``FileIterator.java``: Iterate records in a file, parse them, and return them in the required format.

``ExternalGroupBy.java``: The main class to process input data. Two parameters are required:

* ``chunkSize``: specify the number of records that can be processed in memeory
* ``reduceSum``: specify the number of GroupByReduce threads that can be run in parallel.

Run Test:
------------------------------------
Overall test: 

.. code-block:: bash
	
	javac ExternalGroupByTest.java
	java ExternalGroupByTest
	
FileIterator test:

.. code-block:: bash
	
	javac FileIteratorTest.java
	java FileIteratorTest
	
