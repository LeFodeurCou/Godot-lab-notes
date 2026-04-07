---
titre: Mécanique de Résolution par jet de dé - TEST
type: Règles
aliases:
  - TEST
  - JET-D20
tags:
  - TEST
  - JET-D20
abréviation: []
univers: ""
date de création: 2026-03-14
date de mise à jour: 2026-03-14T19:20:00
status: Brouillon
uid: MD20-TEST
cssclass: []
modification:
---

Dans Multivers-D20, l'issue d'une **Action** entreprise par une Entité est, dans la majorité des cas, définie par le **Résultat** d'un jet de dé à vingt faces (**D20**). Il est alors question d'effectuer un **TEST**.

> [!pa]
> Bien que la mécanique de **TEST** soit simple, elle doit néanmoins être correctement assimilée.

<br />

## 📐 Règle du TEST de base

---

Lorsqu'un Joueur entreprend une Action avec son Personnage, il décrit ses intentions au Narrateur. Le Narrateur détermine ensuite si un TEST est nécessaire.

🎲 **Si un TEST est nécessaire :**

Le Joueur calcule son Score, puis lance 1D20. Le Résultat est  alors comparé au Score.

> [!calcul]
> Score = $CARAC + [MOD-DIFF]$  
> ***<sub>Ceci est un TEST de Caractéristiques</sub>***

- **✅ Réussite** : le résultat du D20 est **inférieur ou égal** au Score
- **❌ Échec** : le résultat du D20 est **supérieur** au Score

🚫 **Si un TEST n'est pas nécessaire :**

C'est une **Résolution Automatique**. Le Narrateur estime que l'Action ne présente pas d'incertitude significative : elle réussit ou échoue sans jet, selon le contexte narratif.

> [!info-n]-
> La Résolution Automatique s'applique quand l'issue ne fait aucun doute : une tâche triviale pour le Personnage, une action sans enjeu réel, ou une situation où le résultat n'a pas d'impact sur la narration. Le Narrateur reste seul juge de ce seuil.

<br />

## 🎯 Réussite et Échec Critique

---

Certains résultats du D20 produisent un effet critique, **quels que soient les Modificateurs ou le Score** du Personnage.

| 🎲 Résultat | Effet                                                             |
|:----------- |:----------------------------------------------------------------- |
| **20**      | 🎉 **Réussite Critique** — réussite automatique, le Joueur décrit |
| **1**       | 💀 **Échec Critique** — échec automatique, le Narrateur décrit    |

> [!info-j]-
> En cas de **Réussite Critique**, le joueur décrit comment son Action se déroule de manière exceptionnelle.

> [!info-n]-
> En cas d'**Échec Critique**, c'est au Narrateur de décrire les conséquences — elles doivent être significatives et cohérentes avec le contexte, sans nécessairement être fatales.

<br />

## 📋 Pour résumer

---

Le Joueur calcule son Score, puis lance **1D20** :

- **Résultat D20 ≤ Score** → ✅ Réussite
- **>Résultat D20 > Score** → ❌ Échec
- **20** → 🎉 Réussite Critique _(automatique, quels que soient les Modificateurs)_
- **1** → 💀 Échec Critique _(automatique, quels que soient les Modificateurs)_

<br />

## 🎚️ Table de Difficulté

---

Le **Modificateur de Difficulté** est l'outil principal du Narrateur pour refléter la complexité d'une Action selon le contexte, il est le seul juge du modificateur à appliquer. C'est sa variable d'ajustement universelle.

| 🎯 Difficulté      | ⚙️ Modificateur |
|:------------------ |:--------------- |
| **Très Facile**    | `+10`           |
| **Facile**         | `+5`            |
| **Normale**        | `0`             |
| **Difficile**      | `-5`            |
| **Très Difficile** | `-10`           |
| **Héroïque**       | `-15`           |

La Difficulté absorbe **tous les facteurs contextuels** :
- 🏗️ Complexité intrinsèque de la tâche
- 🌦️ Conditions environnementales (météo, luminosité, bruit...)
- 🤕 État du personnage (blessé, empoisonné, fatigué...)
- 🔧 Équipement disponible (outils de qualité, inadaptés, aucun...)
- ⏱️ Pression temporelle (combat, course-poursuite, stress...)

