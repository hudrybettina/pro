# Site vitrine — Bettina Hudry-Gerez

En ligne : **https://hudrybettina.github.io/pro/**

Tout le site tient dans un seul fichier : **`index.html`**.
Pour modifier quoi que ce soit, ouvre ce fichier sur GitHub et clique sur le crayon ✏️.
Après avoir enregistré (« Commit changes »), le site se met à jour tout seul en **1 à 2 minutes**.

---

## ⚙️ Changer les tailles de texte et les espacements

**Tu n'as qu'un seul endroit à toucher.** Cherche le bloc
`PANNEAU DE RÉGLAGES` tout en haut du fichier (vers la ligne 40).

```css
--text-base: 17px;    /* Taille du texte courant (paragraphes, puces) */
--text-small: 15px;   /* Taille des précisions en italique entre parenthèses */
--text-lead: 19px;    /* Taille des phrases d'accroche */
--lh-body: 1.75;      /* Interligne : espace ENTRE les lignes d'un paragraphe */

--space-section: clamp(64px, 6vw, 96px); /* Espace vertical entre deux sections */
--space-block: 32px;  /* Espace entre deux blocs dans une section */
--space-para: 18px;   /* Espace entre deux paragraphes */
```

Change **une seule valeur** et toute la page suit automatiquement.

| Ce que tu veux | Ce que tu changes |
|---|---|
| Texte plus gros partout | `--text-base` : passe de `17px` à `18px` ou `19px` |
| Texte plus aéré (lignes plus espacées) | `--lh-body` : passe de `1.75` à `1.9` |
| Plus de blanc entre les sections | `--space-section` : remplace `96px` par `120px` |
| Paragraphes plus espacés | `--space-para` : passe de `18px` à `24px` |

> ⚠️ Garde toujours le `px` et le point-virgule `;` à la fin.

---

## 📄 Remplacer le CV ou le portfolio

Les deux PDF sont à la racine du dépôt :

- `bettina-hudry-gerez-cv.pdf`
- `bettina-hudry-gerez-portfolio.pdf`

Pour les mettre à jour : va sur GitHub → **Add file** → **Upload files**, et dépose
ton nouveau PDF **en gardant exactement le même nom de fichier**. C'est tout, les
boutons de la page pointeront automatiquement vers la nouvelle version.

> 💡 Ne remets pas d'espaces ni d'accents dans les noms de fichiers : ça casse les
> liens sur certains navigateurs. C'est pour ça qu'ils ont été renommés.

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
--bg-secondaire: #e8e4de;  /* Gris perle (fond de la section Contact) */
--accent-color: #FF5757;   /* Rouge corail des accents */
--text-main: #1c1e21;      /* Texte principal */
--text-muted: #6e747c;     /* Texte gris des précisions */
```

---

## 🔤 À propos de la police « Panforte Pro »

Les titres utilisent `Panforte Pro` **si elle est installée sur l'ordinateur du visiteur**.
Comme presque personne ne l'a, le site bascule automatiquement sur **Space Grotesk**,
qui est chargée depuis Google Fonts et s'affiche pour tout le monde.

👉 Sur ton Mac tu vois donc Panforte Pro, mais tes visiteurs voient Space Grotesk.
Si tu veux que **tout le monde** voie Panforte Pro, il faut acheter la licence web
de la police et l'héberger dans le dépôt — dis-le si tu veux qu'on le fasse.
