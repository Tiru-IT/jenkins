### MASTER 
```
sudo curl -o /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
```
```
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
```
# Add required dependencies for the jenkins package
```
sudo yum install fontconfig java-21-openjdk -y
```

```
sudo yum install jenkins -y
```

```
sudo systemctl daemon-reload
```

```
sudo systemctl start jenkins
sudo systemctl enable jenkins
```

```
lsblk
sudo growpart /dev/nvme0n1 4
sudo lvextend -L +20G /dev/mapper/RootVG-homeVol
sudo lvextend -L +10G /dev/mapper/RootVG-rootVol
sudo xfs_growfs /
sudo xfs_growfs /home
```


# in agent we install java also
```
sudo growpart /dev/nvme0n1 4
sudo lvextend -L +20G /dev/mapper/RootVG-homeVol
sudo lvextend -L +10G /dev/mapper/RootVG-rootVol
sudo xfs_growfs /
sudo xfs_growfs /home
```


# in agent we install java also
```
sudo yum install fontconfig java-21-openjdk -y
```



