# deep-learning-getting-started
Setting up Tensorflow and deep learning resources

## Setting up Tensoflow

### Installation
- Follow the [Docker installation instructions](https://www.tensorflow.org/versions/r0.11/get_started/os_setup.html#docker-installation)

- Make sure to [test your installation](https://www.tensorflow.org/versions/r0.11/get_started/os_setup.html#test-the-tensorflow-installation)

- In your working directory create a folder named `notebooks` to save all your notebooks developped using Tensorflow.

### Launching Tensorflow

- Launch your image using the following command (assuming you are using the latest-devel image):

```
docker run -it -p 8888:8888 -p 6006:6006 -v $PWD/notebooks:/root/notebooks gcr.io/tensorflow/tensorflow:latest-devel
```

`-p 8888:8888`: exposes the port 8888 (Jupyter Notebooks)
`-p 6006:6006`: exposes the port 6006 (Tensorboard)
`-v $PWD/notebooks:/root/notebooks`: mounts a volume to save and reuse your notebooks between sessions.

### Launching Tensorboard

`tensorboard --logdir=/root/notebooks/[LOG DIRECTORY]`

## Resources

[Deep Learning Book](http://www.deeplearningbook.org/)
[Tensorflow tutorials](https://www.tensorflow.org/versions/r0.11/tutorials/index.html)
