# Caddy Namecheap Docker Image

This Dockerfile will build Caddy with the Namecheap module located [here](https://github.com/caddy-dns/namecheap). 

This allows Caddy to use the Namecheap API to add DNS records on-the-fly to verify ownership of a domain you are trying to get an HTTPS certificate for.

## Build

[GitHub Actions](https://github.com/jakeprice-dev/docker-caddy-namecheap/actions) builds and pushes the image to [DockerHub](https://hub.docker.com/r/jakepricedev/docker-caddy-namecheap) when a change to the repository is detected.

## Caddyfile

Full Caddyfile configuration examples can be found [here](https://github.com/caddy-dns/namecheap#config-examples)

```
tls {
    dns namecheap {
    api_key {env.NAMECHEAP_API_KEY}
    user {env.NAMECHEAP_API_USER}
    }
}
```

