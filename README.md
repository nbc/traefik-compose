Cet environnement démarre un traefik complet avec création des
certificats SSL

Pour le configurer, copiez le fichier .env.example vers .env et
modifiez le en fonction de vos besoins.

Créez un fichier htpasswd avec le compte nécessaire
```
htpasswd -nb admin password > htpassword
```

Démarrez le projet

```
docker-compose up
```

Vous pouvez normalement vous connecter sur
https://traefik.$DOMAIN_NAME
