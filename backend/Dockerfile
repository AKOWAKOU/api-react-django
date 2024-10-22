# Utilisez une image de base Python officielle
FROM python:3.10-slim

# Définir le répertoire de travail dans le conteneur
WORKDIR /app

# Copier le fichier requirements dans le conteneur
COPY ./requirements.txt /app/requirements.txt

# Installer virtualenv pour créer un environnement virtuel
RUN python3 -m venv venv

# Activer l'environnement virtuel et installer les dépendances
RUN /bin/bash -c "source venv/bin/activate \
&& pip install -r /app/requirements.txt"

# Copier tout le code source dans le conteneur
COPY . /app

# Exposer le port 8000 pour le serveur Django
EXPOSE 8000

# Commande pour démarrer le serveur Django
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
