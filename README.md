# A Foo Specific Mongo Image

**Warning**: this is an experimental image that will surely introduce breaking changes.

## Docker: Building and Pushing

```bash
export DOCKER_TAG_NAME="foo-mongo" \
&& export DOCKER_VERSION="base" \
&& export DOCKER_USERNAME="foosoftware" \
&& docker build -t $DOCKER_TAG_NAME . -f Dockerfile
```
then:
```bash
$ docker login
```

then:
```bash
docker tag $DOCKER_TAG_NAME $DOCKER_USERNAME/$DOCKER_TAG_NAME:$DOCKER_VERSION \
&& docker push $DOCKER_USERNAME/$DOCKER_TAG_NAME:$DOCKER_VERSION
```

- [Pushing to DockerHub](https://docs.docker.com/docker-cloud/builds/push-images/).
