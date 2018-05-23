### Initial ###
1. get `SERCRET_KEY` and put in `.env`
``` shell
docker run --rm sentry config generate-secret-key 
```

2. add externel volumes for using `windows`
``` shell
docker volume create sentry-docker_postgres
```

3. 
``` shell
docker-compose up -d sentry postgres redis
```

4. do migrate and upgrade sentry losing
``` shell
docker-compose exec sentry sentry upgrade
```

### Continue ###

1. start all service
``` shell
docker-compose up -d
```