
# Hugo Site with Firebase Hosting
<h1>Hugo</h1>
<img src="https://user-images.githubusercontent.com/16266381/76162082-10850b80-6164-11ea-8b20-f30b2611f92c.png" alt="screenshot" width="100%">

Hugo is a digital agency Hugo theme for creative agencies,  freelancers, graphic designers, photographers. Can be used for any kind of corporate websites who provides digital services with many expertise such as  Design, Digital Products, Development, Campaign & Content, Employer Branding, Animation & Motion Graphics ,Packaging & Product Design, Retail & Spacial, Print & Editorial Design, Concept/Text, Information Design etc. EBCSHugo’s contact form is supported fabform.

This project is a static website built with Hugo and deployed to Firebase Hosting.

## Prerequisites

- **Hugo**: Static site generator
- **Firebase CLI**: For deployment
- **Node.js & npm**: Required for Firebase CLI

## Installation

### 1. Install Hugo

#### macOS (using Homebrew)
```bash
brew install hugo
```

#### macOS (Direct Download)
```bash
# Download from https://github.com/gohugoio/hugo/releases
# Extract and install
tar -xvf hugo_*.tar.gz
sudo mv hugo /usr/local/bin/
chmod +x /usr/local/bin/hugo
```

#### Windows
```bash
choco install hugo -confirm
```

#### Linux
```bash
snap install hugo
```

### 2. Install Firebase CLI
```bash
npm install -g firebase-tools
```

## Local Development

### Run Hugo Development Server
```bash
hugo serve
```
Your site will be available at `http://localhost:1313`

### Build for Production
```bash
hugo
```
This generates the static site in the `public/` directory.

## Firebase Configuration

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

## Deployment

### 1. Login to Firebase
```bash
firebase login
```

### 2. Initialize Firebase (first time only)
```bash
firebase init hosting
```

### 3. Build and Deploy
```bash
# Build the Hugo site
hugo

# Deploy to Firebase
firebase deploy
```

## Project Structure
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

## Common Commands

| Command | Description |
|---------|-------------|
| `hugo new posts/my-post.md` | Create new content |
| `hugo serve` | Start development server |
| `hugo serve -D` | Include draft content |
| `hugo` | Build site for production |
| `firebase deploy` | Deploy to Firebase |
| `firebase deploy --only hosting` | Deploy only hosting |

## Troubleshooting

### "hugo: command not found"
Hugo is not installed or not in your PATH. Follow the installation instructions above.

### Firebase deployment issues
- Ensure you're logged in: `firebase login`
- Check that the `public` directory exists after running `hugo`
- Verify your Firebase project is correctly configured

## Resources

- [Hugo Documentation](https://gohugo.io/documentation/)
- [Firebase Hosting Documentation](https://firebase.google.com/docs/hosting)
- [Hugo Themes](https://themes.gohugo.io/)






## Table of Contents

- [Live Demo](#live-demo)
- [Installation](#installation)
- [Main Features](#features)
- [Support](#support)
- [Licensing](#licensing)
- [Hire](#hire)

## Live Demo

Checkout the live demo [here](https://roxo-hugo.staticmania.com/)

## Installation

1. Add the repository into your Hugo Project repository as a submodule, `git submodule add git@github.com:StaticMania/roxo-hugo.git themes/roxo-hugo`.
2. Copy the `data`, `content`, `static`, `resources` & `config.toml` files from the `exampleSite` directory and paste it on you Hugo Project repository/directory. From the site home directory:

    cp -a themes/roxo-hugo/exampleSite/* .

3. Build your site with `hugo serve` and see the result at `http://localhost:1313/`.


## Features

* Responsive Ready.
* Powered by Bootstrap 4.
* Dedicated portfolio page.
* Blog Support.
* Well formatted code.
* Easy Customization.
* FabForm.io [static website form](https://fabform.io).
* Crafted for Design Agency/ portfolio

## Support

Have some question or facing any technical trouble feel free to [Contact Us](https://staticmania.com/contact/)

## Licensing

This Repository is licensed under the [MIT](https://github.com/StaticMania/roxo-hugo/blob/master/LICENSE) License

## Hire

Need help to build HUGO websites with your custom requirements. Feel free to [contact](https://staticmania.com/contact/) with us. We provide custom development service for HUGO.
