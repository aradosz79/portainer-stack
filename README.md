# portainer-stack
Files to run full CI/CD stack

# Install Portainer

First install Portainer using docker image. Please use following commands:
```
docker volume create portainer_data
docker run -d -p 8000:8000 -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer
```

Now visit http://localhost:9000 and setup your administrative account using admin/admin credentials.

# Install basic stack

To install basic stack first you need prepare a docker directory on the Windows drive d:

```
D:
cd \
mkdir docker
cd docker
mkdir registry grafana
```
Then using web browser go Portainer>LOCAL>Stacks>Add Stack. Select name "CI/CD Stack" and copy content of [basic-stack.yml](basic-stack.yml)

Push 'Deploy the stack' button. Now go http://localhost:3000 and configure access to Grafana using admin/admin credentials.

# Install humio stack

Before installing stack file for Humio please create directories to store his data:


```
D:
cd \docker
mkdir humio kafka-data
```

Go to Portainer> LOCAL > Stack and Add new Stack. Select name "Humio Stack" and copy content of [humio-stack.yml](humio-stack.yml)

