### mkcert
#### For Ubuntu
```bash
sudo apt install mkcert libnss3-tools
```

#### For Mac
```bash
brew install mkcert
```

#### install CA cert
```bash
mkcert -install
```

### git
```bash
git clone https://github.com/moukail/traefik-reverse-proxy.git
cd traefik-reverse-proxy
```
### generate certs
```bash
mkcert -cert-file certs/cert.pem -key-file certs/key.pem "app.localhost" "*.app.localhost"
```

### Docker
```bash
docker compose up -d --build
```

### traefik dashboard
https://traefik.app.localhost/dashboard/#/
