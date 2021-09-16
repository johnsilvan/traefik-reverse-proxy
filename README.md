# traefik-reverse-proxy

## Development

1. Clone repo
    ```
   git clone https://github.com/johnsilvan/traefik-reverse-proxy.git
    ```
1. Change to it
    ```
    cd traefik-reverse-proxy 
    ```
1. Add Environment Variables 
    ```
    vim .env 
    ```
    ```
    DOMAIN=localhost
    EMAIL=admin@localhost
    CERT_RESOLVER=
    TRAEFIK_USER=admin
    TRAEFIK_PASSWORD_HASH=$2y$10$zi5n43jq9S63gBqSJwHTH.nCai2vB0SW/ABPGg2jSGmJBVRo0A.ni
    ```
    default password is admin for development - must be changed for production
## Deploying on a public server with a real domain 
    Let's say you have a domain example.com and it's DNS records point to your production server. Just repeat the local deployment steps, but don't forget to update DOMAIN, EMAIL and CERT_RESOLVER environment variables. In case of example.com, your .env file should have the following lines:

   ```
   DOMAIN=example.com
   EMAIL=your@email.com
   CERT_RESOLVER=traefik
   ```
   Setting correct email is important because it allows Let’s Encrypt to contact you in case there are any present and future issues with your certificates.
