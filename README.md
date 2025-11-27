# Descriptif complet du mini-projet : Filtre RC + Amplificateur + Analyse du signal

Ce mini-projet consiste à créer un petit système électronique permettant d’étudier comment un signal alternatif se comporte lorsqu’il traverse un filtre passe-bas RC, puis éventuellement un amplificateur.
Il utilise uniquement les outils disponibles sur Tinkercad : un générateur de fonction, un oscilloscope, un multimètre, une alimentation continue, et quelques composants analogiques simples.

L’objectif est d’apprendre à manipuler et analyser des signaux électriques réels, de comprendre le rôle d’un filtre RC et d’un petit étage amplificateur, et d’utiliser les instruments virtuels comme dans un vrai laboratoire.

## 🔶 1. Compréhension générale du projet

Le générateur de fonction produit un signal alternatif (souvent une sinusoïde).
Ce signal est envoyé dans un filtre RC, constitué d’une résistance et d’un condensateur.
Le rôle du filtre est de laisser passer les basses fréquences et d’atténuer les hautes.

Après le filtrage, on a la possibilité d’ajouter un petit amplificateur à transistor NPN pour observer comment il influence le signal : gain, chute de tension, distorsion éventuelle, etc.

L’oscilloscope permet d’afficher simultanément le signal d’entrée et celui de sortie pour voir les différences.
Le multimètre, lui, sert à mesurer les tensions moyennes, les valeurs efficaces ou la fréquence.

## 🔶 2. Objectif du système à construire

Le système final doit :

recevoir un signal sinusoïdal ou carré depuis le générateur,

faire passer ce signal à travers la résistance puis le condensateur (filtre RC),

fournir un signal filtré,

éventuellement envoyer ce signal filtré dans un transistor pour amplification,

afficher sur l’oscilloscope le signal avant filtrage et après filtrage (ou après amplification),

permettre des mesures avec le multimètre,

être alimenté par une source DC pour la partie amplificateur.

## 🔶 3. Composants utilisés

Tous disponibles dans Tinkercad :

générateur de fonction pour produire le signal,

oscilloscope pour visualiser les signaux,

multimètre pour mesurer tensions et fréquences,

alimentation DC,

résistance de 10 kΩ,

condensateur de 0,1 µF,

transistor NPN de type 2N2222 (optionnel pour amplification),

résistances associées au transistor : 1 kΩ pour la base, 4,7 kΩ pour le collecteur,

une breadboard et des fils de connexion.

## 🔶 4. Principe du filtre passe-bas

Le signal du générateur traverse d'abord la résistance.
Après la résistance, on trouve le point de sortie du filtre.
Depuis ce point, un condensateur est relié à la masse.

Le comportement du filtre dépend de la fréquence du signal :

les basses fréquences passent presque sans modification,

les hautes fréquences sont envoyées vers la masse par le condensateur, ce qui diminue fortement leur amplitude.

La fréquence limite du filtre (appelée fréquence de coupure) est d’environ 159 Hz avec R = 10 kΩ et C = 0,1 µF.

Ainsi, un signal de 50 Hz passe presque entièrement, tandis qu’un signal de 1 kHz est clairement atténué.

## 🔶 5. Amplificateur optionnel

Après le filtrage, on peut ajouter un petit amplificateur à transistor NPN.
Ce montage permet :

d’augmenter légèrement l’amplitude du signal,

de visualiser la relation entre le signal d’entrée et celui en sortie du transistor,

d’étudier la possible déformation du signal,

de comprendre le rôle de la base, du collecteur, et de l’émetteur.

Le transistor est monté en émetteur suiveur :
l’amplitude peut augmenter un peu, mais surtout le signal devient plus robuste.

## 🔶 6. Étapes de réalisation
### Étape 1 – Connexion du générateur

Le générateur envoie son signal vers la résistance de 10 kΩ.
Sa borne négative est reliée à la masse du circuit.

### Étape 2 – Construction du filtre RC

La sortie de la résistance rejoint un point commun.
À ce point, on branche le condensateur dont l’autre borne va à la masse.
Ce point commun représente la sortie du filtre RC.

### Étape 3 – Visualisation à l’oscilloscope

L’oscilloscope mesure deux signaux :

le signal avant la résistance,

le signal après le filtre.

On observe l’atténuation des hautes fréquences, le déphasage, et la forme du signal.

### Étape 4 – Ajout du transistor (facultatif)

Le signal filtré est envoyé dans la base du transistor via une résistance.
Le collecteur est alimenté par une tension continue à travers une résistance.
L’émetteur donne la sortie amplifiée.
On observe ensuite cette sortie sur l’oscilloscope.

### Étape 5 – Mesures avec le multimètre

Le multimètre permet de mesurer la tension DC moyenne, la valeur efficace AC, ou la fréquence, selon les fonctions disponibles.

## 🔶 7. Résultats que l’on peut observer

À basse fréquence, le signal d’entrée et celui de sortie sont presque identiques.

À haute fréquence, le signal de sortie est réduit, plus arrondi et déphasé.

Le transistor peut ajouter une légère augmentation de tension ou une distorsion si le niveau dépasse ses limites.

Le déphasage devient très visible en fonction de la fréquence.

Le comportement global du filtre devient très clair sur l’oscilloscope.

## 🔶 8. Conclusion générale

Ce mini-projet est un excellent exercice pour comprendre l’électronique analogique de base.
Il permet de :

comprendre comment fonctionne un filtre passe-bas,

analyser un signal en temps réel avec un oscilloscope,

utiliser un générateur de fonction et une alimentation DC,

visualiser les effets d’un transistor en tant qu'amplificateur simple,

se familiariser avec les mesures électriques essentielles.

Il constitue une introduction idéale avant d’aborder des circuits plus complexes.
