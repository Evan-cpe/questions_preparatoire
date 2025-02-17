# À Quoi Sert `requirements.txt` ?

Le fichier `requirements.txt` est utilisé dans les projets Python pour spécifier les dépendances nécessaires au fonctionnement du projet.

### Points Clés :
- **Gestion des Dépendances** : Il liste toutes les bibliothèques et paquets Python dont le projet a besoin pour fonctionner correctement. Cela inclut les versions spécifiques des paquets.
- **Reproductibilité** : En partageant le fichier `requirements.txt`, les développeurs peuvent s'assurer que tous les environnements de développement et de production utilisent les mêmes versions des bibliothèques, ce qui aide à éviter les problèmes de compatibilité.
- **Installation Facile** : Avec une simple commande (`pip install -r requirements.txt`), tous les paquets nécessaires peuvent être installés automatiquement dans l'environnement Python.
- **Documentation** : Il sert également de documentation pour les dépendances du projet, permettant aux nouveaux développeurs de comprendre rapidement quelles bibliothèques sont utilisées.

# À Quoi Ressemble un Module en Python ?

En Python, un module est un fichier contenant du code Python, généralement avec une extension `.py`. Les modules permettent d'organiser le code en unités logiques et réutilisables.

### Points Clés :
- **Variables** : Les variables définies dans un module peuvent être accédées et modifiées.
- **Fonctions** : Les fonctions peuvent être appelées pour exécuter du code.
- **Classes** : Les classes peuvent être instanciées pour créer des objets.
- **Importation** : Utilisez `import nom_du_module` pour importer tout le module, ou `from nom_du_module import nom_de_fonction` pour importer des éléments spécifiques.

Les modules sont essentiels pour structurer les projets Python, permettant de séparer le code en fichiers distincts et de réutiliser le code facilement.

# À Quoi Ressemble un Package ?

En Python, un package est une manière d'organiser les modules en utilisant des dossiers. Un package est essentiellement un dossier contenant plusieurs modules (fichiers `.py`) et un fichier spécial appelé `__init__.py`, qui indique à Python que le dossier doit être traité comme un package.

### Structure d'un Package :

Voici à quoi ressemble la structure d'un package Python typique :

```
mon_package/
    __init__.py
    module1.py
    module2.py
    sous_package/
        __init__.py
        module3.py
```

### Points Clés :
- **Organisation** : Les packages permettent d'organiser les modules de manière hiérarchique, ce qui est particulièrement utile pour les grands projets.
- **Réutilisabilité** : Les packages facilitent la réutilisation du code en regroupant des modules liés.
- **Initialisation** : Le fichier `__init__.py` peut être utilisé pour initialiser le package ou pour définir ce qui est accessible lorsque le package est importé.

Les packages sont donc une manière puissante de structurer et de gérer le code Python, rendant les projets plus modulaires et maintenables.

# Créer un Code Python Utilisant un Module (`addition.py`)

```python
# addition.py

def additionner(a, b):
    return a + b
```

# À Quoi Sert `pip` ?

`pip` est l'outil de gestion de paquets pour Python. Il permet d'installer, de mettre à jour, de désinstaller et de gérer les bibliothèques et dépendances Python.

### Principales Utilisations :
- **Installation des Paquets**
  - Installation de paquets avec des versions spécifiques.
  - Installation de paquets depuis un fichier `requirements.txt`.
- **Mise à Jour de Paquets**
- **Désinstallation de Paquets**
- **Lister les Paquets Installés**
- **Afficher les Informations sur un Paquet**
- **Utilisation avec des Environnements Virtuels**

### Points Clés :
- **Gestion des Dépendances** : `pip` simplifie la gestion des dépendances en permettant d'installer, de mettre à jour et de désinstaller des paquets facilement.
- **Reproductibilité** : En utilisant des fichiers `requirements.txt`, `pip` aide à garantir que tous les environnements de développement et de production utilisent les mêmes versions des bibliothèques.
- **Isolation** : Utilisé avec des environnements virtuels, `pip` permet de gérer les dépendances de manière isolée pour chaque projet, évitant ainsi les conflits entre les bibliothèques.

# À Quoi Sert `PYTHONPATH` ?

`PYTHONPATH` est une variable d'environnement utilisée par Python pour spécifier des répertoires supplémentaires où rechercher des modules et des packages à importer. Elle permet de définir des chemins de recherche personnalisés pour les modules Python.

### Pourquoi Utiliser `PYTHONPATH` ?
1. **Flexibilité** : Permet de spécifier des répertoires supplémentaires pour la recherche de modules, utile pour les projets avec des structures de répertoires complexes.
2. **Portabilité** : Rend les scripts plus portables en spécifiant explicitement où se trouvent les dépendances.
3. **Débogage** : Utile pour le développement et le débogage, où les modules peuvent être dans des répertoires non standards.
4. **Séparation des Concerns** : Sépare la configuration de l'environnement de l'exécution du code, rendant le code plus propre et plus facile à comprendre.

# Où Sont Stockés les Paquets Installés par `pip` ?

Les paquets sont généralement installés dans le répertoire `site-packages`, mais le chemin peut varier.

- **Sous Unix/Linux/macOS** : `/usr/local/lib/pythonX.Y/site-packages` ou `/usr/lib/pythonX.Y/site-packages`
- **Sous Windows** : `C:\PythonXY\Lib\site-packages`

Pour trouver le chemin d'un paquet, utilisez `pip show nom_du_paquet` dans le terminal ou les modules `site` et `sysconfig` en Python.

# À Quoi Sert `pip install --user` ?

