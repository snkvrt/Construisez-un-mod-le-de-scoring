# Construisez un modèle de scoring

Vous êtes Data Scientist au sein d'une société financière, nommée "Prêt à dépenser",  qui propose des crédits à la consommation pour des personnes ayant peu ou pas d'historique de prêt.

Logo Prêt à dépenser
 

Pour accorder un crédit à la consommation, l’entreprise souhaite mettre en œuvre un outil de “scoring crédit” qui calcule la probabilité qu’un client le rembourse ou non, puis classifie la demande : crédit accordé ou refusé. Elle souhaite donc développer un algorithme de classification pour aider à décider si un prêt peut être accordé à un client.

Les chargés de relation client seront les utilisateurs de l’outil de scoring. Puisqu’ils s’adressent aux clients, ils ont besoin que votre modèle soit facilement interprétable. Les chargés de relation souhaitent, en plus, disposer d’une mesure de l’importance des variables qui ont poussé le modèle à donner cette probabilité à un client.

Pour réaliser ce modèle, Michaël, votre manager, vous a fourni le jeu de données suivant qui contient :

un historique de prêts ;
un historique d’informations financières ;
des informations sur le comportement des emprunteurs (si l’emprunteur a fait défaut ou pas).
Après une première réunion de brief, Michaël vous a envoyé ce mail de récap :

 

De : Michaël

Envoyé : hier 17:14

À : vous 

Objet : Récap. Algo de scoring

Hello,

Merci pour notre meeting. Je souhaitais le compléter en te donnant quelques ressources :

Pour aller plus vite sur la préparation des données, tu peux utiliser un kernel Kaggle. Par contre, fais attention à ce qu’il soit adapté à ton besoin. Essaie notamment de construire au moins trois nouvelles variables à partir des variables existantes qui te semblent pertinentes pour améliorer le pouvoir prédictif du modèle. Essaye aussi de t’approprier le kernel au maximum en l’adaptant pour le projet.
On a évoqué le fait que ton modèle doit être interprétable par les équipes qui vont l’utiliser. N’hésite pas à consulter ce site et ce Github à ce sujet. Pense à expliciter en quelques lignes la méthode d’importance des variables que tu retiendras.
Le modèle sera à présenter aux équipes, fais donc en sorte que ta présentation soit compréhensible par tous, et que ton Jupyter soit bien documenté. Pour les slides, je te suggère ce plan :
Compréhension de la problématique métier
Description du jeu de données
Transformation du jeu de données (nettoyage et feature engineering)
Comparaison et synthèse des résultats pour les modèles utilisés
Interprétabilité du modèle
Conclusion
 

Bon courage !

Michaël

  

Livrables 
Un Jupyter Notebook présentant les différentes parties de votre travail de modélisation.
Ce notebook doit pouvoir être utilisé par une autre personne, comme Michaël par exemple.  Sa présentation et sa structuration doivent donc être soignées afin que le notebook puisse être pris en main par une personne autre que vous, sans que vous ayez à la former à son utilisation
Une présentation (PowerPoint ou une alternative) :
Ce livrable vous servira à présenter votre approche méthodologique de modélisation de la problématique de scoring lors de la soutenance orale devant Michaël.
Pour faciliter votre passage devant le jury, déposez sur la plateforme, dans un dossier zip nommé “Titre_du_projet_nom_prénom”, votre livrable nommé comme suit : Nom_Prénom_n° du livrable_nom du livrable_date de démarrage du projet. Cela donnera : 

Nom_Prénom_1_notebook_mmaaaa
Nom_Prénom_2_presentation_mmaaaa
Par exemple, votre premier livrable peut être nommé comme suit : Dupont_Jean_1_notebook_012022.

Soutenance
Pendant la soutenance, l’évaluateur jouera le rôle de Michaël, à qui vous présentez votre travail. Une attention particulière sera accordée à votre discours. Michaël veut en effet s’assurer que votre présentation est au bon niveau pour qu’elle soit comprise par une audience non technique. 

