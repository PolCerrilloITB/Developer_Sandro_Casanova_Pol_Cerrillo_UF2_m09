# Developer_Sandro_Casanova_Pol_Cerrillo
This repository contains a Dockerfile to build a fully configured development environment with:
✔️ Ubuntu 24.04
✔️ XFCE4 Desktop
✔️ Visual Studio Code
✔️ Python & Flask libraries
✔️ PostgreSQL client
✔️ SSH Server
✔️ VNC Server

## 📥 1️⃣ Clone the Repository
First, download the project from GitHub:
```bash
git clone https://github.com/your_user/developer-docker-image.git
cd developer-docker-image
```
## 🏗️ 2️⃣ Build the Docker Image
Run the following command to create the Docker image:
```bash
docker build -t developer-env .
```
## 🚀 3️⃣ Run the Container
Now, start the container with the appropriate exposed ports:
```bash
docker run -dit -p 5900:5900 -p 2224:22 --name dev-container developer-env
```
### 📌 Explanation of the parameters:

-dit → Runs the container in the background.
-p 5900:5900 → Exposes the VNC server for remote desktop access.
-p 2223:22 → Exposes the SSH server for remote access.
--name dev-container → Assigns a name to the container.
## 🖥️ 4️⃣ Access the Remote Desktop (VNC)
To use the graphical environment, connect via VNC Viewer using:
🔗 localhost:5900

📌 VNC Password: itb2023

## 🔑 5️⃣ Connect to the Container via SSH
The container also includes an SSH server. You can connect using:
```bash
ssh developer@localhost -p 2224
```
📌 Default password: developerpassword
## 📌 Notes
✅ Ensure you have Docker installed before running these commands.
✅ To stop the container, use:
```bash
docker stop dev-container
```
✅ To remove it completely:
```bash
docker rm dev-container
```
## DockerHub Public
[![Docker Hub](https://img.shields.io/badge/Docker%20Hub-0db7ed?style=for-the-badge&logo=docker&logoColor=white)](https://hub.docker.com/repository/docker/polcerrillo/developer_sandro_casanova_pol_cerrillo_uf2_m09)

🔄 Your development environment is now running in Docker! 🚀
