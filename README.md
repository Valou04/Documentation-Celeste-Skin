# Créer son propre skin sur Celeste

Cette documentation concerne la création et comment organiser votre skin sur Celeste.  
Si vous ne savez pas quoi faire ou par où commencer, alors nous essayerons de répondre à votre/vos question(s) ici.

---

## SOMMAIRE

- Composition du dossier du skin  
- Everest.yaml  
- SkinModHelperConfig.yaml  
- Dossier « Dialog »  
- Dossier « Graphics »  
- Dossier « Atlases »  
- Dossier « Portraits »  
- Dossier « Gameplay »  
- Dossier « characters »  
- Configuration skin  
- Colorgrading  
- Position Frames Animations  
- Paramètres de Skin Mod Helper Plus  
- « Advanced Options »  
- Celeste NET  
- Recommandations Logiciels  

---

## Composition du dossier du skin

Votre skin doit être un fichier zip contenant ces dossiers et fichiers :

Afin d’obtenir ce fichier ZIP bien organisé, je vous conseille d’aller voir ce GitHub (créé par Kuksa) qui vous préparera un fichier ZIP pour vous avec tout ce dont vous aurez besoin pour votre skin (certaines animations peuvent manquer si vous faites un skin avec ou sans sac-à-dos, faites donc attention d’avoir tout ce qu’il vous faut !) :  

