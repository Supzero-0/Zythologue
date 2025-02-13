# Zythologue

## Lancer les submodules en local

Pour lancer les submodules backend et frontend en local, suivez ces étapes :

1. Assurez-vous d'avoir Docker et Docker Compose installés sur votre machine.
2. Créez un fichier `start.sh` à la racine de votre projet avec le contenu suivant :

   ```sh
   #!/bin/bash

   # Activer le mode strict pour afficher les erreurs
   set -e

   # Démarrer le backend
   echo "🚀 Démarrage du backend..."
   (cd Zythologue-BeerCraftAPI && docker-compose up -d)

   # Démarrer le frontend
   echo "🚀 Démarrage du frontend..."
   (cd Zytho-Front-ML && npm install && npm run dev)

   # Retourner à la racine du projet
   cd ..
   ```

3. Rendez le script exécutable :

   ```sh
   chmod +x start.sh
   ```

4. Exécutez le script pour démarrer les deux projets :

   ```sh
   ./start.sh
   ```
