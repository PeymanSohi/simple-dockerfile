# 🚀 Hello, [Your Name]! — Docker Project

This project builds a simple Docker image that prints **"Hello, [Your Name]!"** to the console using **Docker ARG** and **ENV variables**.  
It is designed to help you practice working with **Dockerfile arguments**, **environment variables**, and lightweight images like Alpine Linux.

---

## 📋 Project Requirements

- Docker installed and running
- Internet connection (to pull `alpine:latest` base image)

---

## 📂 Project Structure

```bash
hello-name/
├── Dockerfile
└── README.md
```

---

## 🐳 How to Build and Run

### 1. Clone the Project

```bash
git clone https://github.com/your-username/hello-name.git
cd hello-name
```

---

### 2. Build the Docker Image

You can **build the image** and **pass your name** using the `--build-arg` option.

**Example:**

```bash
docker build -t hello-name --build-arg NAME=Peyman .
```

If you don't pass `NAME`, it will default to `Captain`.

---

### 3. Run the Docker Container

After building, you can simply run:

```bash
docker run hello-name
```

Expected Output:

```
Hello, Peyman!
```

(or **Hello, Captain!** if you didn't specify a name during build.)

---

## 🛠 How It Works

- The **Dockerfile** uses **Alpine Linux** as a lightweight base.
- **ARG NAME=Captain** defines a default build argument.
- **ENV NAME=${NAME}** sets the environment variable inside the container.
- **CMD** echoes "Hello, ${NAME}!" when the container runs.

---

## 📝 Example Commands

| Action | Command |
|:------:|:--------|
| Build with custom name | `docker build -t hello-name --build-arg NAME=John .` |
| Build with default name (Captain) | `docker build -t hello-name .` |
| Run the container | `docker run hello-name` |

---

## 🧠 Extra Challenge (Optional)

- Modify the Dockerfile to accept the name at **runtime** (using ENTRYPOINT and CMD instead of only build time).
- Push this Docker image to [DockerHub](https://hub.docker.com/) for global access!

---

## 📜 License

This project is for educational and personal use. No license restrictions.

---

# 🌟 Happy Dockering! 🌟

---

https://roadmap.sh/projects/basic-dockerfile