🔗 [Celeste Skinmod Template](https://kuksattu.github.io/celeste/skinmod-template)

Sur ce GitHub se trouve un choix parmi 4 types de skins :

- « No-backpack only » : qui vous fera un ZIP avec le sprite de Madeline sans backpack.  
- « Backpack only » : qui vous fera un ZIP des sprites avec backpack.  
- « Both » : qui vous fera un ZIP des sprites avec et sans backpack (qui seront séparés).  
- « Reduced Spritecount » : qui vous fera un ZIP très réduit avec le moins d’efforts à faire pour créer le skin.  

Pour les personnes débutantes, je vous conseille d’opter pour le ZIP « Reduced Spritecount », ce dernier vous permettra de gagner du temps, si vous le jugez nécessaire, vous pourrez rajouter d’autres sprites pour obtenir un rendu plus fluide.

⚠️ ATTENTION : le ZIP « Reduced Spritecount » a été enlevé par son/sa créateur/rice (il sera de retour plus tard sous de meilleures conditions, et cette documentation sera mise à jour le moment venu).  

Votre « Nickname » et le nom de votre personnage feront partie de vos dossiers pour votre skin, vous les verrez souvent entre certains dossiers (dans le cas ci-dessous Valou/Val_fox/).  
Pour mieux vous expliquer « Valou/Val_fox / » se traduit par « YourName/YourCharacter/ » et sert à éviter les conflits avec d'autres sprites du même nom mais également cela correspond au système de nommage standard utilisé par la communauté Celeste pour l’architecture des mods.

---

## Everest.yaml

Juste un fichier contenant les dépendances de votre skin.

---

## SkinModHelperConfig.yaml

- `SkinName` = le nom de votre skin  
- `Player_List` = activer si le skin est dans la liste du skin joueur/euse  
- `Silhouette_List` = activer si le skin est dans la liste du skin silhouette, aussi appelé « playback » (à activer uniquement si vous comptez en faire un)  
- `Character_ID` = nom utilisé dans vos fichiers `.xml`  
- `OtherSprite_Path` = chemin des dossiers menant au second fichier `Sprites.xml` pour les sprites supplémentaires.

---

## Dossier « Dialog »

Dans ce fichier `.txt`, vous pourrez nommer les noms de vos types de skins (normal ou playback) :

- `SkinModHelper_Player__Valou_Val_fox` = nom du skin joueur/euse  
- `SkinModHelper_Player__Valou_Val_fox_playback` = nom du skin silhouette  
- `SkinModHelper_Player__Valou_Val_fox__Description` = Description du skin (nom du créateur/rice)  
- `SkinModHelper_Grouping__Valou_Val_fox` = nom du mod de votre skin  

---

## Dossier « Graphics »

Les fichiers `.xml` :

Vous avez deux types de fichiers `.xml`, « Portraits » (contenant les informations sur les visages et boîtes de texte des différents personnages) et « Sprites » (contenant les informations sur chaque sprite de votre skin), nous verrons ces informations un peu plus en détail plus bas dans le document.

👉 **Image d’exemple d’un fichier Graphics :**  
![Graphics Example](readme_assets/graphics_xml.png)

## Dossier « Atlases »

Dans le dossier « Atlases » se trouve deux dossiers :  

- le dossier **Gameplay** où vont se trouver tous les sprites de votre skin,  
- et le dossier **Portraits** où vont se trouver les images des portraits de votre skin (vous n’êtes pas obligé(e) d’avoir des portraits pour votre skin).  

👉 **Exemple d’aperçu :**  
![Atlases Example](readme_assets/atlases_example.png)

---

## Dossier « Portraits »

Il contient un dossier **textbox** où vous aurez la boîte de dialogue de votre personnage.  

Et le second dossier correspond à celui contenant les expressions du visage de votre personnage :  

- le dossier **madeline** pour les expressions courantes de votre skin,  
- le dossier **mirror** pour les expressions de votre skin au cours du chapitre 5,  
- le dossier **phone** pour les expressions de votre skin à la fin du chapitre 2.  

👉 **Exemple d’aperçu :**  
![Portraits Example](readme_assets/portraits_example.png)

---

## Dossier « Gameplay »

Maintenant passons au dossier « Gameplay »  

Il contient un total de 3 dossiers :  

- Un dossier **objects** contenant l’animation des jumelles,  
- Un dossier **cutscenes** avec l’animation du téléphone du chapitre 2A,  
- Un dossier **characters** avec toutes les animations du skin et du playback (du jeu de base et des mods).  

👉 **Exemple d’aperçu :**  
![Gameplay Example](readme_assets/gameplay_example.png)

---

## Dossier « characters »

### Skin classique :  
👉 **Exemple d’aperçu :**  
![Characters Classic Example](readme_assets/characters_classic.png)

### Playback :  
👉 **Exemple d’aperçu :**  
![Characters Playback Example](readme_assets/characters_playback.png)

Le screen du dossier que je vais vous montrer est celui que j’ai fait moi-même, il ne sera pas déjà prêt pour vous quand vous aurez votre fichier ZIP entre vos mains.  

⚠️ ATTENTION : Quand vous téléchargerez votre fichier ZIP, vous obtiendrez un dossier avec un fichier « READ.me » vous disant ceci :

---

### Dossier du skin classique

Vous devez avoir les dossiers :  

- `ColorGrading` (qui va gérer le changement de couleur de votre dash sur votre skin),  
- `Modded` (celui n’est pas obligatoire mais il contient les sprites de différents helpers/mods),  
- `SJ2021` (celui n’est pas obligatoire et a été ajouté manuellement par mes soins, il contient des animations du niveau Paint de la Strawberry Jam),  
- `skinConfig` (qui contient deux fichiers `.cs` qui gèrent les paramètres graphiques de votre skin, nous y reviendrons plus tard),  
- `unused` (qui contient des frames non utilisées),  

Et les dossiers **tentacle** et **wakeUp** contiennent des sprites du jeu de base pour votre skin (chapitre 6 avec les tentacules de Badeline et le réveil de Madeline du chapitre 2).  

Le reste des fichiers sont les sprites du jeu de base pour votre skin, à vous de les modifier également comme bon vous semble.  

---

Avant de se plonger dans les dossiers `skinConfig` et `Colorgrading`, j’aimerais vous parler de ce fichier s’appelant **bang**.  

Sur Celeste, les cheveux de Madeline sont séparés de son corps, si vous voulez modifier la base des cheveux, alors modifiez le fichier « bang », ou alors vous pouvez directement mettre les cheveux sur le corps de base du skin (certains skins ont les cheveux directement sur le sprite, laissez-les).  
⚠️ Mais attention, si vous mettez les cheveux directement sur le sprite, ils ne réagiront pas au vent et aux mouvements directionnels.  

👉 **Exemple (sprite + bang) :**  
![Bang Example](readme_assets/bang_example.png)

## Configuration skin

Maintenant, le dossier « SkinConfig »  

Il contient deux fichiers :  

### CharacterConfig

- **SilhouetteMode** : Le sprite sera teinté de la couleur des cheveux si en « true » (c’est pour cela que les sprites du skin playback sont blancs).  
- **LowStaminaFlashColor** : Spécifie la couleur qui clignotera lorsque l'endurance du joueur/euse sera faible/épuisée.  
- **LowStaminaFlashHair** : Indique une endurance faible qui colorera les cheveux en plus du sprite.  
- **DeathParticleColor** : Spécifie la couleur des particules du skin quand ce dernier meurt.  

---

#### Mode « froid » du chapitre 8 :

- **IdleColdOptions** : Représente la probabilité que l’animation « idle » A, B ou C se joue quand il y a le mode « froid » de Core sur la map (chapitre 8) ou quand il n’y a pas de mode :  
  - 3 chances sur 9 pour avoir l’animation « idleA »  
  - 5 chances sur 9 pour avoir l’animation « idleB »  
  - 1 chance sur 9 pour avoir l’animation « idleC »  

Ces deux lignes sont là si vous souhaitez activer des animations customisées que vous pouvez supprimer (informations sur le Sprites.xml dans le dossier « Graphics »).  

---

#### Mode « chaud » du chapitre 8 :

- **IdleWarmOptions** : Représente la probabilité que l’animation « idle » A, B ou C se joue quand il y a le mode « chaud » de Core sur la map (chapitre 8) :  
  - 3 chances sur 9 pour avoir l’animation « idleA »  
  - 5 chances sur 9 pour avoir l’animation « idleB »  
  - 1 chance sur 9 pour avoir l’animation « idleC »  

- **IdleAnimationChance** : Représente la probabilité que les animations « idleA », « idleB », « idleC » soient jouées à la fin de l’animation « idle ».  

---

### HairConfig

- **HairFlash** : Active le flash blanc qui apparaît lorsque votre nombre de dashs change.  
- **HairFloatingDashCount** : Spécifie le nombre de dashs auxquels les cheveux du skin flottent (comme quand Madeline possède deux dashs).  
- **OutlineColor** : Spécifie la couleur du contour des cheveux, et non celle du sprite.  
- **BangsOffset** : Permet de changer la position du sprite « bang » skin (à faire si ce dernier dépasse la taille de 10x10).  
- **HairOffset** : Permet de changer la position des cheveux du skin (à faire si ce dernier dépasse la taille de 10x10).  
- **Dashes** : Représente le nombre de dashs du skin (« -1 » pour la plume, « 0 » pour aucun dash etc…).  
- **Color** : Modifie la couleur des cheveux et du dash (traînée visuelle) de votre skin en agissant comme un filtre (en code HEX) en fonction de votre nombre de dashs.  
- **Scale** : Modifie la taille des cheveux de votre skin (du début à la fin) en fonction de votre nombre de dashs.  
- **Length** : Modifie la longueur des cheveux de votre skin en fonction de votre nombre de dashs.  

👉 **Exemple d’aperçu d’un fichier de configuration :**  
![Skin Config Example](readme_assets/skinconfig_example.png)

---

## Colorgrading

Le colorgrading est une étape très importante dans la confection de votre skin.  

Le colorgrading est une palette de couleurs qui va remplacer les couleurs qui seront sur votre skin par les couleurs modifiées.  

👉 Exemple :  

**Colorgrading vide, sans modification**  
![Colorgrading Before](readme_assets/colorgrading_before.png)  

**Colorgrading avec modification**  
![Colorgrading After](readme_assets/colorgrading_after.png)  

**Sprite dans votre fichier ZIP**  
![Sprite ZIP](readme_assets/colorgrading_zip.png)  

**Sprite dans le jeu**  
![Sprite Ingame](readme_assets/colorgrading_ingame.png)  

Le colorgrading n’est qu’une palette sur laquelle vous posez les couleurs que vous voudrez voir à la place d’autres couleurs sur votre skin (et cela pour chaque dash).  

⚠️ Attention : Certaines animations de helpers/mods et vanilla peuvent ne pas prendre en compte le colorgrading, vous devrez donc appliquer la couleur de votre dash directement sur le sprite.

---

## Position Frames Animations

Ceci est un point assez spécifique mais je me devais de l’écrire ici, si vous cherchez à modifier la position d’un sprite précis dans une animation, sachez que vous pouvez !  

Si vous voulez par exemple changer la position de la frame 13 de l’animation « idleB », vous devez tout simplement avoir un fichier **.meta.yaml** avec le nom de votre frame (ici « idleB13.meta.yaml ») et vous y mettez simplement de combien de pixels vous voulez décaler votre sprite.  

👉 Exemple :  
![Meta Example](readme_assets/meta-frame_example.gif)

⚠️ Votre fichier « .meta.yaml » doit être dans le même dossier que le sprite concerné.  

---

## Paramètres de Skin Mod Helper Plus

- **Otherself variant**  
- **Silhouette variant**  
- **Variant**  

👉 Lien du mod :  
🔗 [Skin Mod Helper Plus](https://gamebanana.com/mods/53734)  

👉 Exemple :  
![Skin Mod Helper Plus](readme_assets/skinmodhelperplus.png)

---

## « Advanced Options »

Ces paramètres ci-dessous sont pour savoir si vous souhaitez utiliser des animations spécifiques ou alors celles par défaut (celles dans les dossiers de votre skin).  

👉 Exemple :  
![Advanced Options](readme_assets/advanced_options.png)

---

## Celeste NET

« Celeste NET » est un mod permettant de faire du multijoueur sur Celeste, vous pouvez également montrer votre skin à vos amis !  

Il vous suffira que la personne qui joue avec vous possède votre fichier ZIP afin que Celeste NET puisse reconnaître le skin et l’affiche de son côté.  

👉 Exemple :  
![Celeste NET](readme_assets/celeste_net.png)

---

## Recommandations Logiciels

Petite section, si vous ne savez pas vraiment par où commencer afin de créer votre skin, voici quelques logiciels gratuits pour faire de la création de sprites et créer d’autres choses :  

- [Paint.Net](https://www.getpaint.net/)  
- [Krita](https://krita.org/)  
- [Piskel](https://www.piskelapp.com/)  
- [GraphicsGale](https://graphicsgale.com/us/)  
