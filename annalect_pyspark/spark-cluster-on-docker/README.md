# Apache Pyspark Standalone Cluster on Docker


## Contents

- [Quick Start](#quick-start)
- [Tech Stack](#tech-stack)


## <a name="quick-start"></a>Quick Start

### Cluster overview

| Application     | URL                                      | Description                                                |
| --------------- | ---------------------------------------- | ---------------------------------------------------------- |
| JupyterLab      | [localhost:8888](http://localhost:8888/) | Cluster interface with built-in Jupyter notebooks          |
| Spark Driver    | [localhost:4040](http://localhost:4040/) | Spark Driver web ui                                        |
| Spark Master    | [localhost:8080](http://localhost:8080/) | Spark Master node                                          |
| Spark Worker I  | [localhost:8081](http://localhost:8081/) | Spark Worker node with 1 core and 512m of memory (default) |
| Spark Worker II | [localhost:8082](http://localhost:8082/) | Spark Worker node with 1 core and 512m of memory (default) |

### Prerequisites

 - Install [Docker](https://docs.docker.com/get-docker/) and [Docker Compose](https://docs.docker.com/compose/install/), check **infra** [supported versions](#tech-stack)

### Download from Docker Hub (easier)

1. Download the [docker compose](docker-compose.yml) file;

```
brew install docker-compose
```

3. Start the cluster;

```bash
docker-compose up
```

4. Run Apache Spark code using the provided Jupyter [notebooks](build/workspace/):
5. Stop the cluster by typing `ctrl+c` on the terminal;
6. Run step 3 to restart the cluster.

### Build from your local machine

> **Note**: Local build is currently only supported on Linux OS distributions.

1. Download the source code or clone the repository;
2. Move to the build directory;
```bash
cd build
```
3. Start the cluster;

```bash
docker-compose up
```
4. Run Apache Spark code using the provided Jupyter [notebooks](build/workspace/);
5. Stop the cluster by typing `ctrl+c` or the command specified below on the terminal;
```bash
docker-compose kill
```
7. Run step 6 to restart the cluster.
8. Open the notebook Take_home_assignment.ipynb
9. Execute the notebook for solutions to the take home assignment
10. The necessary dataset are present in the data folder 