This is the starting point to AI!

Before we start the coding, we should know the docker workflow for this task, since we have not installed the Tensorflow locally for this purpose and we will use the tensorflow gpu docker image with jupyter notebook for this task. let's go ...
[[how to use tensorflow docker image for running my codes]]
Now we have the development setup ready. The first thing I want to do is just running the code  of [tensorflow example for object detection using tensorhub models](https://www.tensorflow.org/hub/tutorials/tf2_object_detection). Note that in the import section of the example notebook, some of the imported modules have not been installed in the tensorflow docker image by default so you need to install, `scipy, tensorflow_hub`. The other problem is that because of internet connection problems in our place we can't use the `hub` module for fetching the pre-trained models from the tensorhub. Accordingly, we should donwload the models manually and put them in a specific directory structure, to be able to load them and use them for inference. [This medium article](https://xianbao-qian.medium.com/how-to-run-tf-hub-locally-without-internet-connection-4506b850a915) is a good place to learn how to use tensorhub downloaded models, without downloading them by the `hub` module itself. Furthermore by sharing the jupyter notebook directory between container and host, using docker mount option, you can download things in host system and put them in docker container filesystem(There may be some permissions in the future caused by this way of downloading and copying from host to container filesystem, but I have not faced these issues yet.).
Now, we are at the position that we can run the example code and see the inference outputs in the jupyter notebook. For now our task is:
- [ ] Diving deep into the example code and learn every bit of that!
After that we can go further and see how we can use our custom models and so on. So in the future ...
Let's go and learn it!


