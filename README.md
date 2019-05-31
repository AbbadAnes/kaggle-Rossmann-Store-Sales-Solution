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


<h1>Séléction de variables</h1>
<p>
  L’Analyse de donnée n’est souvent pas suffisante pour choisir les variables à choisir lors des prédictions. Les Data-Scientists et les statisticiens ont opté pour d’autres méthodes additionnelles afin de s’assurer de la qualité des variables in- dépendantes et ne laisser que les variables les plus significatives pour prédire la variable dépendante. La méthode la plus simple et la plus efficace est Backward- elimination :
<br>
1.	Fixer un seuil de significativité pour rester dans le modèle (ici 0,01).
<br>
2.	Construire le modèle avec toutes les variables possibles.
<br>
3.	Prendre le prédicteur qui a le plus grand p-value si p-value > seuil passer à 4 sinon passer à 5.
<br>
4.	Enlever le prédicteur, recréer le modèle sans le prédicteur, recalculer les p- values revenir à 3.
<br>
5.	Le modèle est Prêt.
<br>
Cet algorithme nous a validé les variables suivantes :
 <br><br>
<p align="center">
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/pval.PNG" title="hover text">
</p>
</p>

<h1>Apprentissage</h1>
<h2>Réseaux de neuronnes</h2>
<h2>LSTM</h2>
<p>
 Il s’agit d’un réseau de neurones récurrent, très efficace pour résoudre les problèmes les plus difficiles. En effet, ce type de réseaux de neurones a la capacité
de prédire plusieurs sorties au même temps. De plus, son architecture lui permet
d’utiliser les sorties relatives à des moments passés dans la prédiction des sorties
relatives aux moments futurs. Cette caractéristique, le rend très efficace pour les
problèmes Timeseries Forcasting.
Les LSTMs sont le type le plus populaire des réseaux de neurones récurrents
car ils ont apporté une solution simple et efficace au problème du « Vanshing
Gradient » qui a ralenti l’évolution des réseaux de neurones récurent pour des
années.
</p>
<p align="center">
  LSTM
  <br><br>
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/lstm.jpg" width="450" title="hover text">
</p>


<h2>Algorithmes</h2>
<h2>K-Nearest Neighbors Regressor</h2>
<p>
Les K voisins les plus proches est un algorithme d’apprentissage automatique
simple qui prévoit une cible numérique ou catégorique en fonction d’une mesure
de similarité (par exemple, des fonctions de distance) selon une valeur précise de
nombre de voisin à prendre en considération.
Une implémentation simple de la régression KNN consiste à calculer la moyenne
de la cible numérique des K plus proches voisins. Une autre approche utilise
une moyenne pondérée en fonction de la distance inverse des K voisins les plus
proches.
</p>
<p align="center">
  KNN
  <br><br>
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/J5r01.png" width="450" title="hover text">
</p>



<h1>Performance</h1> 
<h2>Root Mean Square Percentage Error</h2>
<p align="center">
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/hey2.PNG"  title="hover text">
</p>
<br>
<p align="center">
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/hey.PNG"  title="hover text">
</p>

<h2>Comment utiliser le code ?</h2>
1. Clonez le projet et decompressez code.rar
<br>
2. Dans le dossier Dataset vous trouverez les dataset du projet
<br>
3. vous trouvez un fichier code.py pour visulaiser les données et toutes les étapes de la réalisation du projet.
<h2>Contribution et Remerciement</h2>
<h3>Projet réalisé par :</h3>
- Anes Abdelfatah ABBAD.
- Amira KETFI
