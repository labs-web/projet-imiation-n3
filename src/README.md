# Dossier du Code Source (`src/`)

Ce dossier héberge l'intégralité du code source de l'application web **Blog des lauréats** développée avec le framework Laravel 12.

---

## 1. Rôle du dossier
- Centraliser l'application Laravel 12 du projet d'imitation.
- Héberger l'architecture en 2 couches :
  - **Contrôleurs minces** : situés dans `app/Http/Controllers/`.
  - **Classes Services** : situées dans `app/Services/`.
- Regrouper les gabarits Blade responsives dans `resources/views/`.
- Gérer les routes applicatives dans `routes/web.php`.

---

## 2. Démarrage rapide du projet Laravel
Pour exécuter l'application en local depuis ce dossier :
- **Installation des dépendances backend** :
  ```bash
  composer install
  ```
- **Configuration de l'environnement** :
  ```bash
  cp .env.example .env
  php artisan key:generate
  ```
- **Lancement des migrations** :
  ```bash
  php artisan migrate
  ```
- **Démarrage du serveur de développement** :
  ```bash
  php artisan serve
  ```

---

## 3. Règles obligatoires
- Rédiger le code selon les standards PSR et les conventions Laravel 12.
- Adopter l'architecture 2 couches : aucun traitement métier direct dans les contrôleurs.
- Vérifier la gestion explicite de l'erreur HTTP 404 pour les ressources non trouvées.
