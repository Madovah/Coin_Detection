# Coin_Detection
<p>Ce projet se concentre sur la création d'un système automatisé de détection et de comptage de pièces dans des images, utilisant des techniques de vision par ordinateur, avec une base de données qui représente des pièces de monnaies ( euro) photographiés avec arrière plan plus ou moins homogène.</p>

## Pour Commencer

Ces instructions vous guideront à travers l'installation et la configuration nécessaires pour exécuter le projet sur votre machine locale. Suivez ces étapes simples pour mettre en place le projet.

### Prérequis

Avant de commencer, assurez-vous d'avoir Python installé sur votre système. Ce projet a été testé avec Python 3.8, mais il devrait être compatible avec d'autres versions de Python 3. Assurez-vous également d'avoir `pip` disponible pour installer des dépendances.
Bibliotheques utilisées:
- os
- OpenCV
- numpy
- matplotlib.pyplot
- keras
  

### Installation

1. **Cloner le dépôt**

   Ouvrez un terminal et clonez le dépôt GitHub en utilisant la commande suivante :

   ```sh
   git clone https://github.com/Madovah/Coin_Detection.git
   cd coin_detection
   ```
### Exécution

Pour exécuter le programme principal, utilisez les commandes suivantes dans le terminal :

```sh
python createmodel.py #pour creer le modele
python main.py #pour tester
```


## La base de données:
<p>La base de données est composées de deux dossiers:
un ensemble d’image étiquetés de pièces de données ( train): 2 euros, 1 euros, 50 cents, 20 cents, 10 cents, 5 cents, 2 cents, 1 cents et
Un ensemble d’images multi-coins (melange) pour le test. </p>


![1c 73](https://github.com/fati1905/coin_detection/assets/81489719/845f0e95-8423-480a-b24d-bf1f807edd1d)

![image](https://github.com/fati1905/coin_detection/assets/81489719/2ee0de51-bddd-4536-938a-2090caf84f20)

![image](https://github.com/fati1905/coin_detection/assets/81489719/a4d7d8ca-252a-48b8-a63e-29a86a0209ba)

## Description du Modèle 

### Prétraitement des Images
- Conversion en system BGR pour utiliser la bibliothèque OpenCV
- Binarisation: pour préparer a et simplifier la détection de contour en les accentuant, permettre une meilleure distinction entre les pièces et l'arrière-plan (changements brusques de valeurs de pixels)
- Détection de contours avec OpenCV
-  Filtrage de contours basé sur la taille et par aire: réduire le bruit (suppression des contours inutiles), et création de masque pour isoler la région d’interet ( pièce)
-  Extraction et regroupement de contours dans une liste



### Méthode de Classification et evaluation
Nous avons choisi de faire la classification CNN: une méthode efficace pour le traitement de d’images
Mais pourquoi? : les CNN sont capable de trouver et extraire des caractéristiques pertinentes dans les données, parfois invisible pour le programmeur a l’œil nu. Cela dit, la plupart des pièces de monnaies se ressemblent dans plusieurs caractéristiques: diamètre, jeux de couleurs, symboles inscrits, etc.. c’est pour cela que nous avons opté pour cette méthode ( influencées par la contrainte de temps et charge de travail aussi), l’évaluation du modèle se fait dans le processus de l’entrainement (General accuracy and loss, validation accuracy and loss).


### Résultats et Observations
Les résultats varient en fonction des images testées, mettant en lumière certaines limitations de notre approche, telles que la difficulté à distinguer des pièces avec des caractéristiques très similaires ou des problèmes liés à l'orientation et au chevauchement des pièces. Cependant, notre modèle montre des performances prometteuses, en particulier avec des pièces de valeurs plus élevées.


<img width="410" alt="Capture d'écran 2024-04-09 174318" src="https://github.com/fati1905/coin_detection/assets/152429992/1b53c47f-7086-4829-90e9-2809e534e60d">
<img width="409" alt="Capture d'écran 2024-04-09 174427" src="https://github.com/fati1905/coin_detection/assets/152429992/e63644c5-5837-4b29-8623-47acd5934cac">
<img width="407" alt="Capture d'écran 2024-04-09 174646" src="https://github.com/fati1905/coin_detection/assets/152429992/62c68169-00a1-4ab2-8b74-91b62ddb6621">
<img width="389" alt="Capture d'écran 2024-04-09 174718" src="https://github.com/fati1905/coin_detection/assets/152429992/9a68bd2d-9cfd-4cc7-a389-0a20315bbee3">
<img width="384" alt="Capture d'écran 2024-04-09 174744" src="https://github.com/fati1905/coin_detection/assets/152429992/6806e82b-9e6e-4603-a54c-9accb2ecdfc7">


### Conclusion
Les CNN sont idéaux pour classer les pièces de monnaie car ils capturent automatiquement les traits distinctifs des images, facilitant ainsi leur identification malgré les variations, mais cela exige beaucoup de travail et de pretraitements pour obtenir des resultats optimals.

Lien vers le projet + la BDD utilisée: [coin_detection](https://drive.google.com/file/d/1lC_kEy5VVAjT6xC7fkIf1ExWpPVXJ_ia/view?usp=sharing)


## Contributeurs:
Ce projet a été réalisé grâce à la contribution des membres suivants:</p>
    <ul>
        <li><strong>Marwa RIZI</strong></li>
        <li><strong>Tilelli BEKTACHE</strong></li>
        <li><strong>Fatima BEN KADOUR</strong></li>
        <li><strong>Sabine BELAID</strong></li>
        
   </ul>

