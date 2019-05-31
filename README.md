<h1>kaggle-Rossmann-Store-Sales-Solution
</h1>
<p align="center">
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/front_page.png" width="50%" title="logo">
</p>
Rossmann exploite plus de 3 000 pharmacies dans 7 pays européens. Les directeurs de magasin Rossmann sont actuellement chargés de prévoir leurs ventes
quotidiennes jusqu’à six semaines à l’avance. Les ventes en magasin sont influencées par de nombreux facteurs, notamment les promotions, la concurrence, les
vacances scolaires, les saisons et la localité. Sans que les gestionnaires individuels
prédisent les ventes en fonction de leurs circonstances particulières, la précision
des résultats peut varier considérablement.
Le but de ce projet, est de construire, comparer et évaluer des modèles permettant
de prédire au mieux les ventes de 1115 magasins « Rossmann ».

<h2> Outils : </h2>
Python : Sickit-Learn, Keras, Matplotlib, Pandas, Numpy
<h2>Données</h2>
Le jeu de données, provenant de Kaggle 1
, est une combinaison de données chronologiques et d’une grande variété de fonctionnalités. On a récupéré deux jeux
de données (Train.csv et Store.csv) et un jeu de données test (test.csv) dont nous
devons prédire les ventes.
Chaque jeu de données contient des données historiques sur les ventes de la série
chronologique de 1 115 magasins Rossmann, sur une période allant du 1er janvier 2013 au 31 juillet 2015, avec près de 1 017 209 observations, ce qui catégorise
ce problème dans la classe « Time Series Forcasting », une classe très importante
et délicate dans le domaine du Machine Learning.

<br>
<a target="_blank" href="https://www.kaggle.com/c/rossmann-store-sales/data">Lien vers les données</a>


<h1>Analyse de données</h1>
<h2>Matrice de Corrélation</h2>
<p align="center">
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/corr.jpg"  width="70%" title="hover text">
</p>
<p> 
 La matrice de corrélation ci-dessous montre la corrélation entre les différentes caractéristiques des données d’apprentissage.
Comme on peut le constater, les ventes sont fortement influencées par les promo- tions en cours, la semaine et les jours fériés, ainsi que par la corrélation évidente entre les ventes et le nombre de clients et le fait que le magasin soit ouvert ou non.
</p>

<h2>Relation entre Promo et les ventes</h2>
<p> 
Le graphique ci-dessous=indique la moyenne des ventes (dans tous les maga- sins) les jours avec ou sans promotions.
L’effet de la promotion sur les ventes est clairement évident, la promotion ayant un effet fortement positif sur celle ci.
</p>
<p align="center">
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/Page-12-Image-5.jpg"  title="hover text">
</p>


<h2>Les clients est une information très importante</h2>
<p align="center">
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/Page-12-Image-6.jpg"  title="hover text">
</p>
<p> 
Le graphique ci-dessus montre la relation entre les ventes et les clients. Nous remarquons que le les ventes et clients sont fortement corrélés.
</p>


<h1>Apprentissage</h1>
<h2>Algorithme utilisé</h2>
<p align="center">
  SVM ( Support Vector Machine )
  <br><br>
  <img src="https://zestedesavoir.com/media/galleries/3985/5128cf36-de17-4ebb-9495-90c9d85f006f.png" width="350" title="hover text">
</p>
<h1>Performance</h1> 
<h2>Accuracy</h2>
Accuracy = # prédictions correctes / # prédictions totales
<br>
<strong> Accuracy = 98% </strong>
<h2>Courbes d'apprentissage</h2>

<h2>Comment utiliser le code ?</h2>
1. Clonez le projet et decompressez code.rar
<br>
2. Dans le dossier R vous trouverez les scripts nécessaires pour récuperer les données à partir de la platforme TCGA
<br>
3. Dans le dossier Python vous trouvez un fichier visualisation.py pour visulaiser les données, et un deuxième fichier implementation.py qui contient toutes les étapes de la réalisation du projet.
<h2>Contribution et Remerciement</h2>
<h3>Projet réalisé par :</h3>
- Anes Abdelfatah ABBAD.
