# Tekton-CI-CD
<h1> Getting started with Tekton </h1>

<h2> Setting up Tekton </h2>
<p> This is pre-requisite setup to interact with things like github.com and docker image registries </p>

1. Generating ssh key:
```
ssh-keygen -t ed25519 -C "<your mail id>"
cat /home/.ssh/id_ed25519.pub
```
Copy the output from cat command for next step

2. Upload the key to github

Go to github settings->SSH and GPG keys->New SSH key

3. Creating Kubernetes secret
  
Assuming you are logged into kubernetes,run the following command to create the secret
```
kubectl create secret generic <secret name> --type=kubernetes.io/ssh-auth --from-file="path to your ssh file, eg: id_ed25519"
kubectl annotate secrets <secret name> tekton.dev/git-0=github.com
```