Présentation (20 minutes) 
Rappel de la problématique, présentation du jeu de données et analyse exploratoire (5 minutes)
Présentation de votre approche méthodologique et de la synthèse des résultats (15 minutes) 
Discussion (5 minutes)
L’évaluateur, jouant le rôle de Michaël, vous challengera sur vos choix.
Débriefing (5 minutes)
À la fin de la soutenance, l'évaluateur arrêtera de jouer le rôle de Michaël pour vous permettre de débriefer ensemble.
Votre présentation devrait durer 20 minutes (+/- 5 minutes).  Puisque le respect des durées des présentations est important en milieu professionnel, les présentations en dessous de 15 minutes ou au-dessus de 25 minutes peuvent être refusées. 

Référentiel d'évaluation
Compétences

Critères d'évaluation

Transformer les variables pertinentes pour un modèle supervisé classique (= feature engineering)

Le feature engineering est complet si :

❒ une analyse exploratoire a été conduite sur les variables initiales 

❒ les variables catégorielles ont été identifiées et transformées pour être utilisées par le modèle (ex : one hot encoding)

❒ au moins trois nouvelles variables ont été construites à partir des variables initiales


Le feature engineering est pertinent si :

❒ les variables ont été normalisées (si besoin selon l’algorithme choisi)

❒ la performance du modèle est améliorée par l’ajout des nouvelles variables construites


Le feature engineering est présentable si :

❒ une représentation graphique de l’importance des variables a été réalisée

❒ la méthode de détermination de l’importance des variables a été explicitée et le principe décrit en 5-10 lignes

Entraîner un modèle supervisé classique qui répond aux attentes des métiers

L’entraînement d’un modèle supervisé classique répondant à la problématique métier est réalisé si :

❒ la variable cible a été identifiée

❒  la séparation du jeu de données en jeu d’entraînement et en jeu de test a été réalisée et il n’y a pas de fuite d’information entre les deux jeux de données (ex : la normalisation a bien été réalisée uniquement sur le jeu d’entraînement indépendamment du jeu de données de test)

❒ La démarche de modélisation prend en compte le déséquilibre des classes (par exemple via un oversampling de type SMOTE ou via l’utilisation de “class_weight”)

❒ Le modèle optimisé prend en compte la différence de coût métier entre un faux négatif et un faux positif"


L’entraînement d’un modèle supervisé classique répondant à la problématique métier est pertinente si :

❒ Plusieurs modèles ont été essayés (au minimum un linéaire et un non linéaire)

❒ Une méthode globale et une méthode locale de mesure de l’importance des variables ont été mises en oeuvre et explicitée.

Evaluer les performances d’un modèle supervisé classique

L’évaluation des performances d’un modèle supervisé classique est complète si :

❒ une métrique spécifiquement adaptée au cas et qui pénalise la non détection a été définie par l'étudiant et utilisé pour évaluer la performance de ses modèles

❒ la performance d’un modèle de référence a été évaluée et sert de comparaison pour évaluer la performance des modèles plus complexes (exemple de modèle de référence : le modèle prédisant qu’aucun client ne fait défaut)


L’évaluation des performances d’un modèle supervisé classique est pertinente si :

❒ la validation croisée est utilisée pour comparer les performances des modèles sur la métrique d’évaluation


L’évaluation des performances d’un modèle supervisé classique est présentable si :

❒ une synthèse comparative des différents modèles a été rédigée (ex : tableau comparatif des résultats pour les différents modèles)

❒ le choix de la métrique d’évaluation a été explicité 

Adapter les hyperparamètres d’un modèle d’apprentissage supervisé classique afin de l’améliorer

L’optimisation des hyperparamètres d’un modèle supervisé est complète si :

❒ les hyperparamètres des modèles utilisés ont été identifiés

❒ une méthode d’optimisation des hyperparamètres a été mise en oeuvre (ex : grid search) 


L’optimisation des hyperparamètres d’un modèle supervisé est pertinente si :

❒ une validation croisée a été mise en oeuvre pour optimiser les hyperparamètres

Compétences évaluées
Evaluer les performances d’un modèle supervisé classique
Transformer les variables pertinentes pour un modèle supervisé classique
Adapter les hyperparamètres d’un modèle d’apprentissage supervisé classique
Entraîner un modèle supervisé classique qui répond aux attentes des métiers
