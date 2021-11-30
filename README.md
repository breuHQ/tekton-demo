# tekton-demo
tekton.dev demo for Breu.io

# Installation 

Install `tkn` in your environment

## Linux / Ubuntu / Debian

`sudo apt update;sudo apt install -y gnupg`

`sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 3EFE0E0A2F2F60AA`

`echo "deb http://ppa.launchpad.net/tektoncd/cli/ubuntu focal main"|sudo tee /etc/apt/sources.list.d/tektoncd-ubuntu-cli.list`

`sudo apt update && sudo apt install -y tektoncd-cli`

Then Install Tekton on your cluster

`kubectl apply --filename https://storage.googleapis.com/tekton-releases/pipeline/latest/release.yaml`

## Tekton Dashboard

`kubectl apply --filename https://github.com/tektoncd/dashboard/releases/latest/download/tekton-dashboard-release.yaml`


## Usage 

1. `kubectl proxy --port=8080`
2. `localhost:8080/api/v1/namespaces/tekton-pipelines/services/tekton-dashboard:http/proxy/`
3. `kubectl --namespace tekton-pipelines port-forward svc/tekton-dashboard 9097:9097`


