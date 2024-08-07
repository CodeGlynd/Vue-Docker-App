# Docker Demo project

Project aims to containerize a simple front-end applicaton(vuejs) with building an image using a Dockerfile

----
## Dockerfile flow 

```bash 
#pull node image

FROM node

#set container working directory to /app
WORKDIR /app

#copy all files(application code) in context file 
COPY . .

#install dependencies in package.json file
RUN npm install 

#run script "serve" in package.json file
CMD ["npm", "run", "serve"]

#expose container's port
EXPOSE 8080

```

## Install & Run 

#### clone project 
```bash

git clone https://github.com/LEGO221/Vue-Docker-App.git
```

#### build new image with Dockerfile
```bash
docker build -t <new imagetag> .
```
> make sure you're in working directory of Dockerfile

#### Create & start docker container 
```bash
docker container run -it -p 8080:8080 <image tag>
```
> From webrowser search for http://localhost:8080
