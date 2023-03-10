# Installing Apache Superset in windows using WSL ( Windows Subsystem for Linux )

Step 1 - Go to microsoft store and install the latest version of ubuntu

step 2 - Make sure in Windows Features the following options are turned on

- Virtual Machine Platform
	
- Windows Hypervisor Platform
	
- Windows Subsystem for Linux
	
step 3 - After Ubuntu Installation, run command `sudo apt-get update` to update the system

step 4 -  Remove any Docker files if they are running in the system, using the following command:

	sudo apt-get remove docker docker-engine docker.io
	
step 5 - Now Install docker from powershell on windows using the below command 

	Start-Process 'Docker Desktop Installer.exe' -Wait install
	
Alternatively you can refer the documentation on offical [docker.com](https://docs.docker.com/desktop/install/windows-install/#install-docker-desktop-on-windows) to install docker on windows

step 6 - Clone Superset's repo in your terminal with the following command:

	git clone https://github.com/apache/superset.git
	
step 7 - Navigate to the folder you created in previous step 

	cd superset
	
step 8 - run the following commands to initiatie docker and run Apache Superset

	docker-compose -f docker-compose-non-dev.yml pull
	
	docker-compose -f docker-compose-non-dev.yml up
	
- Thats it ! now you should be able to run Apache Superset on your local brower localhost on port 8088.

-  loging into superset you can use **admin** as username and password.

- For Further Documentation you can refer the following links [Superset](https://superset.apache.org/docs/installation/installing-superset-using-docker-compose/) and
[Docker](https://docs.docker.com/desktop/windows/wsl/) 




