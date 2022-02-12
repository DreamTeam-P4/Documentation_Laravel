# Commment creer votre premier projet Laravel
```composer
composer create-project  laravel/laravel Crud-Epsilon-App
```
Apres avoir creer le projet creer une base de donnée sur phpmyadmin
<img src="https://cours.ebsi.umontreal.ca/sci6306/res/phpmyadmin_bd.jpg" width=100% />
# Modifier le fichier .env
Modifier le fichier .env pour le nom de la base de données
```.env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=epsilon
DB_USERNAME=root
DB_PASSWORD=
```
# Après cette exécution, vérifiez l'application, l'écran d'accueil du framework Laravel ressemble à ceci.
commande permettant de lancer un serveur laravel
```
php artisan serve

```
<img src="https://d33wubrfki0l68.cloudfront.net/805dc6ba89821cc9110628bf0aec04c0a622515e/2849e/assets/laravel_auth_breeze.7b6c3f3a.png" width=100% />

# Créer une migration
```
php artisan make:migration tableSimplonP4

```

