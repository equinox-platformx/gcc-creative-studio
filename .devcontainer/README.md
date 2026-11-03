# GCC Creative Studio Codespace

## Overview
This GitHub Codespace is pre-configured with the necessary tools and extensions to run Terraform on the repository.

## Google Cloud CLI

https://docs.cloud.google.com/sdk/docs/initialize

Within the container install the `gcloud` utility:

```
# Update and Install Prerequisites
sudo apt-get update
sudo apt-get install apt-transport-https ca-certificates gnupg curl -y

# Add the Google Cloud Public Key
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo gpg --dearmor -o /usr/share/keyrings/cloud.google.gpg

# Add the Repository to your Package Sources
echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] https://packages.cloud.google.com/apt cloud-sdk main" | sudo tee /etc/apt/sources.list.d/google-cloud-sdk.list

# Install the CLI
sudo apt-get update && sudo apt-get install google-cloud-cli -y
```

```zsh
# initialize CLI & login
gcloud init

# just login
gcloud auth login
gcloud auth login --no-launch-browser

# check current user
gcloud auth list

# config info
gcloud info

# see a roster of go-to `gcloud` commands
gcloud cheat-sheet
```
