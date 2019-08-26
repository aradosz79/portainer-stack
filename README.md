# portainer-stack
Files to run full CI/CD stack

# Install Portainer

First install Portainer using docker image. Please use following commands:
```
$ docker volume create portainer_data
$ docker run -d -p 8000:8000 -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer
```

Now visit http://localhost:9000 and setup your administrative account.

# Install basic stack

To install basic stack first you need prepare a docker directory on the Windows drive d:

```
D:
cd \
mkdir docker
cd docker
mkdir registry grafana
```
Then using web browser go Portainer>LOCAL>Stacks>Add Stack. Select name "CI/CD Stack" and switch to Build Method: Repository.
'''
Repository URL: https://github.com/aradosz79/portainer-stack.git
Compose path: basic-stack.yml
'''

Push 'Deploy the stack' button

# Install graylog stack

Go to Portainer> LOCAL > Stack and Add new Stack using following Git credentials:

