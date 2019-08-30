# portainer-stack
Files to run full CI/CD stack

# Install Portainer

First install Portainer using docker image. Please use following commands:
```
docker volume create portainer_data
docker run -d -p 8000:8000 -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer
```

Now visit http://localhost:9000 and setup your administrative account using admin/admin credentials.

# Install Docker Registry

Now it is time to install our own private Docker registry. Execute following in the cmd:

```
D:
cd \
mkdir docker
cd docker
mkdir grafana
```

Then using web browser go to Portainer>LOCAL>Stacks>Add Stack. Select name "registry" and copy content of [registry-stack.yml](registry-stack.yml). Push 'Deploy the stack' button.

# Install puma stack

To install Puma monitoring stack first you need prepare a docker directory on the Windows drive d:

```
D:
cd \
mkdir docker
cd docker
mkdir grafana
```
Then using web browser go Portainer>LOCAL>Stacks>Add Stack. Select name "cicd" and copy content of [basic-stack.yml](basic-stack.yml) changing password to Splunk.

Push 'Deploy the stack' button. Now go http://localhost:3000 and configure access to Grafana using admin/admin credentials.
