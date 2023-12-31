# kali-railway

Want to try out Kali Linux or want to have a mini version of kali linux available at all times? Then feel free to give this project a try:

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/template/E7oTLJ?referralCode=8sCkKx)


## Description
This project uses the official [kali linux rolling](https://hub.docker.com/r/kalilinux/kali-rolling/) image to deploy a container which can then be used to install most of the cli tools which comes with kali linux pre-installed. Behind the scenes, it uses [ttyd](https://github.com/tsl0922/ttyd) to provide a hassel free and a very accessible way to access the command line.

![image](https://github.com/Mys7erio/kali-railway/assets/25553029/8b338827-fa0c-4dbb-bf06-cba5b0f9d8a5)




## Enviroment Variables
  - **PORT:** The port on which the ttyd program will listen on.
  - **USERNAME:** The username which will be used to login to the web shell.
  - **PASSWORD:** The password which will be used to login to the web shell.

### Railway Default Enviroment Variables
When deploying to Railway, the enviroment variables will have the following default values
  - PORT: Defaults to 8080
  - USERNAME: Defaults to "root"
  - PASSWORD: Defaults to "toor"

**NOTE:** It is strongly adviced to provide the USERNAME and PASSWORD enviroment variables before deploying the project.


## Using locally

```
# Using docker to create an image and run a container locally
# To build the container image
docker build -t kali-railway 

# To run a demo installation on port 8080 with the username set to "admin" and password set to "password"
docker run --rm -e USERNAME=admin -e PASSWORD=password -e PORT=8080 -p 8080:8080 kali-railway
```
