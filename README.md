# GCP-commands Essentials for Ubuntu users

## Installation

### On UBUNTU/Debian:
#### 1. Add the Cloud SDK distribution URI as a package source:
```shell
echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] https://packages.cloud.google.com/apt cloud-sdk main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list
```

#### 2. Import the Google Cloud public key:
```shell
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key --keyring /usr/share/keyrings/cloud.google.gpg add -
```
#### 3. Update and install the Cloud SDK:
```shell
sudo apt-get update && sudo apt-get install google-cloud-sdk
```

#### 4. Optionally, install any of these additional components:
```shell
google-cloud-sdk-app-engine-python
google-cloud-sdk-app-engine-python-extras
google-cloud-sdk-app-engine-java
google-cloud-sdk-app-engine-go
google-cloud-sdk-bigtable-emulator
google-cloud-sdk-cbt
google-cloud-sdk-cloud-build-local
google-cloud-sdk-datalab
google-cloud-sdk-datastore-emulator
google-cloud-sdk-firestore-emulator
google-cloud-sdk-pubsub-emulator
kubectl
```
#### 5. Run ```gcloud init``` to start:
```shell
gcloud init
```

## Configuration

### See default configuration setting
#### compact list
```shell
gcloud config list
```
#### detailed list
```shell
gcloud config list --all
```

#### list all the projects
```shell
gcloud projects list
```

#### change a config settings (e.g. set a current project to a project, namely 'HelloGCPWorld' with ID as 'hellogcpworld')
```shell
gcloud config set project hellogcpworld 
```

#### see all the list of regions
```shell
gcloud redis zones list
```
This may generate a prompt like
```
API [redis.googleapis.com] not enabled on project [897975539982]. 
Would you like to enable and retry (this will take a few minutes)? 
(y/N)
```
chose ```Y```.

#### set the zone for the current project
```shell
gcloud config set compute/zone asia-east1-b
```
#### disable prompt
```shell
gcloud config set disable_prompts true
```

#### set up a proxy (type, address and port)
```shell
gcloud config set proxy/type http
gcloud config set proxy/address 127.0.0.0
gcloud config set proxy/port 8080
```


