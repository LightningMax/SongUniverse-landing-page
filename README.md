# Projet à rendre pour le cours de HTML/CSS à l'Efrei

## Explication de la différence entre HTML & CSS:
HTML (Hypertext Markup Language) est une langage de balisage qui sert
à créer la structure d'une page web, alors que le css (cascading stylesheet)
sert à styliser une page web.

## Définition de la sémantique:
Les balises sémantiques sont des balises qui donnent un sens au contenu qu'elles
englobent comme header, nav et section.

## Explication de la différence entre un ID et une class:
Un id sert à donner un identifiant unique à un élement, alors que les classes sertent
à donner un identifiant à plusieurs élements. Ces deux attributs sont très important
à l'organisation du css.

## Explication de la différence entre flexbox, grid et position:
Flexbox sert à aligner des éléments en ligne ou en colonne.

Grid sert à créer des mises en page complexes en deux dimensions (lignes et colonnes).
Ce qui permet de faire les élements se comporter comme une grille.

Position sert à définir comment un élément est positionné dans la page

## Explication du fonctionnement des pseudo-class et transition:
Les pseudo-class permettent de cibler un état spécifique d’un élément.
Par exemple le `:hover` cible un élément lorsque le curseur de la souris est dessus.

Les transitions permettent de créer des animations fluides entre deux états.

## Explication des attributs des médias et de leur utilité:
Pour le contenu du type media, on a quelques attributs importants pour l'accessibilité
comme l'attribut `alt` qui sert à donner une description à une image dans le cas qu'elle
ne se charge pas dans la page.

Pour les videos et audios il y a l'attribut `controls` qui permet d'ajouter des
fonctionalités interactives comme pauser, controller le volume, etc..

## Explication du fonctionnement d’un formulaire HTML:
Les formulaires sont un des élements essentielles dans une page web car ils permettent
de envoyer des informations saisis par l'utilisateur au serveur comme son adresse email,
 mot passe, une message, etc..

## Documentation du processus pour optimiser des images et vidéos:
Pour optimiser les videos et images, j'ai utilisé le puissant compresseur de media **FFMPEG**
J'ai crée un script simple qui permet de itérer dans chaque fichier png sur le directory 
actuel et de les compresser.

## Important : il faut que FFMPEG soit installé sur votre machine

Voici le script pour les images:
```bash
for file in *.png; do
    ffmpeg -i "$file" -q:v 50 "${file%.png}.webp"
done
```
et la commande pour les videos :
`ffmpeg -i input.mp4 -c:v libvpx -c:a libvorbis output.webm`

## Explication du fonctionnement des media queries
Les media queries sertent à créer des mise en pages réponsives en fonction de l'écran
ou de la fênetre du dispositif, ça permet de créer des mise en pages différents pour
chaque dispositif comme les smartphones, pcs, tablettes etc...

## Extra:
- Cette webpage est hébergé sur github pages, voici le lien:
https://lightningmax.github.io/projet-maquette/

- J'ai essaié d'utiliser git et github de façon consise, chaque commit a une description de
ce qui a été changé.
