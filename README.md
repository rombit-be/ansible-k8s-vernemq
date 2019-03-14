# VerneMQ on kubernetes

This project uses [Ansible](https://www.ansible.com/) to create the necessary kubernetes config files for deploying VerneMQ on a Kubernetes cluster. After generating it deploys to the chosen cluster.

A couple of Kubernetes concepts have been used:

* A config map for providing the configuration to the pods
* A stateful set to make sure that the pods have persistent storage
* A service to provide the routing to the server
* A pod disruption budget to ensure that when kubernetes reschedules the pods that a certain amount of pods is always available

To deploy your service you should do the following:

* Copy the config.yml.example into a config.yml file
* Run `ansible-playbook create.yml -i environments/<your env>`


Based on: https://github.com/nmatsui/kubernetes-vernemq