La commande `pip install --user` est utilisée pour installer des paquets Python dans le répertoire utilisateur plutôt que dans le répertoire système. Cela permet d'installer des paquets sans avoir besoin de privilèges administratifs et évite de modifier l'installation Python système.

### Pourquoi Utiliser `pip install --user` ?
1. **Pas Besoin de Privilèges Administratifs** : Vous pouvez installer des paquets sans avoir besoin des droits d'administrateur.
2. **Isolation** : Les paquets installés avec `--user` sont isolés de l'installation Python système, réduisant ainsi le risque de conflits avec d'autres paquets ou applications.
3. **Portabilité** : Les paquets installés dans le répertoire utilisateur sont spécifiques à l'utilisateur, ce qui peut être utile pour les environnements multi-utilisateurs.
4. **Sécurité** : En évitant de modifier l'installation Python système, vous réduisez le risque de corrompre les dépendances système.

# À Quoi Sert `venv` ?

`venv` est un module intégré à Python qui permet de créer des environnements virtuels. Un environnement virtuel est un environnement Python isolé qui possède sa propre copie de l'interpréteur Python et de ses dépendances.

### Pourquoi Utiliser `venv` ?
1. **Isolation des Dépendances** : Chaque environnement virtuel a ses propres dépendances, ce qui évite les conflits entre les bibliothèques utilisées par différents projets.
2. **Portabilité** : Les environnements virtuels peuvent être facilement partagés et déployés, garantissant que les dépendances sont les mêmes sur toutes les machines.
3. **Gestion des Versions** : Vous pouvez utiliser différentes versions de Python et de bibliothèques pour différents projets sans interférer avec l'installation Python système.
4. **Sécurité** : En isolant les dépendances, vous réduisez le risque de corrompre l'installation Python système.

### Comment Utiliser `venv` ?

**Exemple d'utilisation :**

```
/mon_projet
    /mon_env
    /scripts
        mon_script.py
    requirements.txt
```

```sh
cd /mon_projet
python -m venv mon_env  # Créer un environnement virtuel
source mon_env/bin/activate  # Sur Windows : mon_env\Scripts\activate  # Activer l'environnement virtuel
pip install -r requirements.txt  # Installer des paquets
python scripts/mon_script.py  # Utiliser l'environnement virtuel
deactivate  # Désactiver l'environnement virtuel
```

# À Quoi Sert `Docker` ?

`Docker` est une plateforme open-source qui permet de créer, déployer et exécuter des applications dans des conteneurs. Les conteneurs sont des environnements légers, portables et isolés qui contiennent tout ce dont une application a besoin pour fonctionner, y compris le code, les bibliothèques, les dépendances et les paramètres de configuration.

### À Quoi Sert `Docker` ?
1. **Isolation des Applications** : Chaque conteneur Docker fonctionne comme un environnement isolé, ce qui signifie que les applications peuvent s'exécuter sans interférer les unes avec les autres.
2. **Portabilité** : Les conteneurs Docker peuvent être exécutés sur n'importe quelle machine ou environnement qui supporte Docker, ce qui facilite le déploiement d'applications sur différents serveurs ou clouds.
3. **Consistance** : Les conteneurs garantissent que l'application fonctionne de la même manière dans tous les environnements (développement, test, production), réduisant ainsi les problèmes de type "ça marche sur ma machine".
4. **Efficacité** : Les conteneurs sont plus légers que les machines virtuelles (VM) car ils partagent le noyau du système d'exploitation hôte, ce qui permet une utilisation plus efficace des ressources.
5. **Scalabilité** : Docker facilite la mise à l'échelle des applications en permettant de créer et de gérer plusieurs instances de conteneurs rapidement et facilement.
6. **Gestion des Dépendances** : Les conteneurs incluent toutes les dépendances nécessaires, ce qui simplifie la gestion des versions et des configurations.

### Comment Utiliser `Docker` ?

`Docker` utilise plusieurs composants clés pour fonctionner :
1. **Docker Engine** : Le moteur Docker est le cœur de la plateforme. Il permet de créer et de gérer les conteneurs.
2. **Docker Images** : Les images Docker sont des modèles immuables qui contiennent tout ce dont une application a besoin pour s'exécuter. Elles sont utilisées pour créer des conteneurs.
3. **Docker Containers** : Les conteneurs sont des instances exécutables des images Docker. Ils contiennent tout ce dont l'application a besoin pour fonctionner.
4. **Docker Hub** : Un registre public où les utilisateurs peuvent stocker et partager des images Docker. Il existe également des registres privés pour les entreprises.
5. **Docker Compose** : Un outil pour définir et exécuter des applications multi-conteneurs. Il permet de définir les services, les réseaux et les volumes dans un fichier YAML.
6. **Docker Swarm** : Un outil pour orchestrer des clusters de conteneurs Docker, permettant de gérer des déploiements à grande échelle.

### Exemple d'Utilisation de `Docker`

**Créer une Image Docker :**

1. **Créer un Dockerfile** :

```Dockerfile
# Utiliser une image de base
FROM python:3.8-slim

# Définir le répertoire de travail
WORKDIR /app

# Copier les fichiers de l'application
COPY . /app

# Installer les dépendances
RUN pip install --no-cache-dir -r requirements.txt

# Définir la commande à exécuter
CMD ["python", "app.py"]
```

2. **Construire l'Image** :

```sh
docker build -t mon_app .
```

**Exécuter un Conteneur :**

```sh
docker run -d -p 8000:8000 mon_app
```

**Utiliser Docker Compose :**

1. **Créer un Fichier `docker-compose.yml`** :

```yaml
version: '3'
services:
  web:
    image: mon_application
    ports:
      - "8000:8000"
  redis:
    image: "redis:alpine"
```

2. **Démarrer les Services** :

```sh
docker-compose up
```