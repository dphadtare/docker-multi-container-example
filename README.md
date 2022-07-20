docker-multi-container-example
==========

## Note
This is fibsequence application which has following parts involved. This is a sample application created to demonstrate the multi container docker. 

**Client**

Client is frontend application to display the fibsequences generated and form to generate new fib sequence for respective integer

**Server**

Server is the backend application to calculate/store/cache/pull the fibsequence

**worker**

Worker is a consumer application to calculate the fib sequence

**Redis**

Redis is used to cache the fib sequeunce and used as a message queue

**Postgres** 

Postgres is used to store the generated fib sequence

**Nginx**

Nginx service as a proxy server and route everything behind that 
																							 
![image](https://user-images.githubusercontent.com/36766493/179988426-c3a7f0ae-11da-49d9-8e69-4dc1e081be96.png)


**Continous Deployment for multi Container Setup**

- Push code to github	
- Travis automatically pull repo
- Travis builds a test image, test code
- Travis build prod image
- Travis pushes built prod images to docker hub
- Travis pushes project to AWS EB
- EB pull images from Docker Hub, deploys
