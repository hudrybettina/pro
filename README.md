# Site vitrine de Bettina Hudry-Gerez

En ligne : **https://hudrybettina.github.io/pro/**

Tout le site tient dans un seul fichier : **`index.html`**.
Pour modifier quoi que ce soit, ouvre ce fichier sur GitHub et clique sur le crayon ✏️.
Après avoir enregistré (« Commit changes »), le site se met à jour tout seul en **1 à 2 minutes**.

---

## ⚙️ Changer les tailles de texte et les espacements

**Tu n'as qu'un seul endroit à toucher.** Cherche le bloc
`PANNEAU DE RÉGLAGES` tout en haut du fichier (vers la ligne 40).

```css
--text-base: 17px;    /* Texte courant (paragraphes, puces) */
--text-small: 15px;   /* Précisions en italique entre parenthèses */
--lh-body: 1.75;      /* Interligne : espace ENTRE les lignes d'un paragraphe */

--text-lead: clamp(19px, 1.9vw, 23px);       /* « Préparer l'avenir sans… » */
--text-subtitle: clamp(21px, 2.2vw, 27px);   /* « Mes valeurs », « Ma boussole » */
--text-label: clamp(17px, 1.7vw, 19px);      /* « Contexte d'intervention : », etc. */
--text-value-name: clamp(17px, 1.7vw, 20px); /* Aventure, Altruisme, Sagesse… */

--space-section: clamp(52px, 4.5vw, 80px); /* Espace vertical entre deux sections */
--space-block: 32px;  /* Espace entre deux blocs dans une section */
--space-para: 18px;   /* Espace entre deux paragraphes */
```

Change **une seule valeur** et toute la page suit automatiquement.

| Ce que tu veux | Ce que tu changes |
|---|---|
| Texte plus gros partout | `--text-base` : passe de `17px` à `18px` ou `19px` |
| Texte plus aéré (lignes plus espacées) | `--lh-body` : passe de `1.75` à `1.9` |
| Plus de blanc entre les sections | `--space-section` : remplace `80px` par `100px` |
| Paragraphes plus espacés | `--space-para` : passe de `18px` à `24px` |
| « Mes valeurs » encore plus grand | `--text-subtitle` : remplace `27px` par `30px` |

> ⚠️ Garde toujours le `px` et le point-virgule `;` à la fin.

### À quoi sert `clamp(...)` ?

`clamp(21px, 2.2vw, 27px)` veut dire : **jamais plus petit que 21px, jamais plus
grand que 27px**, et entre les deux la taille s'adapte à la largeur de l'écran.
C'est ce qui fait que le texte reste lisible sur téléphone sans être énorme sur
grand écran. Pour agrandir, change surtout **le dernier chiffre**.

---

## ↔️ Le texte justifié

Seule la section **« Qui suis-je ? »** a le texte justifié (aligné des deux
côtés), parce que la photo à droite crée une colonne nette. Partout ailleurs le
texte est aligné à gauche, ce qui évite les grands trous entre les mots.

