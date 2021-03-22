# Pytorch_objectdetecttrack

[![license](https://img.shields.io/github/license/mashape/apistatus.svg)](LICENSE)[![Git HUB Badge](http://img.shields.io/badge/-Tech%20blog-black?style=flat-square&logo=github&link=https://github.com/jdj2261)](https://github.com/jdj2261)

pytorch_objectdetecttrack 설치 및 데모 실행하기 ([pytorch_objectdetecttrack](https://github.com/cfotache/pytorch_objectdetecttrack.git))

작성자 : 진대종 ([github](https://github.com/jdj2261))

> Environment
>
> - Ubuntu Version : 18.04
> - CUDA Version : 11.0
> - cuDNN Version :  7.6.4



### 1. 가상환경 생성 및 활성화

~~~
$ conda create --name pytorch_objectdetecttrack
$ conda activate pytorch_objectdetecttrack
~~~

### 2. git 복제하기

- git clone

  ```
  $ git clone https://github.com/cfotache/pytorch_objectdetecttrack.git
  $ cd pytorch_objectdetecttrack
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
  $ conda install --channel menpo opencv
  $ pip install opencv-contrib-python
  ~~~

### 5. Demo 실행하기

- 가중치 다운로드

  ~~~
  $ wget https://pjreddie.com/media/files/yolov3.weights 
  ~~~

  - custom 가중치 다운로드

    [yolov3_custom.weights](https://drive.google.com/file/d/1IQij8aMnj7CQFa4VFg4Qqz5rPR-irjQB/view?usp=sharing) 다운 (237MB)

    ~~~
    $ curl -c ./cookie -s -L "https://drive.google.com/uc?export=download&id=1IQij8aMnj7CQFa4VFg4Qqz5rPR-irjQB" > /dev/null
    $ curl -Lb ./cookie "https://drive.google.com/uc?export=download&confirm=`awk '/download/ {print $NF}' ./cookie`&id=1IQij8aMnj7CQFa4VFg4Qqz5rPR-irjQB" -o yolov3_custom.weights
    ~~~

- Video Demo

  ~~~
  $ python3 object_tracker.py
  ~~~

  > object_tracker.py 파일 수정
  >
  > config_path= 'config/yolov3.cfg'
  >
  > weights_path='config/yolov3.weights'
  >
  > class_path=  'config/coco.names'    
  >
  > videopath = '/home/djjin/Videos/dwelling.mp4'