# OctoPrint-docker-pi

This repository contains everything you need to run [Octoprint](https://github.com/foosel/OctoPrint) in a docker environment on ARM/Pi device like Raspberry Pi or Orange Pi.

# Getting started

```
git clone https://github.com/rludwiczak/octoprint-docker-pi octoprint-docker && cd octoprint-docker

# search for you 3D printer serial port (usually it's /dev/ttyUSB0 or /dev/ttyACM0)
ls /dev | grep tty

// edit the docker-compose file to set your 3D printer serial port
vi docker-compose.yml

docker-compose up -d
```

You can then go to http://localhost:5000

You can display the log using `docker-compose logs -f`

# Additional tools

## FFMPEG

Octoprint allows you to make timelapses using an IP webcam and ffmpeg. It is installed in `/opt/ffmpeg`

## Cura Engine

Octoprint allows you to import .STL files and slice them directly in the application. For this you need to upload the profiles that you want to use (you can export them from Cura). Cura Engine is installed in `/opt/cura/CuraEngine`.
