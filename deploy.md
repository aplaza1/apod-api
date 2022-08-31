Login to gcloud
```
 gcloud auth login
 ```

To deploy to container registry:
```
docker buildx build --platform linux/amd64 . -t gcr.io/nasa-apod-360502/apod-api

docker push gcr.io/nasa-apod-360502/apod-api
```

Deploy deployment manager template:
```
gcloud deployment-manager deployments create nasa-apod --config ./gcloud/vm.yaml
```


Delete deployment:
```
gcloud deployment-manager deployments delete nasa-apod
```


gcloud compute instances describe nasa-apod-client
