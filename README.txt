Step1: Create the manifest file for your notejam-app namespace
  $sudo kubectl create -f namespace.yaml

Step2: Create the manifest file for your service
  $sudo kubectl create -f service.yaml

Step3: Create the manifest file for your notejam-app deployment
  $sudo kubectl create -f deployment.yaml 

View the notejam-app
Step1: Get your worker node’s external IP address. Copy down the EXTERNAL-IP value for any worker node in the cluster:
 $kubectl get nodes -o wide

Step2:Access the notejam-app services to view its exposed port 
 $kubectl get svc -n notejam-app
![alt text](/home/soumya/Pictures/f1.png)
