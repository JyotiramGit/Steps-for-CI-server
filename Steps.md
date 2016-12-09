error: open /var/run/secrets/kubernetes.io/serviceaccount/token: no such file or director



sudo ssh -i /home/jyo/Downloads/mykey.pem ec2-user@35.160.99.134

sudo ssh -i /home/jyo/Downloads/jyomote.pem ec2-user@172.31.40.254



####### Create CI Server ###############

# install Tomcat

sudo yum install tomcat7 tomcat7-webapps

# Start tomcat service 

sudo service tomcat7 start

# Get Jenkin.war and copy it to tomcat

wget https://jenkins.io/download/


# Install Maven
 
Wget <https://maven.apache.org/download.cgi>

#Set environment variables in ~/.bash_profile


export M2_HOME=/opt/maven/apache-maven-3.3.9

export M2=/opt/maven/apache-maven-3.3.9/bin

export PATH=$M2:$PATH

# genarate archetype- 

mvn archetype:generate -DgroupId=com.jyo -DartifactId=trucks -DarchetypeArtifactId=maven-archetype-webapp -DinteractiveMode=false
 
mvn archetype:generate -DgroupId=com.jyo -DartifactId=CounterWebApp -DarchetypeArtifactId=maven-archetype-webapp -DinteractiveMode=false


#Jyo Mote-
Access Key ID:
AKIAIYFWF62EZPCLXSPQ
Secret Access Key:
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

#
https://122827371149.signin.aws.amazon.com/console

echo "deb https://apt.dockerproject.org/repo ubuntu-trusty main" | sudo tee /etc/apt/sources.list.d/docker.list


# testkitchen Command - 

kitchen init --generate-gemfile --driver=kitchen-docker


knife ec2 server create -r "role[webserver]" -N Git




oc cluster up --public-hostname=ec2-35-160-99-134.us-west-2.compute.amazonaws.com --routing-suffix=35.160.99.134.xip.io

echo "deb https://apt.dockerproject.org/repo ubuntu-trusty main" | sudo tee /etc/apt/sources.list.d/docker.list




