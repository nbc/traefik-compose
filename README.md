Cet environnement démarre un traefik complet avec création des
certificats SSL

Pour le configurer, copiez le fichier .env.example vers .env et
modifiez-le en fonction de vos besoins :
* DOMAIN_NAME : définit le nom de domaine utilisé
* COMPOSE_PROJECT_NAME : définit le nom du projet, vous n'avez pas
  besoin de changer ce paramètre.

Créez un fichier htpasswd avec le compte pour se connecter à la
console traefik :
```
htpasswd -nb admin password > htpassword
```

Démarrez le projet

```
docker-compose up -d
```

Arrêter le projet :
```
docker-compose down
```


La console traefik est accessible sur le port 9443 (pour pouvoir
bloquer l'accès avec un pare-feu) à l'url
https://traefik.$DOMAIN_NAME:9443
