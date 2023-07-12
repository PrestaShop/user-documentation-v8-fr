# Installer PrestaShop 8 sur votre ordinateur

Vous pouvez installer PrestaShop sur votre machine locale pour tester l’application avant d’investir de l’argent dans un serveur et un nom de domaine, ou pour personnaliser votre boutique en local avant de transférer vos modifications vers une installation PrestaShop déjà disponible en ligne.

L’installation en local d’une application web nécessite que vous installiez d’abord l’environnement adéquat, à savoir le serveur web Apache, l’interpréteur de langage PHP, le serveur de bases de données MySQL et, dans l’idéal, l’outil phpMyAdmin. C’est ce qu’on appelle l’ensemble **AMP : Apache+MySQL+PHP.**&#x20;

L'ensemble AMP existe pour de nombreux systèmes d’exploitation. Selon le système d'exploitation, une lettre vient s’ajoute à l’acronyme : WAMP (Windows+Apache+MySQL+PHP), MAMP (Mac OS X+...) et LAMP (Linux+...).

## Choisir un package AMP <a href="#installerprestashop1.7survotrepropreordinateur-choisirunpackageamp" id="installerprestashop1.7survotrepropreordinateur-choisirunpackageamp"></a>

Cette opération s’avère très technique. Heureusement, il existe de nombreux packages précompilés que vous pouvez installer facilement. Ils ne vous dispenseront pas de tous les aspects techniques, mais ils vous seront d’une grande aide. Étant donné que tous les éléments des packages sont en open source, ces installeurs sont gratuits la plupart du temps. Voici une sélection d’installeurs AMP gratuits :

