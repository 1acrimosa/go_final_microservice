# Go Final Project

Architecture of our project, how can you see we used three different UI and connected with mongoDB, PostgreDB and Golang.


<p align="center"> 
<img src="./diagram.png" width="500" />
</p>

This project contains microservices written in Go (gRPC Servers) and their envoy proxy configurations for establishing connection through gRPC-Web with the client (UI). gRPC Unary and gRPC Server-side Streaming examples are available in the services.

|            | gRPC Unary | gRPC Server-side Streaming |
| :--------: | :--------: | :------------------------: |
| Catalog Server |     ✅     |                            |
|  Offer Server  |            |             ✅             |
|  Order Server  |     ✅     |             ✅             |

![](./ui.gif)

## Installation

Make sure Docker is running.

First, clone the repository

```bash
git clone https://github.com/uid4oe/grpc-web-demo.git
```

Then, open a terminal window from the root of the project.
We will just need to create network & execute the `docker-compose` command

```bash
docker network create grpc-web-demo-alva-net
docker-compose up -d
```

At this point everything should be up and running!

You can track service logs from containers: `catalog`, `offer`, `order`.

You can access to UI at

```bash
http://localhost:3000
```
