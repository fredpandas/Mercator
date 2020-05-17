<h1>Carte de Mercator</h1>

<blockquote style="border-left: 10px solid black">
  <b>Auteur : </b>Bro Frédéric</b>
</blockquote>
<br>
<b>Lien pour exécuter ces notebooks dans mybinder :</b>

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fred-pandas/Mercator/master)
<br>
:white_square_button:<b> Préambule :</b>
<ul>
  <li><b>Public visé : </b> Terminale spécialité</li>
  <li><b>Mots clefs : </b> Loxodromie - Logarithme - Méthode d'Euler - Equations </li>
  <li><b>Python : </b> listes - fonctions - modules : math & plotly </li>
  <li> L'activité est écrite dans un notebook pour rendre celui-ci exécutable directement par les élèves</li>
  <li>Dans le répertoire <code>Mercator_elv</code>, se trouve :
    <ul>
      <li>Le notebook <code>Mercator_version_elv.ipynb</code></li>
      <li>Le notebook <code>Mercator_version_prof.ipynb</code></li>
    </ul>
  </li>
</ul>

:white_square_button:<b> Objectifs : </b>
<ul>
  <li>Revisiter autrement l'histoire des mathématiques et tout particulièrement la recherche de loxodromie.</li>
  <li>Mercator publia en 1569 une carte intitulée <em>Nova et Aucta Orbis Terrae Descriptio ad Usum Navigantium Emendate Accommodationata</em> ( Latin de la Renaissance pour "Représentation nouvelle et plus complète du globe terrestre correctement adaptée pour une utilisation en navigation").
    <br> Nous expliquerons comment fut construite cette carte et pourquoi la recherche d'une loxodromie est liée à la recherche de logarithme.
  </li>
  <li>Grâce à Python, cette actvité permettra aux élèves de représenter des loxodromies sur la carte de Mercator comme sur un globe Terrestre et se mettre dans la peau d'un nagigateur !
  </li>
 </ul>



:white_square_button:<b>Mercator un révolutonnaire : </b>
<ul>
  <li>Gérard Mercator (1512-1594) est un mathématicien géographe flamand qui fut l'inventeur d'une carte permettant de représenter les routes à cap constant, appelées loxodromies, en des segment de droite.
   <table>
     <tr>
       <td>Une carte de Mercator</td>
       <td>Image d'une loxodromie sur le globe terrestre</td>
     </tr>
     <tr>
       <td align="center"><img src="https://download.vikidia.org/vikidia/fr/images/thumb/5/53/Longitudes-projection_de_Mercator.jpg/350px-Longitudes-projection_de_Mercator.jpg"></td>
       <td align="center"><img src="./loxodromie.svg"></td>
     </tr>
    </table>
  </li>
  <li>La carte de Mercator possède la propriété que : 
    <ul>
      <li>les méridiens sont perpendiculaires aux parallèles </li>
      <li>les angles relevés sur la Terre sont conservés sur la carte de Mercator</li>
    </ul>
   <li> Mercator souhaita qu'un point sur la Terre repéré par sa longitude $\lambda$ et sa latitude $\varphi$ (exprimées en radian) soit représenté sur sa carte par un point M de coordonnées $\left(\lambda  , y\right)$ avec avec $y=f\left(\varphi\right)$.
Il réussit à prouver que : $$f'\left(\varphi\right)=\dfrac{1}{\cos\left(\varphi\right)},$$ pour tout $\varphi\in\left]-\dfrac{\pi}{2} , \dfrac{\pi}{2}\right[$ avec $f(0)=0$.
</br>
Ainsi pour représenter le parallèle de latitude n degrés, Mercator calculer $f\left(n\right)$, avec la méthode d'Euler, deux siècles auparavant celui-ci : $$f\left(n\right)=\dfrac{1}{\cos\left(1^{\circ}\right)}+\dfrac{1}{\cos\left(2^{\circ}\right)}+\cdots+\dfrac{1}{\cos\left(n^{\circ}\right)}.$$
</li>
</ul>
