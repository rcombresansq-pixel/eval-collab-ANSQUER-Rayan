# Infrastructure & Déploiement - Service VPN WireGuard

## Description du projet
Ce dépôt contient la configuration et la documentation pour le déploiement sécurisé du service VPN WireGuard (`vpn-01`) ainsi que le routage du trafic via le reverse proxy Traefik.

## Architecture & Services
- **VPN WireGuard :** Hébergé sur le serveur `vpn-01`, configuré sur le port UDP `51820`.
- **Pare-feu (`fw-01`) :** Gère le filtrage des flux et l'accès distant pour les télétravailleurs.
- **Reverse Proxy :** Traefik (utilisé pour la gestion dynamique des conteneurs Docker et l'automatisation des certificats TLS).

## Prérequis
- Docker Engine & Docker Compose
- Accès réseau autorisant le port UDP `51820` sur `fw-01`
- `yamllint` pour la validation des fichiers de configuration

## Utilisation & Vérification
1. Vérifier la syntaxe du fichier Compose :
   ```bash
   docker compose config