# mono-compile


## build image and push

```sh
docker build . -t aspick/mono-compile
docker login
docker push aspick/mono-compile
```

## use
```sh
docker run -v $(pwd):/project -w /project aspick/mono-compile mono ../packages/nuget.exe restore
docker run -v $(pwd):/project -w /project aspick/mono-compile xbuild
```
