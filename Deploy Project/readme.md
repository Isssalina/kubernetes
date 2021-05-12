# Prepare java project and package java (jar package or war package)
1. Need to use two dependent environments  
* java environment-jdk  
* maven environment  
2. Type the java project (springboot) into a war package  

* Important things: write dockerfile
~~~
//dockerfile

FROM openjdk:8-jdk-alpine
VOLUME /tmp
ADD ./target/demojenkins.jar demojenkins.jar
ENTRYPOINT ["java","-jar","/demojenkins.jar", "&"]
~~~

~~~
# Package via maven
//Open cmd.exe in the project

mvn clean package

//After packaging, a jar package will be generated under the project
~~~
# Make a mirror
~~~
# Make mirror
docker build -t Java-demo-01:latest.

# View mirror
docker image

# Test: Whether the mirror created by local boot can be accessed normally
//Start the mirror
docker run -d -p 8111:8111 Java-demo-01:latest -t

//View the process occupied by port 8118
netstat -tunlp | grep 8111

//View process
ps -ef | grep demo
~~~
# Upload the mirror to the mirror server
~~~
# Log in to the mirror server

# Add the version number to the mirror

# Push the mirror to the server
~~~
# Deploy images to expose applications
~~~
# Create the yaml file of the deployment type pod
kubectl create deployment javademo1 --image=Java project mirror address (find on Alibaba Cloud server): mirror version --dry-run -o yaml> javademo1.yaml

# Execute yaml file
kubectl apply -f javademo1.yaml

# View the successfully created pod
kubectl get pods -o wide

# Expansion copy
kubectl scale deployment Javademo1 --replicas=3

# Expose the port to the outside (two ways: service, ingress)
//service way
kubectl expose deployment javademo1 --port=8111 --target-port=8111 --type=NodePort

# View externally exposed applications
kubectl get svc
~~~