>[!info-n]
La difficulté est fixée avant le jet, jamais après. Elle reflète les conditions objectives de la situation : environnement, état du Personnage, complexité intrinsèque de l'Action.
>
>En règle générale, le Narrateur **annonce la difficulté au travers de la narration**. Décrire une situation de manière évocatrice — la tempête qui fait rage, la serrure rouillée et tordue, le garde imposant qui ne bronche pas — permet aux Joueurs d'anticiper l'enjeu et de prendre leurs décisions en connaissance de cause.
>
>Cette transparence narrative préserve la confiance à la table : un échec sur une difficulté annoncée est vécu comme un défi, pas comme une injustice.
>
>**Exception délibérée :** le Narrateur peut choisir de ne pas annoncer la difficulté lorsque la surprise fait partie de la narration — un piège dissimulé, une trahison, une situation dont les Personnages ignorent légitimement la dangerosité. Dans ce cas, l'opacité est un outil narratif assumé, et non un arbitrage opaque.

<br />

## 🗂️ Les différents TESTS

---

### 🛠️ TEST de Compétence

Le **TEST de Compétence** s'applique dès qu'un Personnage entreprend une Action relevant d'un domaine de d'expertise : combat, artisanat, discrétion, médecine, acrobatie, etc.

**Résolution :**

1. Le Joueur ou le Narrateur identifie la **Caractéristique** et la **Compétence** pertinentes
2. Le Joueur calcule son **Score**
3. Il lance **1D20** et compare le Résultat au Score

> [!calcul]
> Score = $CARAC + [MOD]:Compétence + [MOD]:Difficulté$

> [!ex]
> Grok veut frapper un Gobelin. Il possède une **[FOR]** de 15 et sa Compétence Bagarre lui confère un **[MOD] FOR +3**. Son Score est donc de **18**.
> 
> Le Narrateur n'impose pas de [MOD:DIFF] à cause de l'effet de surprise.
> 
> > [!calcul]
> > $15 + 3 = 18$
> 
> Grok lance 1D20 et obtient **16**. 16 ≤ 18 → ✅ Réussite.

<br />

### ⚔️ TEST d'Attaque

Le **TEST d'Attaque** s'applique lors d'un Événement d'un affrontement. L'Entité qui attaque effectue toujours son TEST en premier.

**Résolution :**

