# Utilisez une image de base Python officielle
FROM python:3.10-slim

# Définir le répertoire de travail dans le conteneur
WORKDIR /app

# Copier le fichier requirements dans le conteneur
COPY ./requirements.txt /app/requirements.txt

# Installer les dépendances
RUN pip install --no-cache-dir -r /app/requirements.txt

# Copier tout le code source dans le conteneur
COPY . /app

# Exposer le port 8000 pour le serveur Django
EXPOSE 8000

# Commande pour démarrer le serveur Django
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
