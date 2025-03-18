# Planetls

## Description

Planetls est un projet web utilisant Symfony, React et Tailwind CSS. Ce projet est configuré pour fonctionner avec Docker et Composer.

## Prérequis

- Docker
- Docker Compose
- Node.js
- Composer

## Installation

1. Clonez le dépôt :

   ```sh
   git clone <url-du-repo>
   cd planetls
   ```

2. Installez les dépendances PHP avec Composer :

   ```sh
   composer install
   ```

3. Installez les dépendances JavaScript avec npm :

   ```sh
   npm install
   ```

4. Copiez le fichier `.env` et configurez les variables d'environnement :

   ```sh
   cp .env .env.local
   ```

5. Lancez les conteneurs Docker :

   ```sh
   docker-compose up -d
   ```

6. Exécutez les migrations de la base de données :

   ```sh
   docker-compose exec php bin/console doctrine:migrations:migrate
   ```

## Développement

Pour lancer le serveur de développement Symfony :

```sh
docker-compose exec php bin/console server:run
```

Pour lancer le serveur de développement Webpack :

```sh
npm run dev
```

## Tests

Pour exécuter les tests PHPUnit :

```sh
docker-compose exec php bin/phpunit
```

## Structure du projet

- `assets/` : Contient les fichiers JavaScript et CSS.
- `bin/` : Contient les exécutables.
- `config/` : Contient les fichiers de configuration.
- `migrations/` : Contient les fichiers de migration de la base de données.
- `public/` : Contient les fichiers publics (point d'entrée du serveur web).
- `src/` : Contient le code source PHP.
- `templates/` : Contient les templates Twig.
- `tests/` : Contient les tests.
- `translations/` : Contient les fichiers de traduction.
- `var/` : Contient les fichiers générés par Symfony (cache, logs, etc.).
- `vendor/` : Contient les dépendances installées par Composer.

## Contribution

Les contributions sont les bienvenues ! Veuillez ouvrir une issue ou une pull request pour discuter des changements que vous souhaitez apporter.

## Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.
