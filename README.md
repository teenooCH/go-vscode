# go-vscode
## Go (Golang) plus Visual Studio Code (VSC) Editor Docker image.

This image provides
- Go language
- some of the tools usefull for the development of Go programs.
  see [teenooch/golang-plus] (https://hub.docker.com/r/teenooch/golang-plus/)
- Visual Studio Code Editor
- Visual Studio Code extensions
  - code outline
  - docker
  - git history
  - git tags
  - go
  - go tdd
  - vim
- a basic configuration of vsc

Vsc is run as user vscode. Working directory is /go.

To create a container :
```
  docker run -d -v /tmp/.X11-unix/:/tmp/.X11-unix/ -v /dev/shm/:/dev/shm/ -v /home/myuser/go/src/:/go/src/ -v /home/myuser/dev/:/home/vscode/dev/ -e DISPLAY=$DISPLAY --name go-vscode teenooch/go-vscode
```
Make sure you are allowed to open the display. If not try xhost +local:
