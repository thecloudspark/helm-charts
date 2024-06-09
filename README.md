# Helm Charts

This repository hosts a collection of Helm charts for deploying various applications and services on Kubernetes clusters. Helm charts provide a convenient way to define, install, and manage Kubernetes applications.

## Usage
To use these Helm charts, you'll need to have Helm installed on your local machine and configured to connect to your Kubernetes cluster. Once Helm is set up, you can add this repository to your Helm client and start deploying applications.


### Adding the Repository
To add this Helm repository to your local, run the following command:

```bash
helm repo add thecloudspark https://thecloudspark.github.io/helm-chart
```  

### Installing Charts
After adding the repository, you can search for available charts and install them using Helm commands. For example, to install the `vote-app` chart:

```bash
helm install app thecloudspark/vote-app
```

## Available Charts
Here's the list of available charts:  
[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/vote-app)](https://artifacthub.io/packages/search?repo=vote-app)

## Contributing
Contributions to this repository are welcome! If you have improvements to existing charts or new charts to add, please open a pull request. Make sure to follow the contribution guidelines outlined in the repository.