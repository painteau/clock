# 🕒 Clock Nginx Docker Image

## 📖 Overview

This Docker image is based on **Nginx Alpine** and serves a **fullscreen clock** as the default `index.html`. It is lightweight, efficient, and easy to deploy as a simple web-based clock.

## ⭐ Features

- **Fullscreen Clock**: Displays a real-time digital clock.
- **Minimal Resource Usage**: Based on `nginx:mainline-alpine-slim` for efficiency.
- **Easy Deployment**: Just run the container and access the clock via a web browser.

## 🛠 Cloning and Building Locally

### 🔄 Cloning the Repository

First, clone the repository to your local machine:

```bash
git clone https://github.com/painteau/clock.git
cd clock
```

### 🔨 Building the Custom Image

To create your custom Docker image, use:

```bash
docker build -t clock-nginx .
```

## 🚀 Running the Container

Once the image is built, you can start a container with:

```bash
docker run -d --name clock \
    -p 8080:80 \
    clock-nginx
```

This will start the clock web application and serve it on port `8080`.

## 📦 Running from the Official Image

If you prefer to use the prebuilt image from GitHub Container Registry, run:

```bash
docker run -d --name clock \
    -p 8080:80 \
    ghcr.io/painteau/clock:latest
```

## 🌐 Accessing the Clock

Once the container is running, open your browser and navigate to:

```
http://localhost:8080
```

You should see a fullscreen clock displayed.

## ⚠ Security Notice

If deploying in a production environment, ensure that the container is secured and properly configured to prevent unauthorized access.

## 📜 License

This project is open-source and licensed under the MIT License.

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository on GitHub: [painteau/clock](https://github.com/painteau/clock).
2. Create a new branch (`feature-branch`).
3. Commit your changes.
4. Push to your branch and create a pull request.

For major changes, please open an issue first to discuss the proposed modifications.

