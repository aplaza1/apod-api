To deploy to container registry:
```
docker buildx build --platform linux/amd64 . -t gcr.io/nasa-apod-360502/apod-api

docker push gcr.io/nasa-apod-360502/apod-api
```