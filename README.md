# velociraptor-docker
Run [Velocidex Velociraptor](https://github.com/Velocidex/velociraptor) server with Docker
- This Project is forked from Wes Lambert's Velociraptor Docker project. 
- This will install Elasticsearch, kibana and velociraptor.

#### Install

- Ensure [docker-compose](https://docs.docker.com/compose/install/) is installed on the host
- `git clone https://Mastadamus@dev.azure.com/Mastadamus/Velociraptor-ElasticSearch-Kibana/_git/Velociraptor-ElasticSearch-Kibana`
- `cd ./Velociraptor-ElasticSearch-Kibana`
- Change credential values in `.env` as desired
- to run detached enter `docker-compose up -d` or if your prefer to watch the containers come up `docker-compose up`
- Access the Velociraptor GUI via https://\<hostip\>:8889 
  - Default u/p is `admin/admin`
  - This can be changed by running: 
  
  `docker exec -it velocraptor ./velociraptor --config server.config.yaml user add user1 user1 --role administrator`

#### Notes:

Linux, Mac, and Windows binaries are located in `/velociraptor/clients`, which should be mapped to the host in the `./velociraptor` directory if using `docker-compose`.  There should also be versions of each automatically repacked based on the server configuration.

Once started, edit `server.config.yaml` in `/velociraptor`, then run `docker-compose down/up` for the server to reflect the changes

#### Docker image
To pull only the Docker image:

`docker pull wlambert/velociraptor`
