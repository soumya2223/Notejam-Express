
### Create the App
Firstly, we git clone the notejam/express repo "https://github.com/komarserjio/notejam/tree/master/express" in our local system.

***
Step1: Create DokerFile to Dockerised this express web app
~~~
nano Dockerfile
~~~
Step2:Build Dockerfile using this command
~~~
$ sudo docker build -t <image_name:tag> <path/URL>
~~~
Step1: Create the manifest file for your notejam-app namespace
```
$sudo kubectl create -f <namespace.yaml>
```

Step2: Create the manifest file for your service
```
$sudo kubectl create -f <service.yaml>
```

Step3: Create the manifest file for your notejam-app deployment
```
$sudo kubectl create -f <deployment.yaml> 
```

### View the notejam-app
***
Step1: Get your worker node’s external IP address. Copy down the EXTERNAL-IP value for any worker node in the cluster:
```
$kubectl get nodes -o wide
```

Step2:Access the notejam-app services to view its exposed port 
```
$kubectl get svc -n <service-name>
```
Note: application run through <clusterIP>:<port>
 It work only minikube node only in other it is not working 

![Screenshot from 2019-12-18 15-58-29](https://user-images.githubusercontent.com/54974563/71540861-1b5a3d80-2976-11ea-9a79-475ef3a3f313.png)

