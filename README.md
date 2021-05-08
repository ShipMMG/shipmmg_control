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
    $ docker-compose build # --no-cache if nessecary
    ```

1. Run.
    ```sh
    $ docker-compose up
    ```

1. Access [http://localhost:8888/](http://localhost:8888/)
    - Default access token is `shipmmg_control`. Please change this access token by editing Dockerfile.

### By using Dockerfile

1. Build & Run

    - Run and Save the notebooks on your current directory in your Linux or MacOS PC
        ```sh
        $ docker build -t shipmmg-control . # --no-cache should be added after updating Dockerfile
        $ docker run --rm --name shipmmg-control -d -p 8888:8888 -v $(pwd)/notebooks:/notebooks -w /notebooks shipmmg-control jupyter-lab --no-browser --port=8888 --ip=0.0.0.0 --allow-root --NotebookApp.token='shipmmg_control'
        ```

    - Run and Save the notebooks on your current directory in your Windows PC
        ```sh
        $ docker build -t shipmmg-control . # --no-cache should be added after updating Dockerfile
        $ docker run --rm --name shipmmg-control -d -p 8888:8888 -v ${pwd}/notebooks:/notebooks -w /notebooks shipmmg-control jupyter-lab --no-browser --port=8888 --ip=0.0.0.0 --allow-root --NotebookApp.token='shipmmg_control'
        ```

1. Access [http://localhost:8888/](http://localhost:8888/)
    - Default access token is `shipmmg_control`. Please change this access token.

1. Kill image after finishing.
    ```sh
    $ docker kill shipmmg-control
    ```
