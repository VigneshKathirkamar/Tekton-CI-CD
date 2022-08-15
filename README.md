# Tekton-CI-CD
<h1> Getting started with Tekton <h1>

<h2> Setting up Tekton <h2>
<p> This is pre-requisite setup to interact with things like github.com and docker image registries </p>

1. Generating ssh key:
```
ssh-keygen -t ed25519 -C "<your mail id>"
cat /home/.ssh/id_ed25519.pub
```
Copy the output from cat command for next step

2. Upload the key to github

Go to github settings->SSH and GPG keys->New SSH key
