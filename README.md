# Puppeteer / Chrome / Node.js

A basic container setup for Puppeteer on Node.js. Unofficial: beware - may become stale.

## Docker: Building and Pushing

```bash
export DOCKER_TAG_NAME="puppeteer-chrome-node" \
&& export DOCKER_VERSION="latest" \
&& export DOCKER_USERNAME="foosoftware" \
&& docker build -t $DOCKER_TAG_NAME .
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
