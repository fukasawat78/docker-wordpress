# Docker Wordpress w/ efk stack

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

* [Wordpress with efk-stack](#pytorch-template-project)
	* [Usage](#how-to-run)
	* [Organization](#organization)
    * [Acknowledgements](#acknowledgements)

<!-- /code_chunk_output -->

## Usage
Try `docker-compose up -d` to run.

Then, you can access following ports:
* wordpress -> localhost:9000
* kibana -> localhost:5601(index pattern: nginx*)

## Organization

  ```
  docker-efk-wordpress/
    │
    ├── Makefile            <- Makefile with commands like `make data` or `make train`
    ├── README.md           <- The top-level README for developers using this project.
    │
    ├── docker-compose.yml  <- YAML to run docker-compose
    ├── Dockerfile          <- Setup environmemt
    │
    ├── wordpress/
    │ 
    ├── nginx/   
    │   ├── conf.d
    │   │     └── default.conf
    │   ├── log
    │   │     ├── access.log
    │   │     ├── access.log.pos
    │   │     ├── error.log
    │   │     └── locahost.log
    │   └── nginx.conf
    │ 
    ├── fluentd/
    │   ├── config
    │   │     └── fluent.conf
    │   └── Dockerfile
    │ 
    ├── elasticsearch/
    │   └── Dockerfile
    │ 
    ├── db/
    │   └── db-data/
    │ 
    ├── kibana/
    │   └── Dockerfile
    │ 
    └── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
                              generated with `pip freeze > requirements.txt`
  ```
  
## Acknowledgements

