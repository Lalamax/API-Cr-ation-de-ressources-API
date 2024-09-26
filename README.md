# API Albums et Photos

Cette API permet de gérer des albums et des photos. Les utilisateurs peuvent créer, lire, mettre à jour et supprimer des albums ainsi que des photos associées.

## Fonctionnalités

- **Albums** : Créer, lire, mettre à jour et supprimer des albums.
- **Photos** : Créer, lire, mettre à jour et supprimer des photos associées aux albums.
- Stockage des données via **MongoDB**.

## Endpoints

### Albums

- **GET** `/albums`
  - Récupérer la liste de tous les albums.

- **GET** `/albums/:id`
  - Récupérer un album par son ID.

- **POST** `/albums`
  - Créer un nouvel album.
  - Exemple de corps de requête :
    ```json
    {
      "title": "Nouveau Album",
      "description": "Description de l'album"
    }
    ```

- **PUT** `/albums/:id`
  - Mettre à jour un album existant.
  - Exemple de corps de requête :
    ```json
    {
      "title": "Album mis à jour",
      "description": "Nouvelle description"
    }
    ```

- **DELETE** `/albums/:id`
  - Supprimer un album par son ID.

### Photos

- **GET** `/albums/:albumId/photos`
  - Récupérer toutes les photos d'un album spécifique.

- **GET** `/albums/:albumId/photos/:photoId`
  - Récupérer une photo spécifique par son ID.

- **POST** `/albums/:albumId/photos`
  - Ajouter une nouvelle photo à un album.
  - Exemple de corps de requête :
    ```json
    {
      "title": "Nouvelle photo",
      "url": "http://example.com/photo.jpg",
      "description": "Description de la photo"
    }
    ```

- **PUT** `/albums/:albumId/photos/:photoId`
  - Mettre à jour une photo existante.
  - Exemple de corps de requête :
    ```json
    {
      "title": "Photo mise à jour",
      "url": "http://example.com/photo_updated.jpg",
      "description": "Nouvelle description de la photo"
    }
    ```

- **DELETE** `/albums/:albumId/photos/:photoId`
  - Supprimer une photo spécifique d'un album.

## Prérequis

Avant de démarrer, vous devez avoir les éléments suivants installés :

- [Node.js](https://nodejs.org) (version 14 ou supérieure)
- [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) (compte requis)

## Installation

1. **Clonez le dépôt** :

   ```bash
   git clone https://github.com/Lalamax/API-Cr-ation-de-ressources-API.git
   cd API-Cr-ation-de-ressources-API
