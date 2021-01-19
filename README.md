# shipmmg_control

This repository is just for testing MPC control of ShipMMG.

## How to use

### By using docker-compose.yml
1. [Install Docker](https://docs.docker.com/get-docker/) in your PC.

1. [Install Docker Compose](https://docs.docker.com/compose/install/) in your PC.

1. Get this repository.
    ```sh
    $ git clone https://github.com/shipmmg/shipmmg_control.git 
    ```

1. Build.
    ```sh
    $ cd shipmmg_control
    $ docker-compose build
    ```

1. Run.
    ```sh
    $ docker-compose up
    ```

1. Access [http://localhost:8888/](http://localhost:8888/)
    - Default access token is `shipmmg_control`. Please change this access token by editing Dockerfile.
