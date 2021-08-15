# Docker image pull and Push To Azure Cloud  Container

### Image pull from Docker
1. login to docker hub
```
docker login
```
2. pull the image which you want
```
docker pull {image-name}
```
3. check the downloaded image and find it's already there
```
docker images
```
### Login to cloud Container registry
1. login to azure portal from terminal
```
az login
```
2. login to azure container registry
```
az acr login --name myregistry
```
3. tag the pulled image for cloud registry
```
docker tag dockerimage:tag cloudimage:tag
```
#### example
```
docker tag busybox:latest yourcloudcr.azurecr.io/dockerimages/busybox:latest
```
4. push the image to cloud container registry
```
docker push cloudimage:tag
```

##### author @yannainglin



