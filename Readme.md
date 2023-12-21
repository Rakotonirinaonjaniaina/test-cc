## Complexités du Code :

### Gestion des états multiples :
- Suivi de plusieurs états du cuiseur à riz (ricePresent, riceCooked, steamingInProgress, heatingInProgress), ce qui augmente la complexité de la logique des fonctions.

### Utilisation de boucles de délai synchrones :
- La fonction `delaySync()` utilise une boucle de délai synchrone, ce qui peut bloquer l'exécution du code et rendre l'application non réactive pendant le délai.

### Structure de gestion des choix utilisateur :
- La gestion des choix utilisateur avec des instructions conditionnelles (`if-else` ou `switch`) pourrait contenir des redondances ou des sections répétitives dans la logique de traitement des options.

### Dépendances complexes entre les états :
- Les différentes fonctions du cuiseur à riz (`addRice()`, `cookRice()`, etc.) ont des dépendances complexes entre les états, ce qui peut compliquer la compréhension et la maintenance du code.

### Validation d'entrée utilisateur limitée :
- La vérification de l'entrée utilisateur se limite à la conversion en nombre entier (`parseInt`) sans gérer d'autres cas d'erreur ou d'entrées inattendues.

### Boucle infinie dans la simulation :
- La simulation (`simulateRiceCooker()`) utilise une boucle `while` infinie, ce qui peut potentiellement causer des problèmes d'exécution prolongée.

---

## Simplifications Apportées :

### Utilisation de retours pour arrêter l'exécution :
- Les fonctions (`steam()`, `keepWarm()`) utilisent des retours pour interrompre l'exécution dès qu'une condition est remplie, évitant ainsi des traitements inutiles.

### Restructuration de la logique de choix avec switch :
- La gestion des choix utilisateur est améliorée en utilisant une structure `switch` au lieu d'une série de `if-else`, ce qui rend le code plus lisible et plus facile à comprendre.

### Optimisation de la réinitialisation des états :
- `removeRice()` utilise `Object.assign` pour réinitialiser les états du cuiseur à riz en une seule ligne, simplifiant ainsi le processus de réinitialisation.

### Meilleure gestion des entrées utilisateur :
- L'utilisation de `parseInt` et d'une structure `switch` pour les choix de l'utilisateur est une amélioration par rapport à la simple conversion en nombre entier, permettant une meilleure gestion des entrées non valides.
