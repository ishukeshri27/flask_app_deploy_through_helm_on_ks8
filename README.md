Deploying flask app on K8 cluster through Helm


###################
1. Build the Flask app and then try to run it on local host.
2. Then Write Docker file to make image of your application
3. Now Build the image from DockerFile using the command - docker build -t your image name you want to give
4. Then run container using the image you created and after that add tag to your image and push it to docker hub.
5. Set up a ks8 cluster and create helm chart using command- helm create your-chart-name
6. After that check whether helm chart has been created using tree your chart-name
7. Go to deployement.yaml and then put the container port to the port on which your application is listening and in image attibute to image: "{{ .Values.image.repository }}" because as my docker image is not containing any versions and remove liveProbe and readinessProbe.
8. After that go to values.yaml and put your repo name and and containerport on which service(app) is listening.
9. Now validate the configuration using helm lint chartname 
10. If every thing is fine it will say 1 chart linted and 0 failed.
11. After that use helm install <release_name> <chart_name> to get your deployement on ks8 cluster
12. Verify it by using command kubectl get all
13. To access the app outside the cluster you can access it through port forwarding using command kubectl port-forward svc/your_service_name 31041:5000 ( hostip:containerip) or you can also change it to access it without port forwarding by changing service type to load-balancer(you will get an externl ip ) in values.yaml as by deafult service takes cluster-ip.










#HAPPY LEARNING
