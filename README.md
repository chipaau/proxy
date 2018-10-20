Create a new network with the name `nginx-proxy`

Add this to the bottom of all `docker-compose.yml` files

```
networks:
  default:
    external:
      name: nginx-proxy
```

On your project's `docker-compose.yml` file add the following environment variable
```
    environment:
      - VIRTUAL_HOST=dev.example.com
```