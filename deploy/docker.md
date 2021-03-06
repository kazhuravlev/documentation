# Docker image

Centrifugo server has docker image [available on Docker Hub](https://hub.docker.com/r/centrifugo/centrifugo/).

```
docker pull centrifugo/centrifugo
```

Run:

```bash
docker run --ulimit nofile=65536:65536 -v /host/dir/with/config/file:/centrifugo -p 8000:8000 centrifugo/centrifugo centrifugo -c config.json
```

Note that docker allows to set nofile limits in command-line arguments.

To run with admin web interface:

```bash
docker run --ulimit nofile=65536:65536 -v /host/dir/with/config/file:/centrifugo -p 8000:8000 centrifugo/centrifugo centrifugo -c config.json --web
```

### Alternative Dockerfile

There is also docker image in Centrifugo repository.

See https://hub.docker.com/r/fzambia/centrifugo/

This docker image based on centos 7 and rather big in size (~250MB)
