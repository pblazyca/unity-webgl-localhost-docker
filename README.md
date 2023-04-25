## :coffee: Simple Unity WebGL Runner
A simple tool that leverages Docker to create a local server for testing a Unity-built WebGL application.

## prerequisites
- [Docker](https://www.docker.com/) 

## how to use?
### init
1. download or clone this repo
2. place the Unity WebGL build output in the directory `ROOT/source/app`

### start localhost
1. open Terminal or Command Prompt in the root directory (containing the `docker-compose.yaml` file)
2. to begin, run `docker-compose up -d`
3. navigate to http://localhost:4044/ in any browser

### stop localhost
- run `docker-compose down`

### rebuild docker image and start localhost after changes in `app` or configs
- run `docker-compose up --force-recreate --build -d`

## tech stuff
- used [nginx:alpine](https://hub.docker.com/_/nginx) docker image.
- server configuration based on [Unity default configuration](https://docs.unity3d.com/Manual/webgl-server-configuration-code-samples.html).
- ensure webgl apps that utilize `gzip` or `brotli` compression work properly.
- by deafult used localhost port `4044:80`

## contribution
utilizing these awesome sources:
- https://github.com/tomowatt/unity-docker-example
- https://dev.to/tomowatt/running-an-unity-webgl-game-within-docker-5039
