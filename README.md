# karbo-node-service
------
Script package for docker-compose which provides [karbo](https://karbo.io/en) (KRB) master node as a service.

## How to install
------
1. Prepare environment ([link1](https://docs.docker.com/install/linux/docker-ce/ubuntu/), [link2](https://docs.docker.com/compose/install/))
2. Clone that repository
3. Create directory in your host which will store blockchain
4. Edit .env file for setting your optimal preferences
5. *Optional* download blockchain bootstrap with next command:
... `docker-compose run karbo-blockchain-preloader`
6. Run your node with next command:
... `docker-compose up -d karbo-node-service`

## Usage
------
`docker-compose up -d karbo-node-service` - starts up node service

`docker-compose run karbo-blockchain-preloader` - downloads ready-to-use blockchain (read more [here](https://forum.karbo.io/viewtopic.php?f=13&t=203))

`docker-compose logs karbo-node-service` - shows log tty of the node

`docker-compose stop karbo-node-service` - stops the node


## How to maintain
------
### Get a newer node release
1. `docker-compose stop karbo-node-service`
2. `docker-compose pull`
3. `docker-compose up -d karbo-node-service`

## License
------
See LICENSE file