# Initialisation

## Ressources

Le site de test :
https://accessibility-luxembourg.github.io/exercices-formation/index.html

Dans le cadre du TP les tests d'accessibilités seront effectués sur les pages suivantes du site : page d'accueil, graphiques, données et actualités.


Liste des critères d'accessibilité
https://accessibilite.numerique.gouv.fr/methode/criteres-et-tests/

La grille d'audit est téléchargeable depuis la page Kit d'audit du site RGAA4
https://accessibilite.numerique.gouv.fr/ressources/kit-audit/

Téléchargez le fichier de la "Grille d’audit RGAA version 4.1.2" au format ODS.

## Initialiser la grille d'audit

Dans l'onglet "Échantillon" saisir les informations de date, auditeur et site 

Se positionner sur l'onglet "P1"

# Critères de tests

> [!IMPORTANT]
> Le RGAA contient 106 critères mais **seuls les critères listés ci dessous** doivent être testés dans le cadre du TP.

## Images
Choisir une page à tester dans la liste ci-dessus.

Passez les images en revue pur tester les critères de test suivants :

**1.1  Chaque image porteuse d’information a-t-elle une alternative textuelle ?**

**1.2 Chaque image de décoration est-elle correctement ignorée par les technologies d’assistance ? (en particulier le point 1.2.1)**

Pour cela observez le code source de chaque image en vous appuyant sur les attributs "alt" ou "title" de la balise HTML portant l'image. Si l'image contient une information utile, cette information doit être également présente dansun attribut "alt" ou "title". Sinon l'image doit avoir un attribut "alt" ou "title" vide.

Dans la grille d'audit, dans l'onglet "P1" modifiez le statut des deux critères en fonction des résultats du test. Il suffit d'une seule image non conforme pour invalider le test.

Si le critère n'est pas conforme, décrire une image non conforme et une suggestion de correction dans la colonne "Modification à apporter".

> Cette démarche est à reproduire ensuite dans tous les tests ci dessous. Pour chaque test, trouver la ligne correspondant au critère, mettre à jour l'état du critère testé (conforme "C", non-conforme "NC" ou non applicable "NA") et en cas de non conformité, décrire l'origine et  l'emplacement de l'erreur (à quel endroit dans quelle page)

## Couleurs

De la même façon que pour les images, testez le critère suivant en parcourant le site :

**3.1 Dans chaque page web, l’information ne doit pas être donnée uniquement par la couleur. Cette règle est-elle respectée ?**

Pour tester ce critère vous pouvez émuler la visibilité d'une page en mode "daltonien": 

 + dans Firefox utilisez la console > onglet "accessibilité" > bouton "simuler" > aucune couleur
 + dans Chrome utilisez la console> menu trois points (customize) > plus d'outils > rendering > emulate vision defiencencies > no-color

 Ensuite, installez l'extension WCAG contrast checker

 + https://chromewebstore.google.com/detail/wcag-color-contrast-check/plnahcmalebffmaghcpcmpaciebdhgdf (Chrome)
 + https://addons.mozilla.org/en-US/firefox/addon/wcag-contrast-checker/ (Firefox)

 A l'aide de ces extensions vérifiez les critères :

**3.2 Dans chaque page web, le contraste entre la couleur du texte et la couleur de son arrière-plan est-il suffisamment élevé (hors cas particuliers) ?**

**3.3 Dans chaque page web, les couleurs utilisées dans les composants d’interface ou les éléments graphiques porteurs d’informations sont-elles suffisamment contrastées (hors cas particuliers) ?** 

## Liens

Vérifiez les critères suivants en passant en revue l'ensemble des liens hypertextes visibles sur la page :
 
 **6.1 Chaque lien est-il explicite (hors cas particuliers) ?** en vous appuyant sur les définitions du test 6.1.1
 
 **6.2 Dans chaque page web, chaque lien a-t-il un intitulé ?** en vous appuyant sur les définitions du test 6.2.1

## Éléments obligatoires

Vérifiez le critère en vérifiant les balise du tout début le code source de la page. Aidez vous des détails des tests 8.1.1 à 8.1.3

**8.1 Chaque page web est-elle définie par un type de document ?** 

<hr>

Faites passer à votre page le test de validation de conformité de code HTML. Pour cela, le W3C met à disposition un outil de validation en ligne :

https://validator.w3.org/#validate_by_uri

L'outil de validation liste toutes les erreurs de format HTML. Seules certaines erreurs sont pénalisantes pour la validation du critère 8.2. Utilisez la méthodologie du test 8.2.1 pour tester le critère en détail.
**8.2 Pour chaque page web, le code source généré est-il valide selon le type de document spécifié ?**
<hr>

