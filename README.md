requestsInParallel
==================

python script to fire off http Requests in parallel using payload data from a file

In production environment we often need to fire off hundreds of thousands of http requests by reading data off ascii file.
This simple script help to fire off requests in parallel. These are the global variables that you'll typically modify:

define threadpool size:
g_num_concurrent_threads = 10

each threadpool gets a batch of records read from the database
g_batchSize = 1000

separator used in the file
g_separator = ","

rest url base
g_uriBase = "http://hostname:8080/MyService/resourceName"

translates to &customerId=<data>&deptName=<data>
g_data_headers = ["customerId", "deptName"]

type of http request
g_verb = "PUT"
