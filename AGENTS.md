# Directives pour les Agents IA / Contributeurs

## Contexte du projet
Infrastructure de déploiement et d'hébergement de services Docker sécurisés (VPN WireGuard, Reverse Proxy, pare-feu).

## Commandes de vérification
- Valider la syntaxe des fichiers Compose : `docker compose config`
- Tester la connectivité et les règles pare-feu : `ping <IP>` / `nc -zuv <IP> 51820`
- Vérifier les configurations YAML/JSON : `yamllint .`

## Conventions
- Commits : Respect strict des **Conventional Commits** (`feat:`, `fix:`, `docs:`, `ci:`).
- Branches : Utilisation de préfixes normés (`docs/`, `feature/`, `fix/`).

## Interdits
- Ne JAMAIS commiter de secrets, clés privées, tokens ou mots de passe en clair.
- Ne JAMAIS pousser de commits directement sur la branche `main`.