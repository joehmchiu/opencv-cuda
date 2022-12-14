# opencv-cuda
Build opencv with cuda and cuDnn supports by Windows 11.
## pre-requisites
* install chocolatey 
  * https://docs.chocolatey.org/en-us/choco/setup
  * Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
* install java 8
  * choco install -y jdk8
* install python
  * choco install -y python
* install visual studio 2019 v.16
  *  choco install -y visualstudio2019community
* install cmake version 3.23
  * choco install -y cmake --version=3.23
  * add "C:\Program Files\CMake\bin" to environment path
* install cuda toolkits
  * choco install -y cuda
  * or download site: https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64&target_version=11 
  * download cuDnn package from: https://developer.nvidia.com/cudnn (cudnn-windows-x86_64-8.6.0.xxx_cudaxx-archive.zip)
  * make sure merged all cuDnn files under cuda installed path: eq. C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.8\
    * bin
    * include
    * lib
    * LICENSE

## Build and Install
* Follow these articles for the build and installation. 
  * https://machinelearningprojects.net/build-opencv-with-cuda-and-cudnn/
    * WITH_CUDA
    * OPENCV_DNN_CUDA
    * FAST_MATH
    * EXTRA
    * FAST
  * https://thinkinfi.com/install-opencv-gpu-with-cuda-for-windows-10/
  * https://www.youtube.com/watch?v=d8Jx6zO1yw0
    * cmake --build "C:\gpu\opencv\build" --target INSTALL --config Release

## Test
<pre>
import cv2
cv2.__version__
cv2.cuda.getCudaEnabledDeviceCount()
</pre>
<pre>
import cv2
from cv2 import cuda
cuda.printCudaDeviceInfo(0)
</pre>

## Issue
* zlibwapi.lib missing issue
* download zlib123dllx64.zip though it's not in recommnendations
## GPU Supported
* https://en.wikipedia.org/wiki/CUDA#:~:text=GPUs%20supported%5Bedit%5D
