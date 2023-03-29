# Accuracy-Latency-Tradeoff-Dataset

Rate limiting service in API Gateways controls the entry of the request by throttling the requests with a boundary.
This repository consists the dataset that is created to analyze the parameters that are highly affect the performance of rate limiting service.

Dataset creation

This dataset has been created by undergoing set of tasks
1. Identifying parameters
2. Constructing a deployment architecture
    Jmter is used as the front end to send requests
    Envoy proxy API gateway is used in middle and the Ratelimiting service and Backend service are part of Envoy proxy API gateway.
    Deployment Architecture
    
    ![Frame 1](https://user-images.githubusercontent.com/78297372/228508967-8966e740-a325-43e8-90c1-29bf1888cdfc.png)
    
4. Creating testplans
5. Implementing testplan
    Each of the testplan stated is run for 10 mins which means each of the row in the dataset has been obtained by running a test for 10 mins. 
    
Design of the dataset

   ![m](https://user-images.githubusercontent.com/78297372/228509497-574ebcaa-556b-4b8b-8411-f02244e3a1bc.PNG)

The dataset is of seven columns
1. Concurrency
2. Number of successful requests
3. Error percentage
4. Rate limit
5. Throughput
6. Latency
7. Timeout
