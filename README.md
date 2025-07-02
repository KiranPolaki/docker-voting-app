### Tech Stack

- A front-end web app in [Python](/vote) which lets you vote between two options
- A [Redis](https://hub.docker.com/_/redis/) which collects new votes
- A [.NET](/worker/) worker which consumes votes and stores them in…
- A [Postgres](https://hub.docker.com/_/postgres/) database backed by a Docker volume
- A [Node.js](/result) web app which shows the results of the voting in real time

### Run the app in Kubernetes

The folder k8s-specifications contains the YAML specifications of the Voting App's services.

Run the following command to create the deployments and services. Note it will create these resources in your current namespace (default if you haven't changed it.)

kubectl create -f k8s-specifications/
The vote web app is then available on port 31000 on each host of the cluster, the result web app is available on port 31001.

To remove them, run:
kubectl delete -f k8s-specifications/

### We will be creating this dashboard by end of today

![alt text](image.png)
