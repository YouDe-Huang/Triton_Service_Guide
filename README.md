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
