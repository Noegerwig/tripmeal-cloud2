# Utiliser une image de base légère avec Python 3.7
FROM python:3.7-slim

# Définir le répertoire de travail
WORKDIR /app

# Copier uniquement les fichiers de dépendances pour tirer parti du cache Docker
COPY requirements.txt .

# Installer les dépendances nécessaires
RUN pip install --no-cache-dir -r requirements.txt

# Copier le reste des fichiers nécessaires
COPY . .

# Assurer que le fichier app.py est exécutable
RUN chmod +x /app/app.py

# Exposer le port utilisé par l'application
EXPOSE 5000

# Commande par défaut pour exécuter l'application
CMD ["python", "app.py"]
