# Tirage au sort ! (La Roue de l'Infortune)

Une application web interactive et ludique permettant de réaliser des tirages au sort à l'aide d'une roue animée. Idéal pour désigner des participants, des gagnants, ou "qui va s'y coller" !

## 🌟 Fonctionnalités Principales

- **Roue Animée Personnalisée :** Une roue de la fortune générée dynamiquement avec le Canvas HTML5 en fonction du nombre de participants.
- **Gestion des Participants :** Ajoutez, modifiez ou supprimez facilement des participants via une zone de texte. La roue se met à jour instantanément.
- **Tirages Multiples :** Possibilité de choisir le nombre de gagnants à tirer au sort d'affilée.
- **Bouton d'Action Aléatoire :** Le texte du bouton de lancement change de manière amusante (ex: "QUI S'Y COLLE ?", "LA ROUE DE L'INFORTUNE", "PLOUF-PLOUF...").
- **Élimination Automatique :** Lorsqu'un participant est tiré au sort, il est automatiquement retiré de la liste pour les tirages suivants.
- **Effets Visuels :** Animation de rotation fluide de la roue et jet de confettis (grâce à `canvas-confetti`) à l'annonce du gagnant.
- **Fenêtre Modale de Résultat :** Affichage clair et festif du ou des gagnants à la fin du tirage.

## 🛠️ Technologies Utilisées

- **HTML5 :** Structure de l'application et utilisation de l'élément `<canvas>`.
- **CSS3 :** Mise en page avec Flexbox, design moderne (mode sombre) et animations (`transition` sur le canvas).
- **JavaScript (Vanilla) :** Logique de l'application, manipulation du DOM, calculs des angles et des rotations pour la roue.
- **Librairie Externe :** [canvas-confetti](https://www.npmjs.com/package/canvas-confetti) pour l'effet de célébration.

## 🚀 Comment utiliser l'application

1. Ouvrez le fichier `index.html` dans n'importe quel navigateur web moderne. Aucune installation ni serveur n'est requis.
2. **Liste des participants :** Dans la section de droite, modifiez la liste dans la zone de texte (un nom par ligne).
3. Cliquez sur **"Mettre à jour la roue"** si vous avez modifié la liste manuellement.
4. **Nombre de gagnants :** Sélectionnez le nombre de personnes à tirer au sort à l'aide du menu déroulant.
5. **Lancer la roue :** Cliquez sur le bouton d'action principal (le texte varie) pour lancer l'animation.
6. Attendez que la roue s'arrête. Une modale s'ouvrira pour afficher le(s) gagnant(s) sous une pluie de confettis !
7. Fermez la modale pour continuer. Les gagnants auront été retirés de la liste.

## 📁 Architecture du projet

Le projet tient en un seul fichier `index.html` qui contient :
- Le markup HTML pour la structure (Roue + Panneau de contrôle).
- Le style CSS intégré dans la balise `<style>`.
- La logique JavaScript dans la balise `<script>`.

## ⚙️ Contexte et Historique (Notes de version)
Le code actuel correspond à la **version 4.8.1**.
- Correction d'un bug majeur (le 'g' fantôme) présent dans la version 4.7 au niveau de la mise à jour de la roue.
- Amélioration de la fonction `populateDrawCountSelect` pour gérer dynamiquement le nombre maximum de tirages possibles par rapport au nombre de participants restants.
