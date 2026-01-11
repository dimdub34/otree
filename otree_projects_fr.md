## Projets en économie comportementale avec oTree

### Instructions générales

Travail en équipe de 2 ou 3. 

Chaque projet doit comprendre :

1. Une **application oTree fonctionnelle**.
2. Un fichier `tests.py` permettant de **simuler des participants (bots)** pour tester le bon fonctionnement et produire un jeu de données.
3. Une **analyse de données** descriptive (Python ou R) à partir des données simulées.
4. Une **présentation orale** de 15–20 minutes comprenant :
   - **Pitch (5 min)** : contexte, problème du "client", hypothèse comportementale, solution expérimentale
   - **Démo (10 min)** : démonstration de l’application oTree
   - **Analyse (5 min)** : résultats simulés et visualisation

---

### Projet 1 : Le pouvoir de la rareté (e-commerce)

**Contexte :** Un site de e-commerce souhaite savoir dans quelle mesure l’affichage de messages de rareté augmente les taux de clic ou d’achat.

**Question de recherche :** Le type de rareté (quantitative vs. sociale) a-t-il un effet sur les comportements d’achat ?

💡 **Design :** 3 conditions
- Contrôle : "En stock"
- Rareté quantitative : "Plus que 2 articles !"
- Rareté sociale : "12 personnes consultent cet article"

**Pistes :** minuteur, justification du choix, variation de prix

---

### Projet 2 : Cadrage et abonnements (plateforme streaming)

**Contexte :** Une plateforme souhaite savoir dans quelle mesure le cadrage des tarifs influence les choix d’abonnement.

**Question :** Les mentions de gain ou de flexibilité modifient-elles les choix ?

💡 **Design :** 3 conditions : neutre, gain ("2 mois offerts"), flexibilité ("annulable à tout moment")

**Pistes :** ajouter une justification post-choix, perception du meilleur plan


---

### Projet 3 : Recommandations sociales vs. algorithmiques

**Contexte :** Un site de mode veut savoir si les clients préfèrent les recommandations sociales ("produit populaire") ou algorithmiques ("sélectionné pour vous").

**Question :** Quel type de recommandation maximise le taux de clic ?

💡 **Design :** 2 conditions : sociale vs. algo ; interface d’achat avec plusieurs produits

**Pistes :** score de recommandation, mesure de confiance, perception d’efficacité


---

### Projet 4 : Confiance envers un influenceur

**Contexte :** Une marque veut savoir quel est l’impact d’une présentation produit par un influenceur vs. une fiche technique neutre

**Question :** L’endossement augmente-t-il la confiance ou l’intention d’achat ?

💡 **Design :** 2 conditions (neutre / influenceur), mesure d’un score de confiance ou achat (slider, Likert)

**Pistes :** style d’influenceur, effet perçu sur la qualité ou le prix


---

### Projet 5 : L'effet de leurre (stratégie de prix)

**Contexte :** Un site de e-commerce veut orienter vers un produit premium via un produit leurre (plus cher ou moins attractif).

**Question :** L’ajout d’un leurre augmente-t-il le choix du produit premium ?

💡 **Design :** 2 conditions : avec/sans leurre asymétrique

**Pistes :** leurre inversé (favoriser le produit basique), perception du meilleur rapport qualité-prix


---

### Projet 6 : Le "green nudge" (RSE)

**Contexte :** Un supermarché en ligne souhaite réduire les emballages via des nudges pour promouvoir les produits en vrac

**Question :** Un signal social ("80% choisissent cela") ou écologique ("50g de plastique évités") est-il plus efficace ?

 💡 **Design :** 3 conditions : neutre / norme sociale / impact écologique

**Pistes :** empreinte carbone, incitation financière, ordonnancement du panier


---

### Projet 7 : Incitations et productivité (plateforme de travail)

**Contexte :** Une plateforme de livraison teste deux types de bonus (fixe ou aléatoire)

**Question :** Le type d’incitation (bonus fixe vs. loterie à valeur espérée identique) affecte-t-il l’effort ?

💡 **Design :** Tâche réelle ("real effort task") chronométrée

**Pistes :** ajout d’une mesure de confiance, stress


---

### Projet 8 : Honnêteté et déclarations (assurance)

**Contexte :** Une compagnie veut tester si le moment de la signature d’engagement (avant vs. après) réduit la fraude

**Question :** Signer une déclaration avant modifie-t-il la déclaration d’un résultat aléatoire (ex : lancer de dé) ?

💡 **Design :** 2 conditions : signature avant ou après

**Pistes :** ajout de valeurs morales


---

### Projet 9 : Vote et format d'information

**Contexte :** Une collectivité souhaite tester si la façon de présenter les candidats ou les informations influence le vote

**Question :** Le format ou l’ordre de l’information influence-t-il les choix démocratiques ?

💡 **Design :** Simuler un bulletin de vote (3 ou 4 candidats) avec variation de l’ordre, des visuels, ou du contenu informatif

**Pistes :** ajouter un traitement "score objectif" vs. "slogan", ou une ancre aléatoire


---

### Projet 10 : Choix environnementaux (transport / livraison)

**Contexte :** Une entreprise veut savoir si les clients sont prêts à faire un effort pour l’environnement (ex : livraison plus lente mais plus verte)

**Question :** Les gens sont-ils prêts à renoncer à du confort pour un impact environnemental positif ?

💡 **Design :** Choix multiples entre options équivalentes avec trade-off confort/impact/carbone

**Pistes :** affichage d’impact cumulé, feedback collectif, effet de norme


