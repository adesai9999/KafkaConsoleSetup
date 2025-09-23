# Install Kafka Console

1. Go to Operators > Installed Operators. 

	If you see any errors make sure you are on the correct Project Name - userxx-project

2. Click on *Streams for Apache Kafka Console*

3. Click on *Create Instance*

4. Go to **YAML View**:  Paste the below YAML
```
apiVersion: console.streamshub.github.com/v1alpha1
kind: Console
metadata:
  name: userXX-console
  namespace: userXX-project
spec:
  hostname: userXX-console.apps.cluster-xxxx.dynamic.redhatworkshops.io
  kafkaClusters:
    - listener: plain
      name: names-cluster
      namespace: userXX-project
```
		  		  
   Click *Create* Button at the bottom
	
5. A Kafka Console Pod should be running in the namespace. 

6. Open the URL in a browser window:
https://userXX-console.apps.cluster-xxxx.dynamic.redhatworkshops.io

7. Click on *Click to login Anonymously*

8. Explore the Kafka Console UI. 

9. Under *Topics* > Click on *names* topic to explore the different messages and their values getting published to Kafka. 


