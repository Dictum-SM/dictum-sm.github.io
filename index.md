## Dictum State Machine (DSM)
Extensible framework and application for managing everything with GitOps.

### Declare all the things
Centrally manage everything from one source including:
- Kubernetes
- Terraform
- Ansible  

### Git Native

Written in Bash, the DSM is purpose built to be added to any git repo as a submodule for easy versioning and extensibility.

The DSM is initialized similarly to git, with a `.state` file located at the git repo root. This `.state` file holds an index of all configurations to be applied to a target environment contained within the git repo.

### Portable
Run it at home or from a workflow automation, the DSM should always produce the same output defined within the `.state` file by configuring an environment with ony resources defined within the git repo. 

### Easy
Apply a resource by creating a key/value pair in the `.state` file and running the DSM. 

Does the resource have a dependency? Add another key/value pair to the `.state` file that executes a health check between applying configs.

Update the environment with a change to a configuration by running the DSM again.

Delete a resource by removing it fom the `.state` file and running the DSM again.

Add any combination of configurations (ie. kubectl/helm/teraform/ansible-playbooks) and helper utilities (health checking, credential retrieval, other preparation) to achieve the desired state of an environment. 




