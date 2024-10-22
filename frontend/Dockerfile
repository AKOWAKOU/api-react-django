# Utiliser une image officielle de Node.js
FROM node:18-alpine

# Définir le répertoire de travail dans le conteneur
WORKDIR /app

# Copier les fichiers package.json et package-lock.json
COPY package*.json ./

# Installer les dépendances
RUN npm install

# Copier tout le code source dans le conteneur
COPY . .

# Générer une version optimisée de l'application React
RUN npm run build

# Installer un serveur web léger pour servir l'application React
RUN npm install -g serve

# Exposer le port 3000 pour l'application React
EXPOSE 3000

# Commande pour démarrer le serveur web
CMD ["serve", "-s", "build", "-l", "3000"]
