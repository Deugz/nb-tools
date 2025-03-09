# RSS

Pour un site hébergé sur GitHub Pages, vous ne pouvez pas utiliser PHP ou tout autre langage côté serveur, mais vous pouvez toujours créer un flux RSS en utilisant du HTML et du JavaScript pour générer le fichier XML. Voici comment vous pouvez procéder :

### 1. Créer un fichier RSS statique

#### Étape 1 : Créer un fichier `rss.xml`

Créez un fichier nommé `rss.xml` dans votre répertoire racine ou dans un dossier spécifique de votre dépôt GitHub Pages. Ajoutez le contenu XML de base à ce fichier.

Voici un exemple de structure de fichier RSS statique :

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
  <channel>
    <title>Le titre de votre site</title>
    <link>https://votresite.github.io</link>
    <description>La description de votre site</description>
    <language>fr</language>
    <pubDate>Thu, 18 Jul 2024 10:00:00 GMT</pubDate>
    <lastBuildDate>Thu, 18 Jul 2024 10:00:00 GMT</lastBuildDate>
    <generator>GitHub Pages</generator>

    <!-- Ajouter des articles ici -->
    <item>
      <title>Exemple d'article</title>
      <link>https://votresite.github.io/article-exemple</link>
      <description>La description de l'exemple d'article.</description>
      <pubDate>Thu, 18 Jul 2024 10:00:00 GMT</pubDate>
      <guid>https://votresite.github.io/article-exemple</guid>
    </item>

  </channel>
</rss>
```

#### Étape 2 : Ajouter des articles manuellement

Ajoutez vos articles dans le fichier `rss.xml`. Vous devez manuellement insérer chaque article comme indiqué ci-dessus. Voici un exemple d'article supplémentaire :

```xml
<item>
  <title>Deuxième article</title>
  <link>https://votresite.github.io/deuxieme-article</link>
  <description>La description du deuxième article.</description>
  <pubDate>Fri, 19 Jul 2024 10:00:00 GMT</pubDate>
  <guid>https://votresite.github.io/deuxieme-article</guid>
</item>
```

### 2. Automatiser la génération du RSS avec GitHub Actions

Vous pouvez utiliser GitHub Actions pour automatiser la génération de votre fichier RSS à chaque mise à jour de votre site. Cela nécessite de créer un script en JavaScript (ou un autre langage) pour générer le RSS et de configurer une action GitHub pour exécuter ce script.

#### Étape 1 : Créer le script de génération RSS

Créez un script nommé `generate-rss.js` (ou un autre nom) à la racine de votre dépôt :

```javascript
const fs = require('fs');
const path = require('path');

const articles = [
  {
    title: 'Exemple d\'article',
    link: 'https://votresite.github.io/article-exemple',
    description: 'La description de l\'exemple d\'article.',
    pubDate: new Date('2024-07-18T10:00:00Z')
  },
  {
    title: 'Deuxième article',
    link: 'https://votresite.github.io/deuxieme-article',
    description: 'La description du deuxième article.',
    pubDate: new Date('2024-07-19T10:00:00Z')
  }
  // Ajouter d'autres articles ici
];

const rss = `<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
  <channel>
    <title>Le titre de votre site</title>
    <link>https://votresite.github.io</link>
    <description>La description de votre site</description>
    <language>fr</language>
    <pubDate>${new Date().toUTCString()}</pubDate>
    <lastBuildDate>${new Date().toUTCString()}</lastBuildDate>
    <generator>GitHub Pages</generator>
    ${articles.map(article => `
    <item>
      <title>${article.title}</title>
      <link>${article.link}</link>
      <description>${article.description}</description>
      <pubDate>${article.pubDate.toUTCString()}</pubDate>
      <guid>${article.link}</guid>
    </item>`).join('')}
  </channel>
</rss>`;

fs.writeFileSync(path.join(__dirname, 'rss.xml'), rss);
```

#### Étape 2 : Configurer GitHub Actions

Créez un fichier `.github/workflows/generate-rss.yml` :

```yaml
name: Generate RSS

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout repository
      uses: actions/checkout@v2

    - name: Set up Node.js
      uses: actions/setup-node@v2
      with:
        node-version: '14'

    - name: Install dependencies
      run: npm install

    - name: Generate RSS feed
      run: node generate-rss.js

    - name: Commit and push changes
      run: |
        git config --global user.name 'github-actions[bot]'
        git config --global user.email 'github-actions[bot]@users.noreply.github.com'
        git add rss.xml
        git commit -m 'Generate RSS feed'
        git push
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

Ce workflow générera et mettra à jour le fichier `rss.xml` chaque fois que vous pousserez des modifications sur la branche principale de votre dépôt.

### 3. Ajouter un lien vers le flux RSS sur votre site

Ajoutez un lien vers le flux RSS sur votre site en HTML :

```html
<a href="https://votresite.github.io/rss.xml">Abonnez-vous à notre flux RSS</a>
```

Cette méthode vous permettra de maintenir votre flux RSS à jour avec vos articles en utilisant GitHub Pages et GitHub Actions.