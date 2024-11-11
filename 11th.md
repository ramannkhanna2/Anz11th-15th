```

Welcome to OpenDev Etherpad!

Docker demo :


github repo : https://github.com/ramannkhanna2/Anz11th-15th.git


 -- created a server aws/gcp/azure :
     
 ubuntu , 10gb storage , 1 vcpu , 1 gb ram
 

 
 
 
 
 log into the server :
     
     sudo -i

     
     docker installation :

  https://docs.docker.com/engine/install/ubuntu/
 
 
 
 
 
 
 
 
 operations :
     
     -itd
     
     
     i interactiveness
     t : terminal
     d : detached mode 
 
 
 
 
 root@ip-172-31-22-252:~/nodejsapp_jenkins-docker-kubernetes# history
    1  cat /etc/os-release 
    2  ls
    3  clear
    4  docker
    5  # Add Docker's official GPG key:
    6  sudo apt-get update
    7  sudo apt-get install ca-certificates curl
    8  sudo install -m 0755 -d /etc/apt/keyrings
    9  sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
   10  sudo chmod a+r /etc/apt/keyrings/docker.asc
   11  # Add the repository to Apt sources:
   12  echo   "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" |   sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
   13  sudo apt-get update
   14  sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
   15  docker ps
   16  docker images
   17  docker -v
   18  clear
   19  history
   20  clear
   21  git clone https://github.com/ramannkhanna2/nodejsapp_jenkins-docker-kubernetes.git
   22  ls
   23  cd nodejsapp_jenkins-docker-kubernetes/
   24  ls
   25  docker images
   26  rm -rf Jenkinsfile Jenkinsfile2 deploy.tf deploymentservice.yml openshiftdeploymentfile.yaml 
   27  ls
   28  docker -v
   29  systemctl status docker
   30  docker -h
   31  clear
   32  ls
   33  docker run -it --name c1 httpd
   34  docker ps
   35  docker ps -a
   36  docker rm -f c1
   37  clear
   38  docker run -it --name c1 ubuntu
   39  docker images
   40  docker ps
   41  docker run -itd --name c1 centos:7
   42* docker 
   43  docker ps
   44  docker run -d --name c3 httpd
   45  docker ps
 
 
    docker run -td --name c4 centos:7
 
  history
   47  docker ps
   48  docker ps -a
   49  docker attach c3
   50  docker ps -a
   51  docker ps -adocker start c3
   52  docker start c3
   53  docker ps
   54  docker attach c1
   55  docker run -td --name c4 centos:7
   56  docker images
   57  docker ps
   58  docker attach c4
   59  docker ps
   60  docker ps -a
   61  docker exec -it c3 /bin/bash
   62  docker exec -it c3 mkdir khanna
   63  docker exec -it c3 ls
 clear
   66  history
   67  clear
   68  ls
   69  cat dockerfile 
   70  ls
   71  cat index.js 
   72  docker ps
   73  docker exec -it c3 /bin/bash
   74  -adocker ps 0a
   75  docker ps -a
   76  docker images
   77  docker -h
   78  clear
   79  docker images
   80  docker build -t customimage .
   81  docker images
   82  docker customimage history
   83  docker  history customimaqge
   84  docker  history customimage
   85  clear
   86  docker ps -a
   87  docker images
   88  docker stats
   89  docker images
   90  docker run -d --name c5 customimage
   91  docker ps
   92  docker inspect c5
   93  ip a
   94  clear
   95  docker ps
   96  docker inspect c5
   97  curl 172.17.0.6
   98  docker ps
   99  curl 172.17.0.6:3000
  100  ls
  101  cat index.js 
  102  curl 172.17.0.6:3000/ready
  103  docker ps
  104  docker run -d -P --name c6 customimage
  105  docker ps
  106  docker run -d -p 81:3000  --name c6 customimage
  107  docker run -d -p 81:3000  --name c7 customimage
  108  docker ps
 
 
 
 
  code >> dockerfile  >> dockerbuild >> custom image   >> container 
 
 
 https://docs.docker.com/reference/dockerfile/
 
 
 
 
 
 root@ip-172-31-22-252:~/nodejsapp_jenkins-docker-kubernetes# cat dockerfile 
FROM node:latest

WORKDIR /usr/src/app

COPY package.json ./

RUN npm install

COPY . .

EXPOSE 3000
CMD [ "node", "index.js" ]
 
 
 
 
 
 
 
 
 

 
 kubernetes :
     
     
     
     master node : management containers 
         
         
         worker nodes : application containers
         
https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/high-availability/


https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/


https://kubernetes.io/docs/reference/networking/ports-and-protocols/


https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/create-cluster-kubeadm/



         
         
===============================================================================================







kubectl get nodes -A
kubectl get pods -A -o wide 


==============================================


```
