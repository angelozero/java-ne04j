# Neo4j
![neo4j](https://dist.neo4j.com/wp-content/uploads/20170726233003/hello-world-neo4j-inc-company-name-change.png)

---
 ## What is Neo4J ?
 - Neo4j is a graph database (NoSQL)
 - Is a collection of nodes and relationships between nodes.

---
## Node & Relationship
![image](https://github.com/angelozero/java-ne04j/assets/8808207/a5082a18-49dd-47d0-bc83-141002a007d0)


---
## Properties in relations
![image](https://github.com/angelozero/java-ne04j/assets/8808207/95ae61ba-4bfc-42e3-a6a7-150249a9bbd5)

---

## Using Neo4J on Docker
 - How to Deploy a Neo4j cluster in a [Docker](https://neo4j.com/docs/operations-manual/current/tutorial/tutorial-clustering-docker/) container

```yml
version: '3.8'

services:
  neo4j:
    # Docker image to be used
    image: neo4j:5.16.0-enterprise

    # Hostname
    hostname: neo4j-db

    # The ports that will be accessible from outside the container - HTTP (7474) and Bolt (7687).
    ports:
      - "7474:7474"
      - "7687:7687"
    
    # Volumes
    volumes:
      - ./db/data:/data
      - ./db/conf:/conf
      - ./db/logs:/logs
      - ./db/plugins:/plugins
      
    # Passes the following environment variables to the container
    environment:
      - NEO4J_AUTH=neo4j/terra123
      - NEO4J_ACCEPT_LICENSE_AGREEMENT=yes
```

---

## Creating the first database 
 - On your browser after run `docker-compose up` on the docker-compose.yml file, access the url http://localhost:7474/browser/
 - On `neo4j$` terminal to create type: `create database student` or to delete type: `drop database student`
