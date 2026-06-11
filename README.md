# Inception Roadmap

Study roadmap for the **1337 Coding School** Inception project.

Focus areas:

* Linux processes
* Docker fundamentals
* Dockerfiles
* Docker Compose
* Networking & volumes
* MariaDB
* WordPress + PHP-FPM
* NGINX + TLS
* Secrets & security
* Testing & debugging

---

# Roadmap

| Phase | Topic                | Duration |
| ----- | -------------------- | -------- |
| 00    | Linux Processes      | 2 days   |
| 01    | Docker Basics        | 2 days   |
| 02    | Dockerfile           | 3 days   |
| 03    | Compose + Networking | 2 days   |
| 04    | Services             | 5 days   |
| 05    | Security             | 1 day    |
| 06    | Documentation        | 2 days   |
| 07    | Testing              | 2 days   |

Bonus: Redis, Adminer, FTP, Static Site.

---

# Main Goal

Understand:

* how containers work
* why PID 1 matters
* how services communicate
* how volumes persist data
* how Docker networking works
* how to debug broken containers

Not just memorizing commands like a YAML summoning ritual. Humans invented 14 layers of abstraction just to run three services and argue with permissions.

---

# Mandatory Stack

```text
NGINX (443)
     │
     ▼
WordPress + PHP-FPM
     │
     ▼
MariaDB
```

---

# Useful Commands

## Build & Start

```bash
docker compose up --build
```

## Stop

```bash
docker compose down
```

## Remove Volumes

```bash
docker compose down -v
```

## Enter Container

```bash
docker exec -it <container> bash
```

## Logs

```bash
docker logs <container>
```

---

# Important Concepts

## Docker ≠ VM

Containers share the host kernel.
A container is just an isolated process.

## Named Volumes

Used for persistent data:

* MariaDB database
* WordPress files

## Docker Network

Containers communicate through service names:

```bash
curl http://wordpress
```

## Secrets

Never hardcode passwords inside:

* Dockerfiles
* Compose files
* Git history

---

# Evaluation Prep

Be able to explain:

* PID 1
* `exec "$@"`
* Docker volumes
* service DNS
* PHP-FPM
* TLS setup
* container networking

If your explanation starts with “I copied this from a tutorial,” the evaluator will achieve spiritual enlightenment at your expense.

---

# License

Free for learning and educational use.
