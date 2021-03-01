# Minikube CheatSheet
## Basic Commands
* Start Minikube
```
$ minikube start
```
* Stop Minikube
```
$ minikube stop
```
* Check Minikube Status
```
$ minikube status
```
* Delete Minikube
```
$ minikube delete
```
## Advanced Commands
### profile
* Default Profile
```
$ minikube start --vm-driver=virtualbox
```
* New Profile
```
$ minikube start --vm-driver=virtualbox -p <profile-name>
```

* Profile/Cluster with specific resources (CPU and RAM)
```
$ minikube start --vm-driver=virtualbox -p <profile-name> --cpus=2 --memory=2048
```
* List different profiles/clusters
```
$ minikube profile list
```
* Delete Profile/Cluster
```
$ minikube delete -p <profile-name>
```
* Delete all Profiles/Clusters
```
$ minikube delete --all
```
### dashboard
* Accessing Dasboard for default profile/cluster
```
$ minikube dashboard
```
* Accessing Dashboard for specific profile/cluster
```
$ minikube dashboard -p <profile-name>
```
* Get Dashboard URL
```
$ minikube dashboard --url
```
### service
* List Services of default profile/cluster
```
$ minkube services list 
```
* List Services of specific profile/cluster
```
$ minkube services list -p <profile-name>
```
* Get service URL
```
$ minikube service --url <service-name>
```
### ip
* View ip of default profile/cluster
```
$ minikube ip
```
* View ip of specific profile/cluster
```
$ minikube ip -p <profile-name>
```
### ssh
* SSH minikube node environment
```
$ minikube ssh
```
* Retrive ssh-host key of minikube node
```
$ minikube ssh-host
```
* Retrive ssh-key identity path
```
$ minikube ssh-key
```
### addons
* List addons supported by minikube
```
$ minikube addons list
```
* Enable addons
```
$ minikube addons enable <addon-name>
```
* Disable addons
```
$ minikube addons disable <addon-name>
```
### minikube kubectl
* For default profile/cluster
```
$ minikube kubectl get pods
$ minikube kubectl get services
$ minikube kubectl get deployment
```
* For specific profile/cluster
```
$ minikube kubectl get pods -p <profile-name>
$ minikube kubectl get services -p <profile-name>
$ minikube kubectl get deployment -p <profile-name>
```
### docker-env
* Point terminal to minikube docker enviroment
```
$ eval $(minikube docker-env)
```
* Detach terminal from minikube docker enviroment
```
$ eval $(minikube docker-env -u)
```
###  [Note: Follow this link to refer more advanced commands with flags](https://minikube.sigs.k8s.io/docs/commands/)

## Useful Links for Reference 
* [Minikube Official Documentation](https://minikube.sigs.k8s.io/docs/)
* [Github Repository](https://github.com/kubernetes/minikube)
* [Minikube Tutorials](https://minikube.sigs.k8s.io/docs/tutorials/)
