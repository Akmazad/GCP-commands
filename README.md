# GCP-commands

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

#### change a config settings (e.g. set a region)
```shell
gcloud config set redis/region 
```

