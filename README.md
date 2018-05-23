

# Pre-Reqs:

  - Docker Community edition latest version

# Build:

  - Go to the root folder of the project and run below command.
  
  	*docker build -t april:\<Version\> .*

# Deploy:

Single container:

*docker run --name april-app -p 80:80 -p 443:443 -d april:\<Version\>*

Docker Stack in Swarm mode:

If you are running locally, make sure to initialize swarm 

*docker swarm init*

Then use the docker-compose.yml in the root folder to deploy the application image:

*docker stack deploy -c docker-compose.yml april-service*

# Get to Application:

Application will be running on 80 and 443 of the Host you are running on, Ports can changed in the docker-compose.yml.

https://localhost