Vérifiez les critères suivant en analysant le contenu de la balise `<head>` au début du code source de la page et à l'aide des critères de test de la documentation RGAA4 :

**8.3 Dans chaque page web, la langue par défaut est-elle présente ?**

**8.4 Pour chaque page web ayant une langue par défaut, le code de langue est-il pertinent ?**

**8.5 Chaque page web a-t-elle un titre de page ?** 

**8.6 Pour chaque page web ayant un titre de page, ce titre est-il pertinent ?** 

## Structuration de l'information

 Installez l'extension Headingsmap 

+ https://chromewebstore.google.com/detail/headingsmap/flbjommegcjonpdmenkdiocclhjacmbi (Chrome)
+ https://addons.mozilla.org/fr/firefox/addon/headingsmap/ (Firefox)

A l'aide de l'extension headingsmap testez le critère :

 **9.1 Dans chaque page web, l’information est-elle structurée par l’utilisation appropriée de titres ?** 

<hr>
Analysez le code source de la page afin d'identifier que les grandes "structures" de page HTML sont respectées

```
<header></header>
<main></main>
<footer></footer>
```
 
Vérifiez si les zones de navigation sont encapsulées dans des balises `<nav>`



A l'aide de votre analyse testez le critère :

 **9.2 Dans chaque page web, la structure du document est-elle cohérente (hors cas particuliers) ?** 
<hr>
 Identifiez les listes présentes dans la page et vérifiez qu'elles sont bien structurés en HTML à l'aide de l'éditeur de code source.

 En fonction des résultats de votre analyse validez ou invalidez le critère :

**9.3 Dans chaque page web, chaque liste est-elle correctement structurée ?**
<hr>

Identifiez les citations présentes dans la page et vérifiez qu'elles sont bien structurés en HTML à l'aide de l'éditeur de code source.

En fonction des résultats de votre analyse validez ou invalidez le critère :

**9.4 Dans chaque page web, chaque citation est-elle correctement indiquée ?**

## Présentation de l’information

Utiliser la navigation au clavier (tab et shift+tab) afin de parcourir les éléments d'intéraction de la page (liens, boutons, éléments de formulaires). Chaque élément qui "recoit" le focus clavier doit être graphiquement mis en valeur.

En fonction des résultats de votre analyse validez ou invalidez le critère :

**10.7 Dans chaque page web, pour chaque élément recevant le focus, la prise de focus est-elle visible ?**
<hr>

Utilisez l'outil de visualisation responsive du navigateur pour afficher le site sur une largeur de 320 pixels. Vériviez qu'il n'y a pas de barre de défilement horizontale.

En fonction des résultats de votre analyse validez ou invalidez le critère :

**10.11 Pour chaque page web, les contenus peuvent-ils être présentés sans perte d’information ou de fonctionnalité et sans avoir recours soit à un défilement horizontal pour une fenêtre ayant une largeur de 320 px (hors cas particuliers) ?**

## Navigation

Identifiez les méthodes de navigation accessibles depuis la page : menu de navigation, plan du site, moteur de recherche.

En fonction du nombre de méthodes disponibles validez ou invalidez le critère :

**12.1 Chaque ensemble de pages dispose-t-il de deux systèmes de navigation différents, au moins (hors cas particuliers) ?**
<hr>

Une fois les méthodes de navigation identifiées sur la page, naviguez à l'interieur du site et validez ou invalidez le critère :

**12.2 Dans chaque ensemble de pages, le menu et les barres de navigation sont-ils toujours à la même place (hors cas particuliers) ?**
<hr>

Comme pour le test 10.7, passez la page en revue en utilisant le clavier uniquement (tab ou shift + tab). Au début de la page, la navigation clavier doit réveler un menu de raccourcis vers le contenu de la page (c'est ce qu'on appelle un menu d'évitement).

En fonction des résultats de votre analyse validez ou invalidez le critère :

**12.7 Dans chaque page web, un lien d’évitement ou d’accès rapide à la zone de contenu principal est-il présent (hors cas particuliers) ?**

Si vous ne voyez pas de menu d'évitement, essayez de trouver un exemple de site avec un tel menu.

# Conclusions

Dans la grille d'audit, dans l'onglet "P1" modifiez le statut de tous les critères non testés pour "N/A". Refaire la même manip sur les autres pages testées.

Dans l'onglet "Base de calcul" supprimer toutes les colonnes associées aux pages non testées. Si vous avez testé une seule page, supprimez les références des page P2 à P20 (colonnes E-W et AG-AY)

Vérifiez dans l'onglet "synthèse" le taux d'accessibilité évalué à ce stade.
