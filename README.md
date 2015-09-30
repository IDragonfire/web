# FAForever web project
Corresponds to the main website machine

This repository contains a Dockerfile which allows you to get the main FAForever website running in a virtualized environment (Docker).

The clans, website and patchnotes projects are included as git submodules.

Build the container using

    docker build -t faf/web .

Then run it on your local system using

    docker run -p 80:80 faf/web


Happy hacking.
