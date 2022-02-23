# build-openpose-using-docker
Build OpenPose GitHub Project using docker

CAUTION: the machine on which you build the docker needs to have NVidia drivers installed since we are going to install OpenPose with CUDA support.

# How to build using docker
```sh
docker build -t <my-docker-name>:<tag> .
```

# Running OpenPose Through docker
```sh
docker run --rm -it --gpus all -w /opt/openpose -v ${PWD}:/tmp <my-docker-name>:<tag> /opt/openpose/build/examples/openpose/openpose.bin --video /opt/openpose/examples/media/video.avi --write_json /tmp --display 0 --render_pose 0
```