1. L'attaquant calcule son **Score** et lance **1D20**
2. **✅ Réussite** : l'attaque touche. Les dégâts s'appliquent : `Dégâts arme − Armure cible`
    - Si la cible possède une **Compétence de Défense**, elle peut réagir (voir [[08.🎲 Mécanique de Résolution par jet de dé - TEST#🛡️ TEST de Défense|TEST de Défense]])
    - Sinon, elle subit les dégâts
3. **❌ Échec** : l'attaque rate. La cible est **libre de répliquer** lors de sa prochaine Action, ou s'il possède une **Compétence de Défense**

> [!calcul]
> Score = $CARAC + [MOD]:Compétence + [MOD]:Difficulté$

> [!pa]
> L'ordre d'action est déterminé par l'**[[03.🧪 Attributs#⏱️ L'initiative - [INIT]|[INIT]]]**. L'Entité avec la plus grande Initiative agit en premier. Ce n'est qu'après l'Action de l'attaquant que la cible peut répondre, si elle en a la Compétence ou si son Initiative le lui autorise.

> [!ex]- 
> Grok attaque un Gobelin. Il rate son TEST d'Attaque. Le Gobelin, n'étant pas encore passé dans l'ordre d'Initiative, est désormais libre de répliquer s'il possède une compétence de défense ou si son initiative le lui autorise

<br />

### 🛡️ TEST de Défense

Le **TEST de Défense** n'est possible que si le défenseur possède une **Compétence de Défense** active (Maîtrise du Bouclier, Parade, Esquive, Contre-attaque, etc.).

**Résolution :**

1. L'attaque réussit son TEST d'Attaque
2. Le défenseur déclare l'usage d'une Compétence de Défense
3. Il calcule son **Score de Défense** et lance **1D20**
4. **✅ Réussite** : l'effet est défini par la Compétence utilisée _(annulation, réduction, riposte, etc.)_
5. **❌ Échec** : les dégâts s'appliquent normalement

> [!calcul] Score de Défense = $CARAC + [MOD]:Compétence de Défense + [MOD]:Difficulté$

> [!info-j]- 
> Sans Compétence de Défense, ton Personnage ne peut pas réagir à une attaque réussie. Il subit les dégâts. L'apprentissage de compétences défensives est donc un choix stratégique fort.

> [!info-n]- 
> L'effet précis d'un TEST de Défense réussi est toujours défini par la Compétence utilisée. Le Narrateur se réfère à la fiche de compétence concernée pour arbitrer les conséquences.

<br />

### 🤺 TEST d'Opposition

Le **TEST d'Opposition** est la mécanique centrale pour toutes les interactions compétitives entre Entités. Il ne se limite pas au combat : il s'applique à toute confrontation directe où deux volontés s'affrontent.

**Exemples d'usage :** combat, course-poursuite, persuasion, intimidation, tromperie, résistance mentale, bras de fer, etc.

**Résolution :**

1. Chaque participant calcule son **Score** _(CARAC + Compétence + Difficulté)_
2. Chacun lance **1D20**
3. Chacun compare son résultat à son propre Score selon les règles standard du TEST
4. Celui qui réussit son TEST l'emporte

> [!calcul] Score = $CARAC + [MOD]:Compétence + [MOD]:Difficulté$

**Cas particuliers :**

| Situation                              | Résolution                                            |
|:-------------------------------------- |:----------------------------------------------------- |
| Les deux réussissent                   | Relance : chacun relance 1D20, le plus haut l'emporte |
| Les deux échouent                      | Match nul — situation bloquée ou statu quo            |
| Un réussit, l'autre échoue             | Celui qui réussit l'emporte                           |
| Les deux font **20** (double critique) | Match nul épique — le Narrateur décrit                |
| Un fait **20**, l'autre non            | Celui qui fait 20 l'emporte _(Réussite Critique)_     |
| Un fait **1**, l'autre réussit         | Celui qui réussit l'emporte                           |
| Les deux font **1**                    | Match nul catastrophique — le Narrateur décrit        |

> [!pa]-
> Les armures, boucliers et autres protections n'influencent **pas** le TEST d'Opposition. Ils réduisent les dégâts **après** la résolution, selon les règles de combat en vigueur.

> [!info-n]-
> Le choix des Caractéristiques dépend de l'approche narrative de chaque participant. Le Narrateur valide les Caractéristiques mobilisées avant le jet, en cohérence avec la situation décrite.

> [!ex]-
> Mira tente d'intimider un garde pour lui faire baisser les yeux. Le Narrateur décide que Mira utilise **[CHA]** + Intimidation, et que le garde répond avec **[INST]** + Résistance Mentale. Les deux lancent et comparent à leur Score respectif.

<br />

### 🤝 TEST de Coopération

Le **TEST de Coopération** s'applique quand plusieurs Entités agissent ensemble sur un même objectif dans le cadre d'un [[99.📚 Lexique#Événement|Événement]]. Il ne génère **aucun bonus mécanique** : chaque participant agit de son propre chef, avec ses propres Caractéristiques et Compétences.

**Conditions :**

- Aucun adversaire ne doit s'intercaler dans la chronologie de l'[[03.🧪 Attributs#⏱️ L'initiative - [INIT]|[INIT]]] entre les participants coopérants
- Chaque participant déclare sa contribution avant les jets

**Résolution :**

1. Chaque participant déclare son Action et la Caractéristique mobilisée
2. Chacun calcule son Score et lance **1D20** de manière indépendante
3. Les résultats individuels sont interprétés séparément
4. Le Narrateur arbitre l'issue globale selon le nombre de réussites et l'intention narrative

> [!info-n]-
> La Coopération structure l'action collective sans la simplifier. Un groupe qui coopère doit rester coordonné dans l'Initiative — si un adversaire s'intercale entre deux participants, la coopération est rompue pour ce Tour.

> [!ex]-
> Grok et Mira tentent ensemble de forcer une lourde porte. Grok utilise **[FOR]** + Athlétisme, Mira utilise **[FOR]** + Athlétisme également. Chacun lance son D20. Deux réussites : la porte cède dans un fracas. Une seule réussite : elle s'entrouvre, mais résiste. Deux échecs : elle ne bouge pas.