# Modern Astro Web Template

A modern, responsive website template built with Astro.js, featuring a pure CSS theme switcher and reusable components.

## Features

- 🎨 Pure CSS Theme Switcher (Light/Dark)
- 📱 Fully Responsive Design
- 🧩 Reusable Components
- 🎯 SEO-friendly
- 🚀 Fast Performance
- 📦 Zero JavaScript 
- 🎭 Beautiful Transitions
- 🔧 Easy Configuration

## Components

- Header with Navigation
- Footer with Social Links
- Card System
- Card Collections
- Theme Switcher
- Welcome Section

## Prerequisites

### POSIX-compatible Systems (Linux, macOS, BSD)
- Node.js 18 or higher
- npm or yarn
- git

### Windows
1. Install Git:
   - Download Git from [git-scm.com](https://git-scm.com/download/windows)
   - Run the installer, using default settings
   - Verify installation: Open Command Prompt and type `git --version`

2. Install Node.js and npm:
   - Download Node.js LTS from [nodejs.org](https://nodejs.org/)
   - Run the installer, ensure "npm package manager" is selected
   - Verify installation: Open Command Prompt and type `node --version` and `npm --version`

3. (Optional) Install Yarn:
   - Open Command Prompt and run: `npm install -g yarn`
   - Verify installation: `yarn --version`

## Installation

### POSIX-compatible Systems (Linux, macOS, BSD)

1. Clone the repository:
```bash
git clone https://github.com/yourusername/webtemplate.git
cd webtemplate
```

2. Install dependencies:
```bash
# Using npm
npm install

# OR using yarn
yarn install
```

3. Start the development server:
```bash
# Using npm
npm run dev

# OR using yarn
yarn dev
```

4. Open your browser and visit `http://localhost:4321`

### Windows

1. Clone the repository:
   - Open Command Prompt
   - Navigate to your desired location: `cd C:\Projects` (create if needed)
```cmd
git clone https://github.com/yourusername/webtemplate.git
cd webtemplate
```

2. Install dependencies:
```cmd
:: Using npm
npm install

:: OR using yarn
yarn install
```

3. Start the development server:
```cmd
:: Using npm
npm run dev

:: OR using yarn
yarn dev
```

4. Open your browser and visit `http://localhost:4321`

## Configuration

Edit `src/config.ts` to customize your site:

```typescript
export const siteConfig = {
  name: "Your Site Name",
  description: "Your site description",
  author: {
    name: "Your Name",
    social: {
      twitter: "https://twitter.com/yourusername",
      discord: "your-discord-invite-code",
      // Add more social links
    }
  }
}
```

## Project Structure

```
/src
├── components/    # Reusable components
│   ├── Card.astro
│   ├── CardCollection.astro
│   ├── Footer.astro
│   ├── Header.astro
│   ├── ThemeSwitcher.astro
│   └── Welcome.astro
├── layouts/       # Layout templates
│   └── Layout.astro
├── pages/         # Routes and pages
│   └── index.astro
└── config.ts      # Site configuration
```

## Customization

### Themes

Colors are defined using CSS variables in `src/layouts/Layout.astro`:

```css
:root {
  --text-1: #333;
  --text-2: #444;
  --surface-1: #fff;
  --surface-2: #f0f0f0;
  --surface-3: #e0e0e0;
  --accent: #4a90e2;
}

:root:has(#theme-toggle:checked) {
  --text-1: #fff;
  --text-2: #ccc;
  --surface-1: #1a1a1a;
  --surface-2: #2a2a2a;
  --surface-3: #3a3a3a;
  --accent: #64b5f6;
}
```

### Adding New Pages

Create new `.astro` files in the `src/pages` directory. They will be automatically added to your site with their corresponding routes.

## Building for Production

```bash
npm run build
# or
yarn build
```

The built site will be in the `dist` directory, ready to be deployed.

## Browser Support

- Modern browsers that support CSS `:has()` selector
- Firefox ESR and above
- Chrome, Safari, Edge latest versions

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the Lesser GNU Public License v3.0. See the [LICENSE](./LICENSE.md) file for details.
