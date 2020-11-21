# Jfrog Artifactory Installation

#### JFrog Artifactory is an open-source repository management application that can be integrated with continuous integration and delivery tools. It is a cross-platform tool that allows DevOps to manage multiple package repositories. It provides high availability and multi-site replication to automate your pipeline and enable faster releases
```
sudo apt-get update 
```
#### First, install Gnupg2 package with the following command:
```
apt-get install gnupg2 -y
```

#### Next, download and add the GPG key with the following command:
```
wget -qO - https://api.bintray.com/orgs/jfrog/keys/gpg/public.key | apt-key add -
```
#### Next, add the JFrog Artifactory repository with the following command:
```
echo "deb https://jfrog.bintray.com/artifactory-debs bionic main" | tee /etc/apt/sources.list.d/jfrog.list
```
#### Once the repository is added, update the repository and install JFrog Artifactory with the following command:
```
apt-get update -y
```
```
apt-get install jfrog-artifactory-oss -y
```

#### Next, start the Artifactory service and enable it to start at system reboot with the following command:
```
systemctl start artifactory
```
```
systemctl enable artifactory
```
```
systemctl status artifactory
```


#### Add port 8082 in security group for the jfrog artifactory 

### In the dashboard of jfrog artifactory put admin as a username and password as a password. 
