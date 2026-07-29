# Setup Guide

## Prerequisites

- Windows 10/11
- Oracle VirtualBox
- Kali Linux Virtual Machine
- Internet Connection
- Docker Engine

---

## Step 1: Configure VirtualBox

- Create or import a Kali Linux VM.
- Allocate:
  - 4 GB RAM
  - 2 CPUs
- Configure network:
  - Adapter 1: NAT
  - Adapter 2: Host-Only

---

## Step 2: Start Kali Linux

Verify the network:

```bash
ip a
ping -c 4 google.com
```

---

## Step 3: Install Docker

```bash
sudo apt update
sudo apt install docker.io -y
sudo systemctl enable --now docker
```

Verify installation:

```bash
docker --version
```

---

## Step 4: Deploy OWASP Juice Shop

Pull the image:

```bash
sudo docker pull bkimminich/juice-shop
```

Run the container:

```bash
sudo docker run -d -p 3000:3000 --name juice-shop bkimminich/juice-shop
```

Check the container:

```bash
sudo docker ps
```

Access the application:

```
http://localhost:3000
```

---

## Step 5: Validate the Lab

### Nmap

```bash
nmap -sV 127.0.0.1 -p 3000
```

### Burp Suite

- Launch Burp Suite Community Edition.
- Use the default proxy configuration.
- Browse the application.
- Review the HTTP History.

### Wireshark

Capture traffic on the **Loopback (lo)** interface.

Filter:

```text
tcp.port == 3000
```

---

The laboratory is now ready for web application security practice.