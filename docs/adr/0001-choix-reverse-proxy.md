# ADR 0001 : Choix du reverse proxy (Traefik vs Nginx)

## Statut
Accepté

## Contexte
L'équipe héberge une quinzaine de services Docker répartis sur 2 serveurs, avec l'ajout de nouveaux services chaque mois. Le renouvellement manuel des certificats TLS a déjà provoqué des coupures de service. L'équipe maîtrise Nginx mais ne connaît pas Traefik.

## Décision
Nous choisissons d'adopter **Traefik** comme reverse proxy pour l'ensemble des conteneurs.

## Conséquences
- **Positives :**
  - Gestion et renouvellement automatiques des certificats TLS via Let's Encrypt (évite les coupures).
  - Découverte automatique des nouveaux services Docker via les labels dans `docker-compose.yml` (idéal pour l'ajout mensuel de services).
- **Négatives :**
  - Montée en compétences nécessaire pour l'équipe (apprentissage de Traefik).