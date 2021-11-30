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


