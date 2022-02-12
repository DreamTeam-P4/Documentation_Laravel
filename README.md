# Commment creer votre premier projet Laravel
```composer
composer create-project  laravel/laravel Crud-Epsilon-App
```
Apres avoir creer le projet creer une base de donnée sur phpmyadmin
<img src="https://github.com/DreamTeam-P4/Documentation_Laravel/blob/main/db.PNG" width=100% />
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
<img src="https://github.com/DreamTeam-P4/Documentation_Laravel/blob/main/demo.PNG" width=100% />

# Cliquez et ouvrez-le.
``` php
class CreateContactsTable extends Migration
{
    public function up()
    {
       
    }
    public function down()
    {
        Schema::dropIfExists('contacts');
    }
}
```
# Ensuite creer vos champs a l'interieur de la fonction up()
``` php
class CreateContactsTable extends Migration
{
    public function up()
    {
     Schema::create('contacts', function (Blueprint $table) {
            $table->id();
            $table->chaîne('nom');
            $table->chaîne('adresse');
            $table->string('mobile');
            $table->timestamps();
        });
       
    }
    public function down()
    {
        Schema::dropIfExists('contacts');
    }
}
```

# C' est maintenant super il ne vous reste qu' a envoyer votre table dans la base de donnée
```
php artisan migrate

```
Vérifier si la base de donnée a bien été uploadé
<img src="migrate"  width=100%/>

😍😍😍😍 C ' est top ca . J 'espere que vous etes toujour en forme🤷‍♀️

# Creer votre controlleur 
```
php artisan  make:controller EpsilonController --ressource

```

<img src="controller"  />

# Créer un modèle
Un modele a pour role de permettre l obtension des donnees de la base de donnée
```
php artisan make:model simplon
```
<img src="model"  />

```php

<?php

namespace App\Models;

use Illuminate\Database\Eloquent\Factories\HasFactory;
use Illuminate\Database\Eloquent\Model;

class Epsilon extends Model
{
    use HasFactory;
}


```

Ensuite ajouter le champs de vos tables;
```php
<?php

namespace App\Models;

use Illuminate\Database\Eloquent\Factories\HasFactory;
use Illuminate\Database\Eloquent\Model;

class Epsilon extends Model
{
    protected $table = 'simplonp4';
    protected $primaryKey = 'id';
    protected $fillable = ['name', 'address', 'mobile'];
}



```

# Créer des vues






