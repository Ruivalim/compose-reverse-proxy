`docker network create net`

Add those variables to the other projets

```yaml
environmnet:
    - VIRTUAL_HOST=domain.com
    - VIRTUAL_PORT='80'
    - LETSENCRYPT_HOST=domain.com
```

And this network service

```yaml
service:
    networks:
        - net

networks:
    net:
        external: true
```
