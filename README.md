```bash
docker build -t gstreamer-python:ubuntu-18 .
```

```bash
xhost +local:  # to enable GUI

sudo docker run --name gstreamer-python-ubuntu-18 -it \
-e DISPLAY=$DISPLAY \
-v /tmp/.X11-unix/:/tmp/.X11-unix \
gstreamer-python:ubuntu-18
```


docker run -v /Users/Johan/IdeaProjects/gstreamer-py:/Users/Johan/IdeaProjects/gstreamer-py  \
-e DISPLAY=docker.for.mac.host.internal:0 \
gstreamer-python:ubuntu-20 /Users/Johan/IdeaProjects/gstreamer-py/basic-tutorial-1.py



forward X from docker to host
https://gist.github.com/sorny/969fe55d85c9b0035b0109a31cbcb088

https://medium.com/@mreichelt/how-to-show-x11-windows-within-docker-on-mac-50759f4b65cb

-e DISPLAY=docker.for.mac.host.internal:0
/opt/X11/bin/Xquartz :0 -listen tcp

docker build -t gstreamer-python:ubuntu-20 .