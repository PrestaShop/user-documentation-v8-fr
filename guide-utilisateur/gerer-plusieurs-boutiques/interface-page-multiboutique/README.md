# Interface de la page multiboutique

## La page Multiboutique <a href="#interfacedelapagemultiboutique-linterfacemultiboutique" id="interfacedelapagemultiboutique-linterfacemultiboutique"></a>

### Comprendre l'organisation de la page Multiboutique

{% hint style="info" %}
Pour accéder à la page Multiboutique, il faut d'abord [activer la fonctionnalité](../#activer-la-fonctionnalite-multistore) dans **Paramètres Avancés > Pamètres généraux**.&#x20;
{% endhint %}

Une nouvelle page est désormais disponible dans le menu **Paramètres Avancés :** la page **Multiboutique**.

Cette page est divisée en 3 sections :

* **L'arbre multiboutique** : L'arbre multiboutique vous donne un aperçu de vos boutiques organisées en différents groupes.
* **Multiboutique :** Ce tableau liste tous les groupes que vous avez créés, qu'ils soient activés ou non.
* **Options multiboutiques :** Dans cette section, vous pouvez sélectionner la boutique par défaut.

{% content-ref url="ajouter-nouvelle-boutique.md" %}
[ajouter-nouvelle-boutique.md](ajouter-nouvelle-boutique.md)
{% endcontent-ref %}

{% content-ref url="ajouter-groupe-boutiques.md" %}
[ajouter-groupe-boutiques.md](ajouter-groupe-boutiques.md)
{% endcontent-ref %}

{% content-ref url="mettre-en-place-url-boutique.md" %}
[mettre-en-place-url-boutique.md](mettre-en-place-url-boutique.md)
{% endcontent-ref %}

## Travailler dans des contextes différents

### Savoir dans quel contexte vous vous trouvez

Lorsque la fonctionnalité multiboutique est activée, vous pouvez appliquer des modifications à tous les magasins, à un groupe de magasins ou à un magasin spécifique, en fonction du contexte sélectionné dans le sélecteur déroulant ou dans l'en-tête (à partir de la 1.7.8.0).

* **Toutes les boutiques :** Les changements s'appliqueront à toutes vos boutiques.
* **Groupe X :** Les changements s'appliqueront uniquement aux boutiques du groupe X.
* **Boutique Y :** Les changements s'appliqueront uniquement à la boutique Y.

#### Le menu déroulant (anciennes versions et pages non mises à jour)

Le menu déroulant en haut de chaque page du back-office indique le contexte dans lequel vous travaillez (toutes les boutiques, groupe de boutiques, ou une boutique spécifique).

![](<../../../.gitbook/assets/image (45).png>)

#### L'en-tête

L'interface multiboutique évolue et le menu déroulant se transforme en en-tête sur la plupart des pages.

![](<../../../.gitbook/assets/image (42).png>)

{% hint style="success" %}
La couleur des boutiques et des groupes de boutiques peut être modifée sur la page **Paramètres Avancés > Multiboutique.** Ainsi, la couleur de l'en-tête change selon du contexte dans lequel vous vous trouvez et vous pouvez ainsi savoir en un coup d'oeil sur quelle(s) boutique(s) vous êtes en train de travailler.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

### Appliquer des modifications à une boutique ou un groupe de boutiques

Pour appliquer des changements à une boutique spécifique ou un groupe de boutiques, changez de contexte avec l'en-tête et sélectionnez le groupe ou la boutique que vous voulez personnaliser.

L'interface peut être différente selon votre version de PrestaShop et la page sur laquelle vous vous trouvez :

#### Le bouton à bascule et les cases à cocher (anciennes versions et pages non mises à jour)

Dans un contexte de groupe de boutiques ou de boutique spécifique, de nouvelles options apparaissent sur la page, vous permettant de personnaliser les réglages de la boutique ou du groupe sélectionné.

* Un bouton à bascule (Oui/Non).
* Une case à cocher à côté de chaque paramètre à modifier.

**Pour faire des modifications :**

1. Pour que tous les paramètres d'une section soient modifiables, réglez le bouton à bascule multiboutique sur "Oui". Si vous souhaitez uniquement personnaliser un paramètre spécifique, **cochez la case correspondante.**
2. Une fois qu'un paramètre est modifiable, apportez vos modifications puis enregistrez.

{% hint style="info" %}
En réglant le bouton à bascule multiboutique sur "oui" ou en cochant une case, le ou les paramètres sont modifiables mais leur valeur n'est pas modifiée. C'est à vous d'effectuer vos ajustements et de sauvegarder.
{% endhint %}

#### Les cases à cocher

Les cases à cocher sont affichées lorsque vous travaillez dans un contexte de groupes de boutiques ou de boutique spécifique. Elles vous permettent de modifier un paramètre d'une boutique spécifique ou un groupe de boutiques et d'ainsi conserver une trace de cette modification.

Si la case est cochée la prochaine fois que vous vous rendrez sur la page, cela signifie que le paramètre est personnalisé pour la boutique ou le groupe de boutiques sur lequel vous travaillez. En décochant la case, vous annulez la personnalisation et le paramètre prend la même valeur qu'en contexte "Toutes les boutiques" (ou le contexte du groupe, le cas échéant).

Par exemple, dans la capture d'écran ci-dessous, la case à côté du paramètre "Texte de maintenance" est cochée. Cela signifie que ce paramètre est personnalisé dans la boutique 1.

![](<../../../.gitbook/assets/image (57).png>)

### Garder la trace des modifications apportées à une seule boutique

#### La liste déroulante des paramètres spécifiques

Grâce à la liste déroulante des paramètres spécifiques, si vous apportez des modifications à une seule boutique, et que vous revenez ensuite au contexte "Toutes les boutiques" ou groupe, vous pourrez facilement savoir quels paramètres ont été modifiés dans une boutique spécifique.

Ainsi, si vous voyez cette liste déroulante à côté d'un paramètre, cela signifie que ce paramètre a été personnalisé dans au moins une boutique. Déployez la liste déroulante pour voir quelle boutique est concernée.

![](<../../../.gitbook/assets/image (55).png>)

**Personnalisé :** Le paramètre a été modifié dans une boutique.

**Hérité :** Le paramètre est réglé de la même manière pour toutes les boutiques.
