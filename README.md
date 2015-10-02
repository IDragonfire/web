# FAForever web project
Corresponds to the main website machine

This repository contains a Dockerfile which allows you to get the main FAForever website running in a virtualized environment (Docker).

The clans, website and patchnotes projects are included as git submodules.

Build the container using

    docker build -t faf/web .

Then run it on your local system using

    docker run -p 80:80 faf/web

Docker container don't share folder by default, this is fine for production system but stop/build/start a container on each code change is not very elegant. You can add a [data volume](http://docs.docker.com/userguide/dockervolumes/#note-for-osx-users-and-remote-daemon-users) over the `-v` flat of the `run` command, e.g.

    docker run -p 80:80 -v <path_to_your_host_folder>:<path_in_the_container> faf/web

  
Happy hacking.

## Useful Commands

Name your container

    docker run -p 80:80 -v <path_to_your_host_folder>:<path_in_the_container> --name faf-web faf/web
    
Connect to your container

    docker exec -ti faf-web bash
