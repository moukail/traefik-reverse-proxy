# Setting Up Traefik Reverse Proxy with `mkcert` and Docker Compose

This guide outlines the steps to set up Traefik as a reverse proxy using `mkcert` for SSL certificate generation and Docker Compose for container orchestration.

## Step 1: Install `mkcert`
#### For Ubuntu
```bash
sudo apt install mkcert libnss3-tools
```

#### For macOS (Homebrew)
```bash
brew install mkcert
```

#### Install the CA certificate:
```bash
mkcert -install
```

### Step 2: Clone the Repository
Clone the Traefik reverse proxy repository:

```bash
git clone https://github.com/moukail/traefik-reverse-proxy.git
cd traefik-reverse-proxy
```
### Step 3: Generate SSL Certificates
Generate SSL certificates for your domain (e.g., app.localhost):
```bash
mkcert -cert-file certs/cert.pem -key-file certs/key.pem "app.localhost" "*.app.localhost"
```

### Step 4: Run Docker Compose
Start the Traefik reverse proxy and associated containers:

```bash
docker compose up -d --build
```

### Step 5: Access the Traefik Dashboard
Access the Traefik dashboard to manage your reverse proxy configuration:

https://traefik.app.localhost/dashboard/#/

These instructions help you set up a secure reverse proxy with Traefik, ensuring secure communication between your applications and the internet.

https://doc.traefik.io/traefik/getting-started/concepts/