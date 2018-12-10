# go-map-reduce

## compile
```
GOARCH=amd64 CGO_ENABLED=0 GOOS=linux go build wordcount.go
```

## dockerizing
```
docker build -t gcr.io/.../wordcount:latest .
docker push gcr.io/.../wordcount:latest
```

## run glow cluster
```
kubectl create -f master-rc.yaml
kubectl create -f Service.yaml
kubectl create -f node-rc.yaml
```

## test
```
kubectl create -f job.yaml
```
