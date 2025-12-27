# JENKINS SETUP

### PARTITION THE DISK
```
growpart /dev/nvme0n1 4

lvextend -L +10G /dev/mapper/RootVG-varVol
lvextend -L +10G /dev/mapper/RootVG-rootVol
lvextend -l +100%FREE /dev/mapper/RootVG-homeVol

xfs_growfs /
xfs_growfs /var
xfs_growfs /home
```
### INSTALL COMMANDS FROM JENKINS OFFCIAL DOC
```
sudo curl -o /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
```
```
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
```
```
sudo yum install fontconfig java-21-openjdk -y
```
```
sudo yum install jenkins -y
```
```
sudo systemctl daemon-reload
sudo systemctl start jenkins
sudo systemctl enable jenkins
```

### Plugins
* Stage view

### Master Agent Architecture
* Create credentials to connet agent
* Install java in agent
* Select Non Verifiction strategy

# AGENT 

### PARTITION THE DISK

```
growpart /dev/nvme0n1 4

lvextend -L +10G /dev/mapper/RootVG-varVol
lvextend -L +10G /dev/mapper/RootVG-rootVol
lvextend -l +100%FREE /dev/mapper/RootVG-homeVol

xfs_growfs /
xfs_growfs /var
xfs_growfs /home
```
### in agent we install java also
```
sudo yum install fontconfig java-21-openjdk -y
```


