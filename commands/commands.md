# Commands Used

## Network

```bash
ip a
```

```bash
ping -c 4 google.com
```

## Docker

```bash
sudo apt update
```

```bash
sudo apt install docker.io -y
```

```bash
docker --version
```

```bash
sudo docker pull bkimminich/juice-shop
```

```bash
sudo docker run -d -p 3000:3000 --name juice-shop bkimminich/juice-shop
```

```bash
sudo docker ps
```

## Nmap

```bash
nmap -sV 127.0.0.1 -p 3000
```

## Wireshark Filter

```text
tcp.port == 3000
```