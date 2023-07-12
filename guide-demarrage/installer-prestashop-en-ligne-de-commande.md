---
description: >-
  PrestaShop propose également un installateur pour les installations de ligne
  de commande.
---

# Installer PrestaShop 8 en ligne de commande

## De quoi s’agit-il ? <a href="#installerprestashop1.7enlignedecommande-dequoisagit-il" id="installerprestashop1.7enlignedecommande-dequoisagit-il"></a>

{% hint style="info" %}
Cet installateur spécial permet d’installer PrestaShop sans navigateur web : il suffit de placer le contenu de l’archive zip sur votre serveur web pour pouvoir installer PrestaShop via l’interface de ligne de commande (ILC).&#x20;
{% endhint %}

N’importe quel logiciel d’ILC peut être utilisé tant que vous pouvez l’utiliser pour interagir avec les commandes du serveur : Bash, Windows PowerShell, OS X Terminal, PuTTY, etc.

L’intérêt d’avoir un installateur sous forme d’ILC en plus de l’installateur habituel intégré au navigateur est d’offrir cette possibilité aux utilisateurs avancés qui préfèrent souvent des interfaces de ligne de commande car elles sont souvent un moyen plus concis et puissant de contrôler un programme ou un système d’exploitation.

## Mode d’emploi <a href="#installerprestashop1.7enlignedecommande-modedemploi" id="installerprestashop1.7enlignedecommande-modedemploi"></a>

L’installateur ILC est facile d’utilisation : depuis votre terminal, **accédez au dossier `/install` (ou `/install-dev`)** (ce qui implique d’avoir auparavant décompressé le fichier prestashop.zip) et **lancez le script avec cette commande :**

```
$ php index_cli.php
```

Cette opération affiche les différentes options disponibles.

![La page "Option" de l'installateur ILC](../.gitbook/assets/53641263.png)

Toutes les options de l’installateur intégré au navigateur sont disponibles, avec leur valeur par défaut répertoriée. **Presque toutes les valeurs par défaut peuvent être laissées telles** quelles car vous pouvez les modifier dans le back-office de PrestaShop une fois l’installation terminée.&#x20;

{% hint style="info" %}
L'adresse e-mail et le mot de passe sont ceux utilisés pour créer le compte de back-office de l’administrateur.
{% endhint %}

Pour lancer l’installation, **il vous faudra fournir 5 arguments** :

* **domain**. L’emplacement où vous voulez que votre boutique apparaisse.
* **db\_server**. L’adresse du serveur de base de données.
* **db\_name**. Le nom de la base de données que vous souhaitez utiliser.
* **db\_user**. L’utilisateur de la base de données que vous souhaitez utiliser.
* **db\_password**. Le mot de passe du nom d’utilisateur de base de données ci-dessus.

Par exemple :

```
$ php index_cli.php --domain=exemple.com --db_server=sql.exemple.com --db_name=prestashop --db_user=root --db_password=123456789
```

![L'installateur ILC affiche le message "installation réussie"](../.gitbook/assets/53641264.png)

{% hint style="info" %}
Si vous définissez également la valeur `--email` pour qu’elle soit reliée à votre propre adresse, un courriel récapitulatif vous sera envoyé une fois l’installation terminée.
{% endhint %}

## Liste des arguments <a href="#installerprestashop1.7enlignedecommande-listedesarguments" id="installerprestashop1.7enlignedecommande-listedesarguments"></a>

Voici la **liste des arguments** pour `index_cli.php` à compter de la version 8 :

| **Nom**        | **Paramètre par défaut**                        | **Description**                                         |
| -------------- | ----------------------------------------------- | ------------------------------------------------------- |
| --step         | process                                         |                                                         |
| --language     | en                                              | code de langue iso                                      |
| --timezone     | localhost                                       |                                                         |
| --domain       | localhost                                       |                                                         |
| --db\_server   | localhost                                       |                                                         |
| --db\_user     | root                                            |                                                         |
| --db\_password | (blank)                                         |                                                         |
| --db\_name     | prestashop                                      |                                                         |
| --db\_clear    | 1 (true)                                        | Supprime les tables                                     |
| --db\_create   | 0 (false)                                       | Crée la base de données si elle n’existe pas encore     |
| --prefix       | ps\_                                            |                                                         |
| --engine       | InnoDB                                          | InnoDB/MyISAM                                           |
| --name         | PrestaShop                                      | Nom de la boutique                                      |
| --activity     | 0                                               |                                                         |
| --country      | fr                                              |                                                         |
| --firstname    | John                                            |                                                         |
| --lastname     | Doe                                             |                                                         |
| --password     | 0123456789                                      |                                                         |
| --email        | [pub@prestashop.com](mailto:pub@prestashop.com) |                                                         |
| --license      | 0 (false)                                       | Affiche la licence de PrestaShop                        |
| --newsletter   | 1 (true)                                        | Abonne l’administrateur à la newsletter de PrestaShop   |
| --send\_email  | 1 (true)                                        | Envoie un email à l’administrateur après l’installation |
