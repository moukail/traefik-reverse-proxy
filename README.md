### git
```bash
git clone https://github.com/moukail/traefik-reverse-proxy.git
```

#### Install in Ubuntu
```bash
sudo apt install mkcert libnss3-tools
```

#### Mac
todo 

#### generate certs
```bash
mkcert -install
mkcert -cert-file certs/cert.pem -key-file certs/key.pem "app.localhost" "*.app.localhost"
```

#### generate pkcs12
```bash
openssl pkcs12 -export -out certs/certificate.p12 -inkey certs/key.pem -in certs/cert.pem
```

### Docker
```bash
docker compose up -d --build
```

### traefik dashboard
https://traefik.app.localhost/dashboard/#/
