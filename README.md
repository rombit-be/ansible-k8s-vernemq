# ansible-k8s-vernemq

Install VerneMQ cluster on your Kubernetes cluster with Ansible.

Requirements
------------

A working kubernetes cluster, starting from 1.6.* RBAC enabled.

Role Variables
--------------
* k8s_action (required): Either 'create' or 'delete'. Determines whether we should deploy or delete. 
* cluster_context: The cluster you want to deploy to
* cluster_namespace: The namespace you want to deploy to
* aws_region: The region of AWS you're working in (ex: us-east-1)
* route53_zone: The name of the zone you want to use for the external loadbalancer (ex: example.com)
* acm_ssl_cert: The ARN of the certificate for that route53_zone (this certificate will be linked to the external loadbalancer for SSL offloading). It needs to be an SSL-certificate for the domain you're using in `route53_zone`.


Author Information
------------------
Jo Giraerts <<devops@rombit.be>>
