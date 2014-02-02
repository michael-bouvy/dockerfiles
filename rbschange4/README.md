RBS Change v4 Dockerfile
========================

This Dockerfile makes it very easy to deploy within seconds a running and up-to-date RBS Change v4 container.

## Installation steps

### Clone this repo

```
$ git clone https://github.com/michael-bouvy/dockerfiles
$ cd dockerfiles/rbschange4
```

### Build the image

```
$ sudo docker build -t rbschange4 .
```

### Run the container

```
$ sudo docker run -p 8080:80 -d -t rbschange4
```

### Done !

Now open http://localhost:8080/admin.php in your browser and login with `admin` / `admin`.

## SSH access

If you wish to access via SSH to the running container, grab it's IP with this command :

```
$ sudo docker inspect -format='{{.NetworkSettings.IPAddress}}' $(sudo docker ps | grep rbschange4 | cut -d " " -f 1)
```

and login with login `root` and pass `toor`.

------

For more informations about RBS Change, see official GitHub repo : https://github.com/RBSChange/Change
