# Initialisation

## Ressources

Exemple de sites cibles

https://www.blogduwebdesign.com/blog/graphisme/affiches-officielles-jo-paris-2024.html

https://monarchiebritannique.com/blog/linstitution/105-ordre-de-succession-au-trone-britannique

https://www.suzannecollinsbooks.com (en)


Liste des critères d'accessibilité
https://accessibilite.numerique.gouv.fr/methode/criteres-et-tests/

La grille d'audit est téléchargeable depuis la page Kit d'audit du site RGAA4
https://accessibilite.numerique.gouv.fr/ressources/kit-audit/

Téléchargez le fichier de la "Grille d’audit RGAA version 4.1.2" au format ODS.

## Initialiser la grille d'audit

Dans l'onglet "Échantillon" saisir les informations de date, auditeur et site 

Se positionner sur l'onglet "P1"

# Critères de tests

## Images
Choisir une page à tester dans la liste ci-dessus.

Passez les images en revue pur tester les critères de test suivants :

**1.1  Chaque image porteuse d’information a-t-elle une alternative textuelle ?**

**1.2 Chaque image de décoration est-elle correctement ignorée par les technologies d’assistance ? (en particulier le point 1.2.1)**

Pour cela observez le code source de chaque image en vous appuyant sur les attributs "alt" ou "title" de la balise HTML portant l'image.

Dans la grille d'audit, dans l'onglet "P1" modifiez le statut des deux critères en fonction des résultats du test. Il suffit d'une seule image non conforme pour invalider le test.

Si le critère n'est pas conforme, décrire une image non conforme et une suggestion de correction dans la colonne "Modification à apporter".

## Couleurs

De la même façon que pour les images, testez le critère suivant en parcourant le contenu de la page :

**3.1 Dans chaque page web, l’information ne doit pas être donnée uniquement par la couleur. Cette règle est-elle respectée ?**

 Ensuite, installez l'extension WCAG contrast checker

 https://chromewebstore.google.com/detail/wcag-color-contrast-check/plnahcmalebffmaghcpcmpaciebdhgdf (Chrome)

 https://addons.mozilla.org/en-US/firefox/addon/wcag-contrast-checker/ (Firefox)

 A l'aide de ces extensions vérifiez les critères :

**3.2 Dans chaque page web, le contraste entre la couleur du texte et la couleur de son arrière-plan est-il suffisamment élevé (hors cas particuliers) ?**

**3.3 Dans chaque page web, les couleurs utilisées dans les composants d’interface ou les éléments graphiques porteurs d’informations sont-elles suffisamment contrastées (hors cas particuliers) ?** 

## Liens

Vérifiez les critères suivant en passant en revue l'ensemble des liens hypoertextes visibles sur la page :
 
 **6.1 Chaque lien est-il explicite (hors cas particuliers) ?** en vous appuyant sur les définitions du test 6.1.1
 
 **6.2 Dans chaque page web, chaque lien a-t-il un intitulé ?** en vous appuyant sur les définitions du test 6.2.1

## Éléments obligatoires

Vérifiez le critère en affichant le code source de la page :

**8.1 Chaque page web est-elle définie par un type de document ?** en vous appuyant sur les tests 8.1.1 à 8.1.3

Vérifiez le critère :

**8.2 Pour chaque page web, le code source généré est-il valide selon le type de document spécifié ?**

Pour cela, le W3C met à disposition un outil de validation de la norme HTML

https://validator.w3.org/#validate_by_uri

L'outil de validation liste toutes les erreurs de format HTML. Seules certaines erreurs sont pénalisantes pour la validation du critère 8.2. Utilisez la méthodologie du test 8.2.1 pour tester le critère en détail.

Vérifiez les critères suivant en analysant le code source et à l'aide des critères de test de la documentation RGAA4 :

**8.3 Dans chaque page web, la langue par défaut est-elle présente ?**

**8.4 Pour chaque page web ayant une langue par défaut, le code de langue est-il pertinent ?**

**8.5 Chaque page web a-t-elle un titre de page ?**

**8.6 Pour chaque page web ayant un titre de page, ce titre est-il pertinent ?** 

## Structuration de l'information

 Installez l'extension Headingsmap 

 https://chromewebstore.google.com/detail/headingsmap/flbjommegcjonpdmenkdiocclhjacmbi (Chrome)

https://addons.mozilla.org/fr/firefox/addon/headingsmap/ (Firefox)

A l'aide de l'extension headingsmap testez le critère :

 **9.1 Dans chaque page web, l’information est-elle structurée par l’utilisation appropriée de titres ?** 

<hr>
Analysez le code source de la page afin d'identifier les zones encapsulées dans des balises **header** et **main**

Vérifiez si les zones de navigation sont encapsulées dans des balises `<nav>`

A l'aide de votre analyse testez le critère :

 **9.2 Dans chaque page web, la structure du document est-elle cohérente (hors cas particuliers) ?** 
<hr>
 Identifiez les listes présentes dans la page et vérifiez qu'elles sont bien structurés en HTML.

 A l'aide de votre analyse testez le critère :

**9.3 Dans chaque page web, chaque liste est-elle correctement structurée ?**
<hr>

Identifiez les citations présentes dans la page et vérifiez qu'elles sont bien structurés en HTML.

 A l'aide de votre analyse testez le critère :

**9.4 Dans chaque page web, chaque citation est-elle correctement indiquée ?**


# Conclusions

Dans la grille d'audit, dans l'onglet "P1" modifiez le statut de tous les critères non testés pour "N/A". Refaire la même manip sur les autres pages testées.

Dans l'onglet "Base de calcul" supprimer toutes les colonnes associées aux pages non testées. Si vous avez testé une seule page, supprimez les références des page P2 à P20 (colonnes E-W et AG-AY)

Vérifiez dans l'onglet "synthèse" le taux d'accessibilité évalué à ce stade.
