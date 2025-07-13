# AMISITE - AMICIF Website

## About AMICIF

**Une véritable chaîne d'amitié francophone depuis 65 ans !**

L'AMICIF est l'amicale des anciens stagiaires des Centres Internationaux Francophones (CIF) des Lions Clubs de France. This French association charity (1901) is dedicated to the promotion of French culture around the world.

Créée dans les années 1960, elle rassemble aujourd'hui un réseau de plus de 11 000 membres à travers le monde. Nommée AMICIF lors du 50e anniversaire des CIF en 2008 à Strasbourg, elle vise à faire vivre le réseau et entretenir l'amitié francophone née chaque été aux quatre coins de la France.

## About This Website

This site, **AMISITE**, is specifically designed for all ex-participants of the CIF stages - all the "anciens" that we call the **amicale des CIFs**. It serves as a digital hub for our global francophone community to stay connected and maintain the bonds of friendship forged during their time in France.

## Our Mission & Values

**Pourquoi une association aujourd'hui ?**

L'association de l'amicale des CIF a été nommée AMICIF lors du 50ème anniversaire des CIF à Strasbourg, en 2008. Son objectif est d'animer le réseau des anciens et entretenir la flamme d'amitié francophone ravivée chaque été en juillet aux quatre coins de France.

Cette association est la nôtre, anciens stagiaires aux quatre coins du monde ! Les membres fondateurs de l'association (BDA et Conseil d'Administration) ont à cœur de poursuivre les actions portées depuis toujours par l'AMICIF et la dynamique de notre belle communauté, toujours dans un esprit d'amitié francophone.

### Our Core Values:
- **Solidarité**: Favoriser l'entraide et le soutien mutuel entre les membres
- **Engagement**: Impliquer activement les membres dans la vie de l'association
- **Respect**: Promouvoir le respect des différences et des opinions de chacun

## Development Team

This website was created by **EB Creative Solutions LTD**, a digital agency specializing in innovative solutions for various industries. The company's Directors, Enzo and Bassel, are also "anciens" of the AMICIF association, bringing both technical expertise and deep understanding of our community's needs.

Enzo, Director of EBCS, leads the development with a passion for connecting our francophone network through digital innovation.

### About EB Creative Solutions

**Transform Your Healthcare Practice** - While EBCS specializes in healthcare digital transformation, their expertise extends to creating meaningful digital experiences for communities like AMICIF.

Learn more about EBCS: [https://ebcreativesolutions.com/](https://ebcreativesolutions.com/)

## Technical Details

This project is a static website built with Hugo and deployed to Firebase Hosting.

### Prerequisites

- **Hugo**: Static site generator
- **Firebase CLI**: For deployment
- **Node.js & npm**: Required for Firebase CLI

### Installation

#### 1. Install Hugo

##### macOS (using Homebrew)
```bash
brew install hugo
```

##### macOS (Direct Download)
```bash
# Download from https://github.com/gohugoio/hugo/releases
# Extract and install
tar -xvf hugo_*.tar.gz
sudo mv hugo /usr/local/bin/
chmod +x /usr/local/bin/hugo
```

##### Windows
```bash
choco install hugo -confirm
```

##### Linux
```bash
snap install hugo
```

#### 2. Install Firebase CLI
```bash
npm install -g firebase-tools
```

### Local Development

#### Run Hugo Development Server
```bash
hugo serve
```
Your site will be available at `http://localhost:1313`

#### Build for Production
```bash
hugo
```
This generates the static site in the `public/` directory.

### Firebase Configuration

The project includes a `firebase.json` configuration file:

```json
{
  "hosting": {
    "public": "public",
    "ignore": [
      "firebase.json",
      "**/.*",
      "**/node_modules/**"
    ],
    "rewrites": [
      {
        "source": "**",
        "destination": "/index.html"
      }
    ]
  }
}
```

### Deployment

#### 1. Login to Firebase
```bash
firebase login
```

#### 2. Initialize Firebase (first time only)
```bash
firebase init hosting
```

#### 3. Build and Deploy
```bash
# Build the Hugo site
hugo

# Deploy to Firebase
firebase deploy
```

### Project Structure
```
.
├── archetypes/       # Content templates
├── content/          # Your content files
├── data/            # Data files
├── layouts/         # Template files
├── public/          # Generated site (git-ignored)
├── static/          # Static files
├── themes/          # Hugo themes
├── config.toml      # Hugo configuration
└── firebase.json    # Firebase configuration
```

### Common Commands

| Command | Description |
|---------|-------------|
| `hugo new posts/my-post.md` | Create new content |
| `hugo serve` | Start development server |
| `hugo serve -D` | Include draft content |
| `hugo` | Build site for production |
| `firebase deploy` | Deploy to Firebase |
| `firebase deploy --only hosting` | Deploy only hosting |

### Troubleshooting

#### "hugo: command not found"
Hugo is not installed or not in your PATH. Follow the installation instructions above.

#### Firebase deployment issues
- Ensure you're logged in: `firebase login`
- Check that the `public` directory exists after running `hugo`
- Verify your Firebase project is correctly configured

## Features

- Responsive Ready
- Powered by Bootstrap 4
- Dedicated portfolio/member showcase pages
- Blog Support for AMICIF news and updates
- Well formatted code
- Easy Customization
- Contact forms for member communication
- Crafted specifically for the AMICIF community

## Support

For technical support or questions about this website, please contact the development team at EB Creative Solutions LTD.

For AMICIF-related inquiries, please reach out through the official association channels.

## Resources

- [Hugo Documentation](https://gohugo.io/documentation/)
- [Firebase Hosting Documentation](https://firebase.google.com/docs/hosting)
- [Hugo Themes](https://themes.gohugo.io/)
- [AMICIF Official Information](https://amicif.org)
- [EB Creative Solutions](https://ebcreativesolutions.com/)

---

*Connecting the global francophone community of CIF alumni through digital innovation.*
