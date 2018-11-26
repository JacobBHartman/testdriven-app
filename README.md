# testdriven-app

Created on: 26th of November, 2018

All stages of production are located on a Google Cloud Platform Compute Engine instance running Ubuntu 18.04 LTS

Python 3.6.7
Flask 1.0.2
docker-machine was ignored since development was done in the cloud
`docker-compose` was ran with `sudo`

$ docker -v
Docker version 18.03.1-ce, build 9ee9f40
$ docker-compose -v
docker-compose version 1.23.1, build b02f1306


# before you run...
$ python3.6 -m venv env
# run...
$ sudo apt-get install python3-venv

```

During docker setup it was necessary for me to..
`chmod +x ~/testdriven-app/services/users/entrypoint.sh`
manually before docker-compose

When running `docker-compose -f docker-compose-dev.yml run users python manage.py recreate_db` change `recreate_db` to `recreate-db` due to a change in a library used by `docker-compose`
