1. pip3 install flask - for flask installation
2. python3 app.py - for running flask app
3. docker build -t <your image name> - building images
4. docker run -p hostport:containerport <imagename> - to run app as conatiner
5. docker images - to check image has been build or not
6. docker login - to login to your docker hub
7. docker image tag <imagename> <yourdockerhubaccountreponame>/<tag-name-you-want-to-give> - for tagging name to image
8. docker push <give your image after tagging> - for pushing image on docker hub
9. helm create <your-chart-name> - create helm chart
10. tree <your-chart-name> - to check the chart
11. helm lint demochart - to check whether the configuration is right after doing chages
12. helm install <release_name> <chart_name> to run your helm chart and get deployment of service of cluster
13. kubectl get all - to check deployement of components
14.kubectl port-forward svc/flask-demo-flask-demo-chart 31041:5000 - to port forward the service as it is of type cluster ip 
