# La boutique francaise

Site e-commerce de vêtements. Construit sous Symfony 5 ce site m'a permis de mieux comprendre symfony, d'intégrer des fonctionnalités que je ne maitrisais pas comme Stripe pour le paiement et Mailjet pour l'envoie de mail d'informations. Design réalisé avec le template de Bootstrap.

## Pour commencer

Entrez ici les instructions pour bien débuter avec votre projet...

### Pré-requis

1. Vous devez avoir MAMP, XAMP ou LAMP pour pouvoir lancer le serveur MySQL ainsi que le serveur PHP pour faire fonctionner le site
2. Avoir maximum la version PHP 7.4.2 au maximum
3. Avoir composer.
4. Dernièrement avoir Symfony-cli afin de lancer les commandes de symfony

### Installation

1. `composer install`
2. Modifier le fichier `.env` en particulier les variables d'environnement concernant la base de données.
3. `DATABASE_URL="mysql://root:@127.0.0.1:3306/laboutiquefrancaise"`
4. Ne créer pas la base de donnée symfony le fera pour vous : `symfony console doctrine:database:create`. 
5. Pour remplir la base de donnée il suffit de : `symfony console make:migration` qui permet de préparer la structure de la base de données et enfin `symfony console doctrine:migrations:migrate` pour envoyer sur la base de données les migrations.

## Démarrage

 - Lancer ``symfony serve`` dans votre terminal et rendez vous sur l'adresse affichée, qui pourrait être : `https://127.0.0.1:8000`

### Administration

Pour accéder à l'administration du site il vous suffit modifier base de données sur phpMyAdmin pour ce faire modifier la table `user` puis de changer la valeur du champ `roles` par `"ROLE_ADMIN"` entre les crochets. 
Il suffit pour finir de raffraichir la page et de vous reconnecter au site avec les mêmes identifiants.
