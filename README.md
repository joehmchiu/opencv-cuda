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
* install cuda toolkits
  * choco install -y cuda
  * or download site: https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64&target_version=11

## Build and Install
* Follow this article for the build and installation. 
  * https://machinelearningprojects.net/build-opencv-with-cuda-and-cudnn/
