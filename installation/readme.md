--PreReq;

--Ubuntu 18

--Install CUDA/CUDNN
(https://developer.nvidia.com/cuda-downloads?target_os=Linux&target_arch=x86_64&Distribution=Ubuntu&target_version=18.04&target_type=deb_local)

wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-ubuntu1804.pin

sudo mv cuda-ubuntu1804.pin /etc/apt/preferences.d/cuda-repository-pin-600

wget https://developer.download.nvidia.com/compute/cuda/11.8.0/local_installers/cuda-repo-ubuntu1804-11-8-local_11.8.0-520.61.05-1_amd64.deb

sudo cp /var/cuda-repo-ubuntu1804-11-8-local/cuda--keyring.gpg /usr/share/keyrings/

sudo dpkg -i cuda-repo-ubuntu1804-11-8-local_11.8.0-520.61.05-1_amd64.deb

sudo apt-get update

sudo apt-get -y install cuda*

--Install zlib

sudo apt-get install zlib1g

--install latest GPU drivers.
--install cudnn
https://developer.nvidia.com/rdp/cudnn-archive
Download from here and open with installer.

https://docs.nvidia.com/deeplearning/cudnn/install-guide/index.html#installcuda

Install docker
install the pre-reqs

sudo apt-get install curl apt-transport-https ca-certificates software-properties-common

Add repos

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"


