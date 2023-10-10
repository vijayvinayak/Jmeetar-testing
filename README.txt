# jmeter integrate with jenkins-pipeline

##Install Jenkins on EC2 :
    1  sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
    2  sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
    3  sudo yum install java-17-amazon-corretto-devel
    4  sudo yum install jenkins
    5  sudo systemctl start jenkins
    6  sudo systemctl enable jenkins
    7  sudo cat /var/lib/jenkins/secrets/initialAdminPassword
    
 ##Install Jmeter on EC2 :   
    1  sudo yum update -y
    2  wget https://downloads.apache.org/jmeter/binaries/apache-jmeter-5.6.2.tgz
    3  ll
    4  tar -xzf apache-jmeter-5.6.2.tgz
    5  sudo mv apache-jmeter-5.6.2 /opt/jmeter
    6  echo 'export JMETER_HOME="/opt/jmeter"' >> ~/.bashrc
    7  echo 'export PATH="$PATH:$JMETER_HOME/bin"' >> ~/.bashrc
    8   source ~/.bashrc
    9   jmeter --version
    
##Install Jmeter Plugin in Jenkins :
   Plugin Name : Performance
   
##write a pipeline script for jmeter performance test :
##note : In github repository-add jenkinsfile and test-plan.jmx file 
