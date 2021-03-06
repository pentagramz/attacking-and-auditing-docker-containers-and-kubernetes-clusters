# Auditing Docker Runtime and Endpoints

* Checking for the docker daemon configuration

```bash
docker system info
```

![docker system info](images/docker-system-info.png)

* Checking for the docker API exposed on `0.0.0.0`

```bash
sudo cat /lib/systemd/system/docker.service
```

![docker using tcp socket](images/docker-tcp-socket.png)

* Checking if the docker socket is mounted to any running container

```bash
docker inspect | grep -i '/var/run/'
```

![docker inspect for socket](images/docker-inspect-for-socket.png)

* Checking other files and data related to docker

```bash
sudo ls -l /var/lib/docker/
```

![docker system files and data](images/docker-data-files.png)