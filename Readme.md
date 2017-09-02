Inspired by [floydhub/dl-docker](https://github.com/floydhub/dl-docker), this docker includes my personal setting for Deep Learning development.

This dockerfile includes:
- Ubuntu 16.04 + Nvidia Cuda 8.0 + CuDNN 6
- Tensorflow 1.3.0 gpu
- Theano 0.9.0
- Keras 1.2.0
- Torch
- Caffe
- Caffe-SSD
- Lasange 0.1
- OpenCV 3
- Jupyter

(personal preference)
- tmux
- vim
- zsh
- 
* Welcome to grab this, but note that I am new to Docker and this dockerfile is more for personal practice. 


# Some useful commands

```bash

# run a certain python through docker
docker build -t deepaul -f Dockerfile.gpu .   # build

# run a certain python through docker
docker run -it -v "$PWD":/app -w /app -e PYTHONPATH=/root/caffe-ssd/python deepaul python xxx.py

# run a certain python through docker
nvidia-docker run -it -p 8888:8888 -p 6006:6006 -v /sharedfolder:/root/sharedfolder deepaul zsh


```bash