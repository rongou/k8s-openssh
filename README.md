# k8s-openssh
OpenSSH test on Kubernetes.

* Build docker image with OpenSSH:
```shell
docker built -t rongou/openssh .
```
* Push it to docker hub:
```shell
docker push rongou/openssh
```
* Create k8s `Secret` containing the ssh keys:
```shell
./create-secret.sh
```
* Test ssh communication:
```shell
kubectl create -f openssh-test.yaml
```
