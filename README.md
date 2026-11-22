# Blog des Lauréats

> Plateforme web de partage d'expériences, de publication d'articles professionnels et de valorisation des parcours des lauréats.

---

## 1. Présentation du Projet

Le **Blog des Lauréats** est une application web conçue pour créer un espace d'échange et de capitalisation d'expérience :
- **Pour les lauréats :** Une plateforme d'expression pour rédiger, administrer et publier des articles techniques et professionnels relatant leurs parcours et retours d'expérience.
- **Pour les apprenants :** Un espace de consultation fluide pour découvrir les retours du terrain, s'inspirer des bonnes pratiques et faciliter leur insertion professionnelle.
- **Pour l'équipe de modération :** Un tableau de bord permettant de superviser les publications, d'administrer les catégories et de garantir la qualité des contenus.

---

## 2. Architecture & Stack Technique

L'application s'appuie sur une architecture logicielle moderne, modulaire et robuste :
- **Backend :** Laravel 13 (PHP), architecture en 2 couches (Contrôleurs minces -> Classes de Service métier).
- **Base de données :** MySQL avec gestion stricte de l'intégrité relationnelle et des transactions.
- **Interface & Design System :** Tailwind CSS avec la bibliothèque de composants accessibles Preline UI.
- **Frontend Réactif :** Alpine.js pour l'interactivité dynamique légère directement intégrée dans les vues Blade.
- **Sécurité & Contrôle d'Accès :** Spatie Laravel-Permission (RBAC) pour la gestion déclarative des rôles et autorisations.
- **Automatisation & Ingénierie :** Agent Antigravity pour l'assistance méthodologique et le respect des standards.

---

## 3. Organisation du Dépôt

L'arborescence du projet sépare rigoureusement la gouvernance, la documentation et le code source :
- [.agents/](./.agents/) : Configuration permanente de l'Agent IA (règles de développement et compétences outillées).
- [docs/](./docs/) : Livrables d'ingénierie logicielle (cadrage, analyse, conception, architecture, qualité).
  - [docs/cadrage/](./docs/cadrage/) : Notes de cadrage fonctionnel et dossiers de justification technique.
- [sprints/](./sprints/) : Feuilles d'engagement de sprint, procès-verbaux de revue et rétrospectives agiles.
- [scrum/](./scrum/) : Product Backlog priorisé et raffiné.
- [src/](./src/) : Code source de l'application Laravel (modèles, migrations, contrôleurs, services, vues Blade).

---

## 4. Guide d'Installation et de Démarrage Rapide

### Prérequis Logiciels
- PHP 8.2 ou supérieur avec les extensions requises (pdo_mysql, mbstring, openssl).
- Composer 2.x.
- Node.js 18+ et gestionnaire de paquets NPM.
- Serveur de base de données MySQL 8.x.
- Client Git.

### Installation Pas-à-Pas

1. **Cloner le dépôt et se placer dans le projet :**
   ```bash
   git clone https://github.com/labs-web/projet-imiation-n3.git
   cd projet-imiation-n3
   ```

2. **Installer les dépendances PHP et Node :**
   ```bash
   composer install
   npm install
   ```

3. **Configurer l'environnement :**
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```
   Renseigner les accès MySQL dans le fichier `.env` (`DB_DATABASE`, `DB_USERNAME`, `DB_PASSWORD`).

4. **Exécuter les migrations et le peuplement des données :**
   ```bash
   php artisan migrate --seed
   ```

5. **Compiler les assets et lancer les serveurs :**
   ```bash
   npm run dev
   php artisan serve
   ```
   L'application est alors accessible à l'adresse locale `http://localhost:8000`.

---

## 5. Gouvernance Git & Cycle de Contribution

- **Convention de branches :** Tout travail actif est réalisé sur la branche de sprint (`sprint[N]`). La branche `main` est réservée aux versions stables livrées.
- **Souveraineté humaine :** Les commits et les pushs sont obligatoirement exécutés par le développeur après validation des livrables.
