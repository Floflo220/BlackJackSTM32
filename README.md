# 🃏 BlackJackSTM32

Projet de jeu **Blackjack** sur microcontrôleur **STM32** avec interface utilisateur via boutons physiques (BP1) et ecran tactile.

---

## 🎮 Description du jeu

Ce projet implémente un jeu de Blackjack en version **solo** ou **multijoueur local**, affiché sur un écran (type OLED/LCD) et contrôlé par boutons. Il est programmé pour tourner sur une carte STM32 (Nucleo, Discovery, etc.).

---

## 📋 Règles du Blackjack

- Le but du jeu est de battre la **banque** en obtenant une main de **valeur plus proche de 21** sans la dépasser.
- Les cartes :
  - Chiffres = leur valeur (2 à 10)
  - Valets, Dames, Rois = 10
  - As = 1 ou 11, selon ce qui avantage le joueur
- À son tour, le joueur peut :
  - **Tirer une carte** ("Hit") → `UP`
  - **S'arrêter** ("Stand") → `STAND`
- La **banque** joue après le joueur :
  - Elle **tire jusqu'à atteindre 17 ou plus**
  - Si elle dépasse 21, elle perd
- Le joueur gagne si :
  - Il a une meilleure main que la banque sans dépasser 21
  - Ou que la banque dépasse 21

---

## 🧩 Fonctionnement du programme

Le jeu est divisé en **3 écrans successifs** :

### 1️⃣ Écran de sélection du mode de jeu
- Choix entre :
  - **Solo**
  - **Multijoueur local**
- Navigation entre les modes : `appuis sur le mode voulue`
- mode multijoueur non disponible 

### 2️⃣ Écran de mise
- Le joueur sélectionne une **mise initiale**
- Incrémenter la mise : `+ ou - sur l'ecran`
- Valider la mise et passer à la partie : `BP1`

### 3️⃣ Jeu principal
- Les cartes sont distribuées automatiquement.
- Le joueur voit sa main et celle visible de la banque.
- Actions :
  - **Tirer une carte** : `UP`
  - **Stand** (laisser la banque jouer) : `STAND`
- Résultat affiché à la fin :
  - Victoire / Défaite / Égalité

---

## 📦 Matériel nécessaire

- Carte STM32 (ex: STM32F103, STM32F4, Nucleo, etc.)
- Écran OLED/I2C ou LCD
- 1 boutons physiques :
  - `BP1` → valider
- Alimentation USB

---

## 🛠️ Compilation & flash

1. Ouvrir le projet avec **STM32CubeIDE**
2. Connecter la carte STM32
3. Compiler le projet
4. Flasher via ST-Link
5. Profiter du Blackjack embarqué 🕹️

---

## 📄 Licence

Projet open-source sous licence MIT.
