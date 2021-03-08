# Pytorch_objectdetecttrack

[![license](https://img.shields.io/github/license/mashape/apistatus.svg)](LICENSE)[![Git HUB Badge](http://img.shields.io/badge/-Tech%20blog-black?style=flat-square&logo=github&link=https://github.com/jdj2261)](https://github.com/jdj2261)

pytorch_objectdetecttrack 설치 및 데모 실행하기 ([pytorch_objectdetecttrack](https://github.com/cfotache/pytorch_objectdetecttrack.git))

작성자 : 진대종 ([github](https://github.com/jdj2261))

> Environment
>
> - Ubuntu Version : 18.04
> - CUDA Version : 10.0
> - cuDNN Version :  7.6.5



### 1. 가상환경 생성 및 활성화

~~~
$ conda create --name pytorch_objectdetecttrack
$ conda activate pytorch_objectdetecttrack
~~~

### 2. git 복제하기

- git clone

  ```
  $ git clone https://github.com/cfotache/pytorch_objectdetecttrack.git
  $ cd pytorch-yolo-v3
  ```

### 3. pytorch 설치하기

- pytorch 설치

  - [pytorch-1.2.0 설치](https://pytorch.org/get-started/previous-versions/)

  ~~~
  $ conda install pytorch==1.2.0 torchvision==0.4.0 cudatoolkit=10.0 -c pytorch
  ~~~

### 4. 필수 패키지 설치하기

- 필수 패키지 설치 

  - matplotlib, pandas, opencv

  ~~~
  $ conda install matplotlib
  $ conda install pandas
  $ conda install numba (pytorch_objectdetecttrack)
  $ conda install scikit-image (pytorch_objectdetecttrack)
  $ conda install scikit-learn (pytorch_objectdetecttrack)
  $ conda install filterpy (pytorch_objectdetecttrack)
  $ conda install --channel mempo opencv
  $ pip install opencv-contrib-python
  ~~~

### 5. Demo 실행하기

- 가중치 다운로드

  ~~~
  $ wget https://pjreddie.com/media/files/yolov3.weights 
  ~~~

- Image Demo

  ~~~
  $ python detect.py --images $(img path) --det det 
  ~~~

- Video Demo

  ~~~
  $ python video_demo.py --video video.avi
  ~~~

- Webcam Demo

  ~~~
  $ python cam_demo.py
  ~~~