# masters_prject_chandu_fuldev "The project going on full stack development with devops"

## docker:

- command to install docker "sudo apt-get install docker-ce docker-ce-cli containerd.io"
- docker run -p 8080:8080 <image_name>

## Jenkins:
- command to install jenkins :- sudo apt install openjdk-11-jdk -y
- sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian/jenkins.io-2023.key
  echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
- sudo apt-get update
- sudo apt-get install jenkins
- for chnaging the port we need to modify in 2 files one is from jenkins(.../etc/default/jenkins) and another in service file need to change the port in this project the jenkins running on 8085 port
## kubernetes and kubectl download guide.
### this is for linux X86-64 that i am using now
- curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
Validate the binary
- curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"
### Validate the kubectl binary against the checksum file:
- echo "$(cat kubectl.sha256) kubectl" | sha256sum --check
### if you validate the output as "kubectl: OK" then its fine.
- install Kubectl
- sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
### check the version
- kubectl version --client

### kubernetes command to install minikube
- curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb
- sudo dpkg -i minikube_latest_amd64.deb

### Start minikube 
- minikube start --force

- minikube status

