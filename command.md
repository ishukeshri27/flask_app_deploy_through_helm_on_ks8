pip3 install flask - for flask installation
python3 app.py - for running flask app 
docker build -t <your image name> - building images
docker images - to check image has been build or not
docker login - to login to your docker hub
docker image tag <imagename> <yourdockerhubaccountreponame>/<tag-name-you-want-to-give> - for tagging name to image 
docker push <give your image after tagging> - for pushing image on docker hub
helm create <your-chart-name> - create helm chart
tree <your-chart-name> - to check the chart
helm lint demochart - to check whether the configuration is right after doing chages 
helm install <release_name> <chart_name>
