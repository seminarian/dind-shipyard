#Docker in Docker Shipyard project
## Running the Shipyard project swarm-mode
* git checkout swarm-mode
* In the following lines change "/home/pieter/projecten/shipyard:/shipyard" to the correct path of your shipyard repo.
* docker build . -f dind-compose.dockerfile  -t dind
* docker run -it --privileged -v "/home/pieter/projecten/shipyard:/shipyard" -p "3000:3000" --name dind dind
* In a new terminal tab:
* docker exec dind docker-compose -f shipyard/docker-compose.dev.yml up
* Browse to http://localhost:3000
* log in with admin:shipyard

## Running the Shipyard project from master branch
BROKEN
* git checkout master
*In the following lines change "/home/pieter/projecten/shipyard:/shipyard" to the correct path of your shipyard repo.
* docker build . -f dind-compose.dockerfile  -t dind
* docker run -it --privileged -v "/home/pieter/projecten/shipyard:/shipyard" -p "8000:8000" --name dind dind
* In a new terminal tab:
* docker exec dind docker-compose -f shipyard/docker-compose.yml up
* Browse to http://localhost:8000
* log in with admin:shipyardaaaaaaaaaaaaaaaaaa