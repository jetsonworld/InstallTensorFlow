# 젯슨 나노에서 텐서플로우 설치하기
***
2가지 설치방법을 설명하겠습니다. 

## I. 첫번째, 배쉬로 자동설치
```
wget https://raw.githubusercontent.com/jetsonworld/InstallTensorFlow/master/install-tensorflow.sh
sh install-tensorflow.sh
```

## II. 두번째, 수동설치
(1) HDF5 설치
```
sudo apt update
sudo apt-get -y install libhdf5-serial-dev hdf5-tools
```

(2) pip 설치
```
sudo apt-get -y install python3-pip
sudo pip3 install -U pip
```

(3) 텐서플로우에 필요한 패키지설치
```
sudo apt-get -y install zlib1g-dev zip libjpeg8-dev libhdf5-dev
sudo pip3 install -U numpy==1.16.1 grpcio absl-py py-cpuinfo psutil portpicker grpcio six mock requests gast h5py astor termcolor
sudo pip3 install -U cython
```

(4) 텐서플로우 설치
```
pip3 install --no-cache-dir --extra-index-url https://developer.download.nvidia.com/compute/redist/jp/v42 tensorflow-gpu==1.13.1+nv19.4 --user
```

(5) Numpy 업그레이드
```
sudo pip3 install numpy==1.18
#sudo pip3 install scipy==1.1.0
```
