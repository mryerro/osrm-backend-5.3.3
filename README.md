# Dockerfile for osrm-backend
This container run [osrm-backend](https://github.com/Project-OSRM/osrm-backend) project.
Open Source Routing Machine (OSRM) Docker Image [\[Docker Hub\]](https://hub.docker.com/r/cartography/osrm-backend-docker/)

## Installation

1. Install [Docker](https://www.docker.com/)

2. Manual deploy.

  $ docker build -t un/osrm-backend .
  ```

## Usage
Run it:  
```
docker run -d -p 5000:5000 --name osrm-api un/osrm-backend:latest osrm Spain "http://download.geofabrik.de/europe/spain-latest.osm.pbf"
```  

Explanation:  
- `-d` - run container in background and print container ID 
- `-p 5000:5000` - publish a container port to host
- `osrm` - go via entrypoint script, w/o osrm keyword - classic mode
- `label` - your label of OSM data
- `url` - link to OSM data in PBF format
