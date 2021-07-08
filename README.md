# Data-science-Open-Food-Fact

I) Problématique
Le projet sera notamment dévolu à des travail autour des concepts liés aux transitions alimentaires sur la base de données Open Food Facts.
Voici donc quelques questions que l’on peut se poser sur ces données Open Food Facts :
- Quels sont les discours des fournisseurs, selon leurs descriptions ? Les discours diffèrent-ils avec
le(s) type(s) de métier ? Selon cette étude de discours, que semblent vouloir communiquer les
fournisseurs en circuit court (numérique) à leurs clients (les membres des ruches, qui ont accès à ces
données) ?

- Y a-t-il un lien entre les tailles (nombre d’employé, ou taille d’exploitation en hectares), et leur
ancienneté, à la fois générale, et ancienneté dans le réseau Ruche ?
- Où se situent ces fournisseurs sur le plan géographique ?
- Y a-t-il des liens entre différentes professions (se retrouvant souvent ensemble chez un même
fournisseur ?) ? Que nous disent ces liens sur la complémentarité entre métiers et la volonté
d’intégration au sein d’une même filière ou d’un même produit ?
- Y a-t-il un lien entre le volume de distributions et la date d’arrivée dans le réseau, de première
distribution... ?
Il y a d’autres questions que vous relèverez peut-être vous même mais l’intérêt pour vous est de réfléchir aux enjeux de cette analyse de données en terme de questions de recherche sur une base de données contenant presque 2 millions de références, alimentée via un dispositif de self-scanning, et dont la finalité est de fournir aux consommateurs, citoyens, mangeurs, des informations transparentes, ainsi que des formes d’évaluations qualitatives liées aux produits mais aussi à leurs impacts environnementaux.

II) Base de données

La base de données s’obtient sous différents formats, dont le format csv qui permet l’étude par CorText.Manager, via le site d’Open Food Facts : https://fr.openfoodfacts.org.

En haut au milieu de cette page d’accueil, vous trouverez un champ « chercher un produit ». Je vous
invite à choisir le terme de requête (ex : « cacao », « citron », « yaourt »). 

Il y a une limite de 10 000
au nombre de produits que vous pouvez télécharger sous forme de base de données, je vous invite donc à choisir un terme qui vous donnera le plus de résultats possibles tout en restant dans la limite
(avoir au minimum 2500 produits me paraît réalisable pour un grand nombre de cas, mais si vous pouvez en avoir 8000 ou 9000, c’est mieux).

Dans le tableau, vous verrez un grand nombre de données différentes. Je vous invite à travailler sur les données de votre choix mais je vous conseille fortement de vous focaliser sur celles qui sont en
gras ci-dessous. Elles ont trait à la fois aux qualités des produits représentées par le Nutri-Score et la classification NOVA (qualités nutritionnelles, degrés de transformation) et à la dimension liée à
l’impact environnemental représenté notamment par le EcoScore (type d’emballages, origines des ingrédients). Bien entendu, les données de catégories permettant de classer les différents types de
produits dans votre base de données sont essentielles. 

Code = identifiant
• Creator = nickname du contributeur
• Generic name = description détaillée du produit
• Packaging = emballages employés (carton, plastique etc.)
• Brands = marques
• Categories = multiples catégories de produits figurant sur une même référence
• Origins = origines des ingrédients (quand elles sont mentionnées)
• Manufacturing places = lieu de fabrication (pays voire adresse exacte)
• Labels = « bio », « Max Havelaar », « sans gluten », « fabriqué en France », etc.
• Stores = enseigne où l’achat ou le scan du produit a eu lieu
• Countries = pays de l’enseigne d’achat / scan
• Ingredients = ingrédients au complet
• Allergens ; traces = allergènes et traces d’allergènes
• Additives n = nombre d’additifs
• Additives tags = noms des additifs
• Ingredients from palm oil ; ingredients from palm oil tags ; ingredients that may be from
palm oil = présence ou non d’ingrédients contenant à coup sûr ou potentiellement de l’huile
de palme, ainsi que leurs noms
• Nutri-score_score = score exact (légèrement négatif à fortement positif, par exemple -1 à
+18)
• Nutri-score_grade = A, B, C, D, E
• Nova_group = classification selon le degré de transformation des aliments :

- 1 : Aliments non transformés ou transformés minimalement (ex : cacao)
- 2 : Ingrédients culinaires transformés(ex : chocolat)
- 3 : Aliments transformés (ex : Chocolat)
- 4 : Produits alimentaires et boissons ultra-transformés (ex : Nutella)
• Eco-score = impact écologique lié à l’Analyse du Cycle de Vie
→ L'analyse de cycle de vie est une méthode d'évaluation normalisée permettant de réaliser
un bilan environnemental multi-étapes et multi-critères :
- 6 étapes de production : agriculture, transformation, emballage, transport, distribution et
consommation
- 14 indicateurs d’impacts environnementaux : changement climatique / empreinte carbone,
appauvrissement de la couche d'ozone, rayonnements ionisants, utilisation des sols, de l’eau,
et de l’énergie ; pollution de l’air et de l’eau marine et de l'eau douce (particules,
acidification, eutrophisation) ; et épuisement des ressources.
• Main category = catégorie principale du produit (ex : bonbons)
• Energy 100g = énergie en kj pour 100g de produit
• Fat 100g = graisses pour 100g de produit
• Saturated fat 100g = graisses saturées pour 100g de produit
• Acids = nombreuses catégories (ex : acide citrique)
• Carbohydrates = glucides
• Sugars = sucres
• Fibres
• Proteins = protéines
• Salt = sel
• Vitamins = nombreuses catégories (ex : vitamine C)
• Minéraux = nombreuses catégories (ex : magnesium)
• Carbon footprint = lié à l’Analyse du Cycle de Vie (inclut une catégorie liée aux viandes et
poissons)