* EasyPHP : [http://www.easyphp.org/](http://www.easyphp.org) (Windows)
* MAMP : [http://www.mamp.info/](http://www.mamp.info) (MacOS)
* WampServer : [http://www.wampserver.com](http://www.wampserver.com) (Windows)
* XAMPP : [https://www.apachefriends.org/fr/index.html](http://www.apachefriends.org/en/xampp.html) (Windows, MacOS, Linux, Solaris)

Choisissez le package qui vous paraît le plus pratique et lancez-le.

## Vérifier que tout fonctionne <a href="#installerprestashop1.7survotrepropreordinateur-verifierquetoutfonctionne" id="installerprestashop1.7survotrepropreordinateur-verifierquetoutfonctionne"></a>

{% hint style="info" %}
Avant de poursuivre ce tutoriel d’installation de PrestaShop, assurez-vous que tous les composants de votre package AMP fonctionnent :
{% endhint %}

*   **Le serveur web doit être opérationnel**. Vous devez être en mesure d’y accéder via votre navigateur en saisissant “127.0.0.1” dans la barre d’adresse.

    [`http://127.0.0.1`](http://127.0.0.1) est le “localhost”, c’est-à-dire “votre ordinateur” : il s’agit d’une adresse de retour qui dirige le navigateur vers votre serveur web local.

    En fait,[`http://127.0.0.1`](http://127.0.0.1) et [`http://localhost`](http://localhost) sont synonymes : vous pouvez utiliser l’un ou l’autre ; les deux renvoient vers le dossier racine de votre serveur web local.

    Il se peut que certains serveurs web ne fonctionnent pas car leurs ports de connexion (généralement, le port 80) sont déjà utilisés par une autre application.
* **Le serveur de base de données doit être opérationnel**. MySQL est l’endroit où toutes les données de PrestaShop sont stockées. Le package AMP vous indique clairement si MySQL est en cours d’exécution ou non.
* **L’outil phpMyAdmin doit être accessible**. Il s’agit de l’application web qui vous permet de gérer les données stockées dans MySQL. Son emplacement dépend du package AMP que vous avez choisi : il peut se trouver à l’adresse [`http://127.0.0.1/phpmyadmin`](http://127.0.0.1/phpmyadmin) (XAMPP, WampServer, MAMP), [`http://127.0.0.1/mysql`](http://127.0.0.1/mysql) (EasyPHP) ou à un autre emplacement. Consultez la documentation de votre package. Il se peut qu’il indique un bouton phpMyAdmin qui ouvre la bonne URL dans votre navigateur.

## Trouver le dossier racine du serveur web local <a href="#installerprestashop1.7survotrepropreordinateur-trouverledossierracineduserveurweblocal" id="installerprestashop1.7survotrepropreordinateur-trouverledossierracineduserveurweblocal"></a>

Une fois que vous avez vérifié que le package est correctement installé et que tous ses composants fonctionnent, vous devez trouver le dossier racine de votre serveur web local.

Il s’agit du dossier local dans lequel vous placerez les fichiers de votre application. Il peut être comparé au dossier racine de votre serveur en ligne. L’adresse [`http://127.0.0.1`](http://127.0.0.1) permet d’accéder uniquement à son contenu.

L’emplacement local réel du dossier dépend fortement du package AMP et peut être personnalisé :

* **EasyPHP :** `C:\easyphp\www`
* **MAMP :** `/Applications/MAMP/htdocs/`
* **WampServer :** `C:\wamp\www`
* **XAMPP :** `C:\xampp\htdocs` ou `/Applications/xampp/htdocs`

## Trouver les données utilisateur MySQL <a href="#installerprestashop1.7survotrepropreordinateur-trouverlesdonneesutilisateurmysql" id="installerprestashop1.7survotrepropreordinateur-trouverlesdonneesutilisateurmysql"></a>

Enfin, vous devez connaître le nom d’utilisateur et le mot de passe de MySQL pour installer PrestaShop.

{% hint style="info" %}
**La plupart des packages utilisent le nom d’utilisateur "root" et un mot de passe vide**, y compris EasyPHP, MAMP, WampServer et XAMPP.

Lisez la documentation de votre package.
{% endhint %}

## Dernière remarque avant le tutoriel d’installation <a href="#installerprestashop1.7survotrepropreordinateur-derniereremarqueavantletutorieldinstallation" id="installerprestashop1.7survotrepropreordinateur-derniereremarqueavantletutorieldinstallation"></a>

Une fois tous ces éléments clarifiés et effectués, vous pouvez suivre les étapes du guide de mise en route et commencer à installer PrestaShop.

Lorsque vous installez PrestaShop en local, gardez à l’esprit que :

* Les **fichiers ne doivent pas être mis en ligne via un logiciel FTP** (comme FileZilla) **sur un serveur web** : il suffit de les déplacer dans le bon dossier local comme indiqué ci-dessus.
*   Vous **n’avez pas besoin de créer un nom de domaine local** : PrestaShop est disponible à l’adresse de bouclage indiquée ci-dessus : [http://localhost](http://localhost) ou [http://127.0.0.1](http://127.0.0.1).&#x20;

    PrestaShop est disponible à cette adresse en ajoutant le nom de son dossier, par exemple [http://localhost/prestashop](http://localhost/prestashop) ou [http://127.0.0.1/prestashop](http://127.0.0.1/prestashop) si PrestaShop est dans le sous-dossier `/prestashop/` du dossier racine local. Lorsque vous accédez à cette adresse pour la première fois, vous devriez être automatiquement redirigé vers l’installation de PrestaShop, sur [http://localhost/prestashop/install](http://localhost/prestashop/install) ou [http://127.0.0.1/prestashop/install](http://127.0.0.1/prestashop/install).\


{% hint style="success" %}
Avez-vous tout lu ? À présent, suivez le guide d’installation habituel en commençant directement par la section “Créer une base de données pour votre boutique” : [Installer PrestaShop](installer-prestashop.md).
{% endhint %}





{% hint style="success" %}
_Cette page a été mise à jour récemment._

**🗣 Que pensez-vous de cet article ? Dites-le nous !**&#x20;

Vos retours nous permettent d'améliorer la documentation PrestaShop pour toute la communauté ! 🙌

Vous pouvez utiliser les emojis, situé en bas à droite de ce article pour nous faire part de votre retour. ⬇️
{% endhint %}
