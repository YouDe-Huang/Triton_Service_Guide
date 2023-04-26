# Triton_Service_Guide
## How to install "Triton Server" environment
1. **Install Docker environment**
	1. install dependent package

		* sudo apt-get update

		* sudo apt-get install apt-transport-https ca-certificates curl gnupg-agent software-properties-common
	
	2. Add Docker GPG key

		* curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

		* sudo apt-key fingerprint 0EBFCD88

	3. Add Docker repository(stable)

		* sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

	4. Install docker-ce docker-ce-cli containerd.io

		* sudo apt-get update

		* sudo apt-get install docker-ce docker-ce-cli containerd.io

	5. Add NVIDIA Docker docker repository

		* distribution=$(. /etc/os-release;echo $ID$VERSION_ID)

		* curl -s -L https://nvidia.github.io/nvidia-docker/gpgkey | sudo apt-key add -

		* curl -s -L https://nvidia.github.io/nvidia-docker/$distribution/nvidia-docker.list | sudo tee /etc/apt/sources.list.d/nvidia-docker.list

	6. Install NVIDIA container Toolkit

		* sudo apt-get update

		* sudo apt-get install nvidia-container-toolkit

	7. Restart Docker

		* sudo systemctl restart docker

	8. Execute Docker without sudo (Optional)

		* sudo groupadd docker

		* sudo gpasswd -a ${USER} docker

		* sudo service docker restart
***

