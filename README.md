

# Pre-Reqs:

  - Docker Community edition latest version

# Build:

  - Go to the root folder of the project and run below command.
  
  	*docker build -t april:\<Version\> .*

# Deploy:

- Single container:

*docker run --name april-app -p 80:80 -p 443:443 -d april:\<Version\>*

- Docker Stack in Swarm mode:

If you are running locally, make sure to initialize swarm 

*docker swarm init*

Then,

*docker stack deploy -c docker-compose.yml april-service*
