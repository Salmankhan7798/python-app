
-------my-task on python project - day-1--------


1. Launch EC2 instance 
2. Install Java as we are going to install jenkins on the same instance.
	
	sudo apt update
	sudo apt-get install openjdk-17-jre
	java -version
	
3. Jenkins installation
	
	curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
  
	echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
  
	sudo apt-get update
	sudo apt-get install jenkins
	

4.	Docker installation
	
	apt install docker.io
	
	usermod -aG docker jenkins
	
	chmod 777 /var/run/docker.sock

5.	Now get the source code by cloning below repositoy
		https://github.com/Salmankhan7798/python-app.git
		
6.	cd another_python_project 

7.	Now unloack and access jenkins on web with public ip of ec2 instance with 8080	port
	http://18.191.85.1:8080/
	
8. 	Installed below required plugins for this project

	Poll scm
	github integration
	github authentication
	
9.	Go to jenkins dashboard/credentials and add Docker and Github credentials {add docker credentials saperatly for user and password}

10. Now create Declarative pipeline

11. add credentials in jenkins
	
	github (username, token)
	dockerhub (username, token) - make sure you give ID as a "dockerhub"

---------------------

git remote add origin https://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@github.com/Salmankhan7798/vue.js-1.git
git push origin  main
git remote set-url origin https://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@github.com/Salmankhan7798/vue.js-1.git
git remote -v
cp -r (copy)

git token- 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
docker token- dckr_pat_mGOl96IBe_ZmFJmiOA-TiilsQfU

jenkinsurl/github-webhook/

cVG5OL+AIwKDbchTl7Y0mdmshjkOd0ngB89WbqQl

https://faun.pub/how-to-integrate-kubernetes-on-aws-eks-with-jenkins-the-devsecops-way-36d72407f302	

	
