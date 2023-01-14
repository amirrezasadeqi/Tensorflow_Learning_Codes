To create a docker container for learning the use of tensorhub models in object detection, you can use below command:
```shell
docker run -it --net=bridge --gpus all --name tensorhub_obj_detection \
-p 8888:8888 \
-w /tmp \
--env="DISPLAY" \
--env="NVIDIA_DRIVER_CAPABILITIES=all" \
--env="QT_X11_NO_MITSHM=1" \
--volume="/tmp/.X11-unix:/tmp/.X11-unix:rw" \
--volume="$PWD:/tmp" \
tensorflow/tensorflow:latest-gpu-jupyter \
bash
```
note that in the case you want to run GUI applications from inside of the docker container, you also need to provide the permission of using the X server by running `xhost +` (`xhost -` to disable the permission).
Also note that you should run above command in the directory of the jupyter notebooks. In the container you can run jupyter notebook server by running below command:
```shell
jupyter notebook --ip 0.0.0.0 --no-browser --allow-root
```
now in the host machine you can open the jupyter notebook by opening the link from above command output in the firefox or by opening `localhost:8888/tree‌` in firefox and copy/paste the token from the above command output in the corresponding form field. Now the tensorflow docker container with gpu support is at your service!