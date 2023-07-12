---
description: Cette page liste tout ce dont vous avez besoin pour installer PrestaShop 8.
---

# Ce dont vous avez besoin

## Instructions de configuration rapides <a href="#cedontvousavezbesoin-instructionsdeconfigurationrapides" id="cedontvousavezbesoin-instructionsdeconfigurationrapides"></a>

Voici une synthèse de ce dont vous avez besoin pour commencer l’installation de PrestaShop 8. Vous trouverez, si nécessaire, des instructions plus détaillées dans les sections suivantes.

## Configuration requise

* **Système :** Unix, Linux ou Windows
* **MySQL :** 5.6 ou version ultérieure
* **PHP :** 7.2 ou version ultérieure.
* **Dans votre fichier `php.ini`:**
  * **Réglages utiles :**
    * `allow_url_fopen` réglé sur **“On”✅** (Activé),
    * `register_globals` réglé sur **“Off”** ❌(Désactivé),
    * `upload_max_filesize` réglé sur **“16MB”** (ou plus).
  * **Extensions PHP indispensables:**
    * **CURL:** le CURL ([Client URL extension](https://php.net/manual/en/book.curl.php)) permet de télécharger des ressources à distance, comme des modules ou des packs de langue.
    * **DOM:** l'extension [DOM ](https://php.net/manual/en/book.dom.php)est requise afin d'analyser les documents XML.
    * **Fileinfo:** l'extension [File information](https://php.net/manual/en/book.fileinfo.php) permet de comprendre le type de fichier téléchargé.&#x20;
    * **GD:** l'extension [GD](https://php.net/manual/en/book.image.php) permet de créer des miniatures pour les images téléchargées.
    * **Intl:** l'extension [ICONV ](https://www.php.net/manual/en/book.iconv.php) permet de convertir les jeux de caractères.
    * **Mbstring:** l'exension [Multibyte string ](https://www.php.net/manual/en/book.mbstring.php)permet de manipuler des chaînes n'importe où.
    * **Zip:** l'extension [Zip](https://php.net/manual/en/book.zip.php) permet de décompresser les fichiers compressés, comme les modules ou packs de langues.
    * **JSON:** l'extension [JSON ](https://www.php.net/manual/en/json.installation.php)permet de prendre en charge le format JSON.
    * **Iconv:** l'extension [ICONV](https://www.php.net/manual/en/book.iconv.php) permet de convertir des jeux de caractères.
* **Outils serveur utiles :**
  * Cron/[Crontab](https://crontab.guru/), [Memcached](https://memcached.org/).

### Pour un meilleur fonctionnement :

* **Hébergeur :** Unix/Linux.
* **Serveur web :** Apache 2.2 (ou version ultérieure), Nginx 1.0 (ou version ultérieure).
  * **Paramètres des modules Apache :**
    * `mod_rewrite` **activé** ✅,
    * `mod_security` **désactivé** ❌,
    * `mod_auth_basic` **désactivé** ✅.
* **RAM serveur :** Au moins 256 Mo de RAM dédiée à PHP. Plus la mémoire sera élevée, meilleures seront les performances.
* **Codes d’accès** à votre serveur FTP et à votre base de données MySQL. Ces codes doivent vous être fournis par votre [hébergeur](ce-dont-vous-avez-besoin.md#trouver-un-hebergeur) si vous n’effectuez pas d’installation locale.
* **Un éditeur de texte.**
* **Un client FTP.**
* **Un navigateur web récent** (si vous utilisez Internet Explorer : au moins IE9).

Il vous faudra également connaître l’adresse web (sur votre domaine) depuis laquelle vous souhaitez vendre des produits

Une fois votre configuration prête, vous pouvez utiliser le guide d’installation :&#x20;

{% content-ref url="installer-prestashop.md" %}
[installer-prestashop.md](installer-prestashop.md)
{% endcontent-ref %}

## Instructions de configuration détaillées

PrestaShop est une application web. Pour fonctionner, elle doit être installée sur un serveur web et a besoin d’un nom de domaine que vos visiteurs utiliseront pour accéder à votre boutique.

### Enregistrer un nom de domaine <a href="#cedontvousavezbesoin-enregistrerunnomdedomaine" id="cedontvousavezbesoin-enregistrerunnomdedomaine"></a>

Avant de télécharger ou d’installer quoi que ce soit, **vous devez offrir un toit à votre boutique en ligne PrestaShop.**&#x20;

Il est constitué de deux éléments : un **nom de domaine** et un **serveur web.**&#x20;

### Qu'est-ce qu'un nom de domaine ?

Le nom de domaine est l’identifiant en ligne de votre site web, par exemple : [`exemple.com`](http://example.com) ou [`maboutiqueenligne.net`](http://myonlineshop.net). Il s’agit de la **partie publique de votre serveur web et donc de votre boutique.**

Vous devez **acheter un nom de domaine pour votre boutique**. Vous pouvez obtenir un hébergement web et un nom de domaine en même temps : de nombreux hébergeurs offrent un nom de domaine gratuit à la création de chaque nouveau compte. Un nom de domaine peut être gratuit pendant un an ou pour toute la durée de votre contrat d’hébergement, ce qui permet de bénéficier facilement et directement d’une offre complète (hébergement + nom de domaine).

Les noms de domaine fournis par certains hébergeurs peuvent poser problème : si vous n’êtes pas satisfait du service, vous voudrez peut-être migrer votre boutique chez un meilleur hébergeur, **ce qui nécessite de déplacer vos fichiers, vos données et votre nom de domaine vers ce dernier.**

Les fichiers et les données sont faciles à déplacer, mais en fonction de l’hébergeur, vous pourriez avoir du mal à récupérer votre nom de domaine.&#x20;

Dans la mesure où l’hébergeur a acheté le nom de domaine pour vous, techniquement, **le domaine lui appartient**. L’hébergeur **peut donc vous interdire de le transférer vers un autre hébergeur ou vous autoriser à le faire moyennant des frais.** Comme le nom de domaine est votre marque et votre adresse sur Internet, **vous devez vous plier aux règles de l’hébergeur.**

C’est la raison pour laquelle il est souvent recommandé de générer votre nom de domaine auprès d’un bureau d’enregistrement indépendant&#x20;

(voir : [https://fr.wikipedia.org/wiki/Bureau\_d%27enregistrement](http://en.wikipedia.org/wiki/Domain\_name\_registrar)).&#x20;

{% hint style="warning" %}
Techniquement, **vous ne pouvez jamais acheter un nom de domaine** ; vous pouvez seulement le louer, la plupart du temps moyennant des frais annuels.&#x20;

Cela vous donne le droit d’utiliser ce nom de domaine, mais dès que vous cessez de payer, **le nom de domaine ne vous appartient plus et peut être récupéré par n’importe qui.**
{% endhint %}

En plus de payer l’enregistrement du nom de domaine, vous devrez payer l’hébergement sur Internet. Toutefois, vous restez libre de passer chez un meilleur hébergeur à tout moment sans surcoût : vous n’aurez qu’à modifier les adresses DNS du nom de domaine. La modification sera appliquée dans le monde entier dans un délai de 24 heures.

{% hint style="info" %}
Si vous préférez obtenir votre nom de domaine auprès d’un bureau d’enregistrement indépendant, en voici quelques-uns auxquels vous pouvez faire confiance :

* **Gandi :** [http://en.gandi.net/](http://en.gandi.net)
* **Namecheap :** [http://www.namecheap.com/](http://www.namecheap.com)
* **GoDaddy :** [https://www.godaddy.com/](https://www.godaddy.com)
* **1&1 IONOS :** [https://www.ionos.fr/](https://www.ionos.fr)

Il en existe beaucoup d’autres. Renseignez-vous !
{% endhint %}

### Trouver un hébergeur

Maintenant que vous avez un nom de domaine, **il faut qu’il soit relié à PrestaShop**. Cela signifie que les fichiers de PrestaShop doivent être hébergés sur un serveur web. Vous pouvez avoir votre propre serveur web, mais il est plus probable que votre boutique soit hébergée par un [service d’hébergement Internet](https://en.wikipedia.org/wiki/Internet\_hosting\_service) qui vous fournit un domicile en ligne moyennant un abonnement mensuel ou annuel.

Avant de lancer une boutique en ligne, vous devrez d’abord **choisir un fournisseur d’hébergement.** Presque tous les hébergeurs peuvent prendre en charge la solution PrestaShop de manière efficace. Toutefois, **seuls quelques fournisseurs d’hébergement proposent des serveurs optimisés pour PrestaShop** (avec une fonction d’installation en 1 clic et une version à jour).&#x20;

Vous pouvez trouver la liste de partenaires d’hébergement[ ici.](https://prestashop.fr/prestashop-partners/)

{% hint style="info" %}
Lorsque vous choisissez votre hébergeur, rappelez-vous une condition essentielle, **l’hébergeur doit prendre en charge :**

* &#x20;**PHP 7.1** (ou une version plus récente), le langage de programmation dans lequel PrestaShop est écrit,
* **MySQL 5.6** (ou une version plus récente), le système de bases de données où PrestaShop stocke toutes ses données.&#x20;

Cette liste d'exigeance est non-exhaustive. Reportez-vous à la section **“Exigences techniques”** ci-après.
{% endhint %}



### Pré-requis techniques

PrestaShop est une application qui fonctionne sur un serveur web. Elle est rédigée dans le langage de programmation PHP. **Elle stocke ses données sur un serveur MySQL.**

[PHP](https://www.php.net/) est un **langage de programmation** open source, principalement utilisé pour les applications web. Créé en 1995, il est depuis devenu le langage de programmation le plus utilisé par les développeurs web. Il utilise une syntaxe de type C qui permet aux développeurs de l’apprendre facilement.

[MySQL ](https://www.mysql.com/)est un **système de gestion de bases de données** open source. Également créé en 1995, il est désormais le système de bases de données le plus utilisé par les développeurs web. Il est basé sur le langage SQL, le langage de base de données le plus répandu.

\
Quel que soit le service d’hébergement que vous choisissez, les composants suivants doivent être installés sur votre serveur web :

* **Système** : Unix, Linux ou Windows. (Unix est fortement recommandé).
* **Serveur web** : Serveur web Apache 2.2 ou version ultérieure.
* **PHP :** 7.1 ou version ultérieure.
* **MySQL :** 5.6 ou version ultérieure.
* **RAM serveur :** Au moins 256 Mo de RAM sur votre serveur.

{% hint style="info" %}
PrestaShop peut également fonctionner avec un [serveur web IIS 6.0 Microsoft](https://www.iis.net/) ou une version ultérieure, et un [serveur Nginx 1.0](https://docs.nginx.com/nginx/admin-guide/web-server/) ou une version ultérieure.
{% endhint %}

### Outils <a href="#cedontvousavezbesoin-outils" id="cedontvousavezbesoin-outils"></a>

Vous aurez besoin de deux outils :&#x20;

* **un éditeur de texte,** pour éditer les fichiers texte,&#x20;
* **un client FTP,** pour transférer les fichiers de votre machine vers votre serveur et vice versa.

#### Éditeur de texte <a href="#cedontvousavezbesoin-editeurdetexte" id="cedontvousavezbesoin-editeurdetexte"></a>

Voici quelques éditeurs de texte bien connus, vous pouvez utiliser celui qui vous convient le mieux :

* **Windows**
  * Sublime Text : [http://www.sublimetext.com/](http://www.sublimetext.com)
  * Notepad++: [https://notepad-plus-plus.org/](https://notepad-plus-plus.org/downloads/)
* **MacOS :**
  * Sublime Text: [http://www.sublimetext.com/](http://www.sublimetext.com/)
  * BBEdit: [https://www.barebones.com/products/bbedit/](https://www.barebones.com/products/bbedit/)
* **Unix/Linux :**
  * Vim : [http://www.vim.org/](http://www.vim.org)
  * Emacs : [http://www.gnu.org/software/emacs/](http://www.gnu.org/software/emacs/)

{% hint style="warning" %}
N'utilisez **jamais** un logiciel de traitement de texte lorsque vous voulez modifier les fichiers de PrestaShop, comme Microsoft Word ou [OpenOffice](http://www.openoffice.org/) Writer.
{% endhint %}

### Client FTP

**FTP** est l’abréviation de “File Transfer Protocol”, un protocole standard utilisé pour transférer des fichiers depuis un ordinateur vers un hébergeur.

#### Utiliser Filezilla

Dans ce guide, nous utiliserons **FileZilla**, un client FTP gratuit et efficace pour Windows, MacOS et Linux.

{% hint style="info" %}
**Téléchargez FileZilla** sur [http://filezilla-project.org/](http://filezilla-project.org) et **lancez l’installeur**.&#x20;

**Remarque** : Télécharez **FileZilla Client** et non pas FileZilla Server.
{% endhint %}

Une fois FileZilla installé, vous devrez **le configurer** avec les paramètres de connexion de votre serveur web, normalement fournis par votre hébergeur. Si vous n’avez pas reçu ces paramètres, demandez-les à votre hébergeur ou consultez votre dossier spam pour vérifier qu’ils ne s’y trouvent pas.

Les principaux paramètres nécessaires sont les suivants :

* **Un nom d’hôte** ou **une adresse IP** : emplacement du serveur FTP de votre espace d’hébergement.
* **Un nom d’utilisateur** : votre identifiant de compte d’hébergement unique.
* **Un mot de passe** : mesure de sécurité obligatoire.

**Ouvrez** FileZilla et le **Gestionnaire de site**. Vous pouvez le faire de trois manières différentes :

* Appuyez sur **Ctrl+S**.
* Cliquez sur l’icône **“Ouvrir le Gestionnaire de site”** située dans l’angle supérieur gauche.
* Ouvrez le menu **“Fichier”** et sélectionnez **l’option “Gestionnaire de site”.**

Une fenêtre s’ouvre.

<figure><img src="../.gitbook/assets/image (61).png" alt=""><figcaption><p>La page "Site Manager" de FileZilla.</p></figcaption></figure>

Pour **ajouter votre espace d’hébergement** au Gestionnaire de site :

1. Cliquez sur le bouton **“Nouveau site”**. Une nouvelle entrée est créée dans la liste des sites. Donnez-lui un nom facilement identifiable.
2. Sur le côté droit, dans l’onglet **“Général**”, saisissez les paramètres fournis par votre hébergeur : **nom d’hôte**, **nom d’utilisateur** et **mot de passe**. Vous n’avez normalement pas à modifier les autres paramètres par défaut, à moins que votre hébergeur ne vous le demande.
3. Une fois tous les champs correctement renseignés, cliquez sur le bouton “Connexion”. Cette opération permettra d’enregistrer votre site dans la liste et de vous connecter à votre compte pour que vous puissiez vérifier que tout fonctionne correctement.

{% hint style="info" %}
Si FileZilla ne vous convient pas, voici quelques autres clients FTP connus :

* **Windows :**
  * CoreFTP: [http://www.coreftp.com/](http://www.coreftp.com/)
  * WinSCP: [http://winscp.net/](http://winscp.net/)
  * SmartFTP: [http://www.smartftp.com/](http://www.smartftp.com/)
* **Mac OS :**
  * Cyberduck: [http://cyberduck.ch/](http://cyberduck.ch/)
  * Transmit: [http://www.panic.com/transmit/](http://www.panic.com/transmit/)
  * Fetch: [http://fetchsoftworks.com/fetch/](http://fetchsoftworks.com/fetch/)
* **Unix/Linux :**
  * gFTP: [http://gftp.seul.org/](http://gftp.seul.org/)
  * NcFTP: [http://www.ncftp.com/ncftp/](http://www.ncftp.com/ncftp/)
  * Kasablanca: [http://kasablanca.berlios.de/](http://kasablanca.berlios.de/)
{% endhint %}

## Se préparer

Dans un premier temps, **vous devez décider de l’endroit où héberger PrestaShop.**&#x20;

Quatre possibilités s’offrent à vous par rapport à votre nom de domaine :

* Au niveau de la **racine du domaine** : [http://www.exemple.com/](http://www.example.com)
* Dans un **dossier** : [http://www.exemple.com/boutique/](http://www.example.com/shop/)
* Dans un **sous-domaine** : [http://boutique.exemple.com/](http://store.example.com)
* Dans le **dossier d’un sous-domaine** : [http://vêtements.exemple.com/boutique/](http://clothes.example.com/boutique/)

{% hint style="success" %}
Grâce à la [fonctionnalité multiboutique](../guide-utilisateur/configurer-boutique/parametres-avances/multiboutique.md), vous pouvez avoir autant de boutiques que vous le souhaitez avec une seule installation de PrestaShop 8, chacune avec son propre nom de domaine si nécessaire. Tenez-en compte lorsque vous décidez de votre organisation.

Quel que soit votre plan, la boutique par défaut résidera toujours à l’endroit où se trouve PrestaShop.
{% endhint %}



## Installer PrestaShop

Maintenant que votre configuration est effectuée, vous pouvez commencer l'installation de PrestaShop !

{% content-ref url="installer-prestashop.md" %}
[installer-prestashop.md](installer-prestashop.md)
{% endcontent-ref %}



{% hint style="success" %}
_Cette page a été mise à jour récemment._

**🗣 Que pensez-vous de cet article ? Dites-le nous !**&#x20;

Vos retours nous permettent d'améliorer la documentation PrestaShop pour toute la communauté ! 🙌

Vous pouvez utiliser les emojis, situé en bas à droite de ce article pour nous faire part de votre retour. ⬇️
{% endhint %}
