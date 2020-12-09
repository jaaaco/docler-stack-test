[![Contact me on Codementor](https://www.codementor.io/m-badges/jaaaco/book-session.svg)](https://www.codementor.io/@jaaaco?refer=badge)

# Starting and updating

```bash
docker stack deploy -c stack.yml mystack
```

# Stopping / Removing

```bash
docker stack rm mystack
```

# Executing commands


## Find your container

```bash
docker ps | grep mystack_
```

## Run bash command

```bash
docker exec -it <container id> bash
```

# Connect to other containers inside the stack

## Install ping tool (example)

inside container (Debian based image only):

```bash
apt-get update && apt-get install -y iputils-ping
```

* make sure all containers are in the same network
* ping container using its service name, for example:

```bash
ping web
ping db
```

