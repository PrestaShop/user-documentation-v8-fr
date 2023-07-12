# Informations complémentaires

## Garder une version d’essai sous la main ! <a href="#informationscomplementaires-garderuneversiondessaisouslamain" id="informationscomplementaires-garderuneversiondessaisouslamain"></a>

{% hint style="info" %}
**Une fois la configuration de votre boutique effectuée mais avant de l'ouvrir au public, nous vous recommandons vivement d’installer une version d’essai.**

Vous pouvez le faire de manière locale (sur votre ordinateur personnel) à l'aide de [WAMP](http://en.wikipedia.org/wiki/Comparison\_of\_WAMPs) pour Windows, [MAMP](http://en.wikipedia.org/wiki/MAMP) pour Mac, ou [LAMP](http://en.wikipedia.org/wiki/LAMP\_\(software\_bundle) pour Linux (ou [XAMPP](http://www.apachefriends.org/en/xampp.html) pour n’importe laquelle de ces plateformes)&#x20;

Vous pouvez également installer une version d'essai ailleurs sur votre serveur d’hébergement.
{% endhint %}

Cette deuxième instance servira d’environnement de préparation de la production où vous pourrez effectuer toutes les modifications de votre boutique en ligne PrestaShop sans affecter la version active. De cette façon, en cas d’erreur, votre boutique restera inchangée.

Après avoir confirmé que votre version d’essai fonctionne normalement, copiez la version d’essai sur la version active. Il est préférable de le faire après les heures de trafic élevé en désactivant correctement et temporairement votre boutique depuis le back-office de PrestaShop.

Pour ce faire, vous pouvez utiliser le [mode maintenance](../guide-utilisateur/configurer-boutique/configurer-parametres-boutique/general/maintenance.md).

## Vérifier la bibliothèque GD <a href="#informationscomplementaires-verifierlabibliothequegd" id="informationscomplementaires-verifierlabibliothequegd"></a>

La [bibliothèque GD](https://libgd.github.io/) permet à PrestaShop de retravailler les images que vous mettez en ligne, notamment de les redimensionner.

Sur une installation par défaut de PHP, la bibliothèque GD doit être activée. Toutefois, si ce n’est pas le cas, les instructions standard de Windows sont :

1. Dans le répertoire racine de votre dossier PHP, **ouvrez le fichier `php.ini`.**
2.  **Désactivez le commentaire de la ligne `extension=php_gd2.dll`**en supprimant le “;” au début de la ligne.&#x20;

    La ligne se devrait se situer au milieu du fichier environ, au milieu d’une longue liste d’extensions.
3. **Redémarrez les services PHP.**

{% hint style="info" %}
Si vous n’avez pas accès au fichier `php.ini` (ce qui est souvent le cas en hébergement partagé), contactez votre hébergeur pour lui faire part de vos besoins.
{% endhint %}

## Activer PHP 7.2+ <a href="#informationscomplementaires-activerphp5.6+" id="informationscomplementaires-activerphp5.6+"></a>

{% hint style="warning" %}
Pour installer PrestaShop, **PHP 7.2** doit être activé. La compatbilité est étendue jusqu'à PHP 8.1 mais ne tentez pas d'exécuter PrestaShop à l'aide de PHP 8.2, cela ne fonctionnera pas.
{% endhint %}

N’hésitez pas à publier sur [GitHub](https://github.com/PrestaShop) (vous aurez besoin d’un compte) un rapport de bogue pour obtenir des conseils afin de faire fonctionner PrestaShop sur votre service d’hébergement. Nous les ajouterons à ce guide à mesure que nous les recevrons.

Voici une liste des procédures que nous connaissons :

### 1&1 IONOS <a href="#informationscomplementaires-1-and-1ionos" id="informationscomplementaires-1-and-1ionos"></a>

Ajoutez cette ligne à votre fichier `.htaccess` :

```
AddType x-mapp-php5 .php
```

Pour la **réécriture d'URL**, ajoutez ces lignes :

```
Options +FollowSymLinks
RewriteEngine On
```

### Free.fr <a href="#informationscomplementaires-free.fr" id="informationscomplementaires-free.fr"></a>

Ajoutez cette ligne à votre fichier `.htaccess` :

```
php 1
```

### OVH <a href="#informationscomplementaires-ovh" id="informationscomplementaires-ovh"></a>

Ajoutez cette ligne à votre fichier `.htaccess` :

```
SetEnv PHP_VER 5
```

Pour **désactiver les variables globales** :

```
SetEnv REGISTER_GLOBALS 0
```

### GoDaddy <a href="#informationscomplementaires-godaddy" id="informationscomplementaires-godaddy"></a>

Pour **voir** votre version de PHP :

1. Connectez-vous à votre **Account Manager**.
2. Dans la section Products, cliquez sur **Web Hosting**.
3. À côté du compte d'hébergement que vous voulez utiliser, cliquez sur **Launch**.

Dans la section Server, vous pourrez voir la version de PHP.

Pour **modifier** votre version de PHP :

1. Dans le menu **Content**, sélectionnez **Programming Languages**.
2. Sélectionnez la **version de PHP** que vous souhaitez utiliser, puis cliquez sur **Continue**.
3. Cliquez sur Update.

{% hint style="info" %}
Les modifications peuvent mettre jusqu'à 24h à être prises en compte.
{% endhint %}

### Lunarpages (mutualisé) <a href="#informationscomplementaires-lunarpages-mutualise" id="informationscomplementaires-lunarpages-mutualise"></a>

1. Connectez-vous à **cPanel.** Il devrait se trouver à l'adresse [http://www.(votre\_domaine).(com/net/org/etc.)/cpanel](http://www.\(votre\_domaine\).\(com/net/org/etc.\)/cpanel)
2. Saisissez vos **identifiants**.
3. Dans la page qui s'affiche, cliquez sur l'icône **"Enable/Disable PHP 7.2+"**.
4. Dans la page qui s'affiche, cliquez sur **"Add PHP 7.2+ To Your Account!"**.

{% hint style="info" %}
Les modifications peuvent mettre jusqu'à 24h à être prises en compte.
{% endhint %}
