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

# Install graylog stack

Go to Portainer> LOCAL > Stack and Add new Stack using following Git credentials:

