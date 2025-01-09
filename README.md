
### Étapes pour créer un exécutable avec PyInstaller

1. **Installer PyInstaller**  
   PyInstaller est une bibliothèque Python qui permet de créer des exécutables :

   ```bash
   pip install pyinstaller
   ```

2. **Créer l'exécutable**  
   Dans le terminal ou l'invite de commandes, exécutez la commande suivante :

   ```bash
   pyinstaller --onefile mon_script.py
   ```

   - `--onefile` : Crée un seul fichier exécutable au lieu d'un dossier contenant plusieurs fichiers.


3. **Résultat**  
   - PyInstaller génère un dossier `dist/` dans le répertoire courant.
   - L'exécutable se trouve dans `dist/mon_script` ou `dist/mon_script.exe` (selon système d'exploitation).

---

### Options supplémentaires pour PyInstaller

- **Ajouter une icône à l'exécutable** : Utilisez l'option `--icon` pour inclure une icône personnalisée :
  ```bash
  pyinstaller --onefile --icon=mon_icone.ico mon_script.py
  ```

- **Mode silencieux** : Ajoutez l'option `--noconsole` pour supprimer la fenêtre de console lors de l'exécution (utile pour les applications graphiques) :
  ```bash
  pyinstaller --onefile --noconsole mon_script.py
  ```
### Utilisation de `--name`


```bash
pyinstaller --onefile --name mon_executable mon_script.py
```

- **`--onefile`** : Crée un fichier exécutable unique.
- **`--name mon_executable`** : Le fichier exécutable généré s'appellera `mon_executable.exe` (Windows) ou `mon_executable` (Linux/macOS), peu importe le nom du script Python.
- **`mon_script.py`** : Le script Python source.

### Créer un exécutable portable

Les exécutables générés incluent toutes les dépendances nécessaires, ce qui les rend portables. Cependant, si vous utilisez des bibliothèques natives ou des ressources externes, assurez-vous qu'elles sont compatibles avec le système cible.

---

### Supprimer les fichiers temporaires générés par PyInstaller

PyInstaller génère plusieurs fichiers temporaires et dossiers inutiles après la création de l'exécutable. Vous pouvez les supprimer avec ces commandes :

```bash
rm -rf build/
rm -rf __pycache__/
rm mon_script.spec
```