Pour changer ça sur une section, cherche `text-align: left;` dans la balise
`<div class="container"...>` de la section et remplace par
`text-align: justify; text-justify: inter-word;` (ou l'inverse).

---

## 📄 Remplacer le CV ou le portfolio

Les deux PDF sont à la racine du dépôt :

- `bettina-hudry-gerez-cv.pdf`
- `bettina-hudry-gerez-portfolio.pdf`

**Oui, tu peux les remplacer quand tu veux.** Une seule règle : **garde exactement
le même nom de fichier**.

La méthode la plus simple, en 3 étapes :

1. Renomme ton nouveau fichier sur ton ordinateur pour qu'il s'appelle exactement
   `bettina-hudry-gerez-cv.pdf` (ou `bettina-hudry-gerez-portfolio.pdf`).
2. Sur GitHub : **Add file** → **Upload files**, et dépose-le.
3. Clique sur **Commit changes**.

GitHub voit que le nom existe déjà et remplace l'ancienne version. **Pas besoin de
supprimer d'abord.** Le site se met à jour en 1 à 2 minutes, et les boutons
pointent automatiquement vers la nouvelle version : tu n'as aucun code à toucher.

> ⚠️ Si tu déposes un fichier avec un **nom différent**, les boutons continueront
> de chercher l'ancien nom et afficheront une page d'erreur. Dans ce cas il faut
> aussi modifier les liens dans `index.html` (ils apparaissent 2 fois chacun :
> une fois dans « Qui suis-je ? », une fois dans « Engager la réflexion »).

> 💡 Ne remets jamais d'espaces ni d'accents dans les noms de fichiers : ça casse
> les liens sur certains navigateurs. C'est pour ça qu'ils ont été renommés.

---

## 🔗 Les onglets du menu

Chaque onglet du menu est relié à une section par une « ancre ».
Le lien `href="#offre"` renvoie vers la section `id="offre"`.

**Les deux mots doivent être identiques**, sinon l'onglet ne fait rien quand on clique.

| Onglet du menu | Section correspondante |
|---|---|
| Vision | `id="vision"` |
| Offre | `id="offre"` |
| Expériences | `id="projets"` |
| Qui suis-je ? | `id="qui-suis-je"` |
| Contact | `id="contact"` |

---

## ✍️ Modifier un texte

Cherche simplement la phrase dans `index.html` (avec `Ctrl+F` / `Cmd+F`) et réécris-la.
Ne touche pas à ce qui est entre chevrons `< >`.

Pour mettre un mot **en rouge corail et en gras** :

```html
<span class="highlight-corail">le mot à mettre en valeur</span>
```

---

## 🎨 Changer les couleurs

Toujours dans le même bloc en haut du fichier :

```css
--bg-principal: #faf6f0;   /* Fond crème */
--bg-secondaire: #e8e4de;  /* Gris perle (bandeau chiffres + section Contact) */
--accent-color: #FF5757;   /* Rouge corail des accents */
--surface: #fffcf8;        /* Blanc chaud : fond des cartes */
--text-main: #1c1e21;      /* Texte principal */
--text-muted: #6e747c;     /* Texte gris des précisions */
```

---

## ✨ Les animations

La page comporte quatre effets, tous écrits à la main (aucune bibliothèque
externe, donc rien à mettre à jour, rien qui puisse casser) :

| Effet | Ce que ça fait |
|---|---|
| Barre de progression | Fine ligne corail en haut qui suit l'avancement dans la page |
| Barre de navigation compacte | La baseline s'efface au défilement pour gagner de la place |
| Onglet actif | L'onglet de la section en cours se souligne en corail |
| Apparition en fondu | Les blocs montent doucement quand ils entrent à l'écran |

**Pour ajouter l'effet d'apparition à un nouveau bloc**, ajoute-lui la classe
`reveal` :

```html
<div class="reveal"> ... </div>
```

**Pour retirer un effet d'apparition**, enlève simplement le mot `reveal` de
la balise.

> 🔒 Sécurité : si le JavaScript ne fonctionne pas chez un visiteur, tout le
> contenu s'affiche normalement, rien ne peut rester invisible. Et si la
> personne a activé « réduire les animations » dans les réglages de son
> système, les effets sont automatiquement désactivés.

---

## 📊 Modifier les chiffres clés

Le bandeau gris sous le titre d'accueil. Cherche `stats-band` dans le fichier :

```html
<div class="stat">
    <div class="stat-value">13 ans</div>
    <div class="stat-label">en conseil en innovation et stratégie…</div>
</div>
```

Tu peux en ajouter ou en retirer : la grille se réorganise toute seule.

---

## 🔤 À propos de la police « Panforte Pro »

Les titres utilisent `Panforte Pro` **si elle est installée sur l'ordinateur du visiteur**.
Comme presque personne ne l'a, le site bascule automatiquement sur **Space Grotesk**,
qui est chargée depuis Google Fonts et s'affiche pour tout le monde.

👉 Sur ton Mac tu vois donc Panforte Pro, mais tes visiteurs voient Space Grotesk.
Si tu veux que **tout le monde** voie Panforte Pro, il faut acheter la licence web
de la police et l'héberger dans le dépôt. Dis-le si tu veux qu'on le fasse.
