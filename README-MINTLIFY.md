# Nolano.AI Documentation (Mintlify)

This repository contains the Mintlify-based documentation for Nolano.AI.

## Getting Started

### Prerequisites

- Node.js 18+ and npm
- Mintlify CLI

### Installation

1. Install Mintlify CLI globally:
```bash
npm install -g mintlify
```

2. Install dependencies:
```bash
npm install
```

### Development

Run the development server:
```bash
npm run dev
# or
mintlify dev
```

Open [http://localhost:3000](http://localhost:3000) to view the documentation.

### Building

Build the documentation for production:
```bash
npm run build
```

## Project Structure

```
.
├── mint.json              # Mintlify configuration
├── introduction.mdx       # Homepage/Introduction
├── quickstart.mdx         # Quick start guide
├── data-preparation.mdx   # Data preparation docs
├── model-configuration.mdx # Model configuration docs
├── training.mdx           # Training configuration docs
├── evaluation.mdx         # Evaluation and inference docs
├── api-reference/         # API reference pages
│   ├── data-config.mdx
│   ├── model-config.mdx
│   ├── optimization-config.mdx
│   └── evaluation-config.mdx
├── tutorials/             # Tutorial pages
│   ├── text-models.mdx
│   ├── time-series.mdx
│   └── custom-tokenizers.mdx
└── logos/                 # Logo and favicon files
    ├── logo_docs_dark.png
    ├── logo_docs_light.png
    └── favicon-light.png
```

## Customization

### Branding
- Update colors in `mint.json` under the `colors` section
- Replace logo files in the `logos/` directory
- Modify the favicon reference in `mint.json`

### Content
- Edit `.mdx` files for content changes
- Add new pages by creating `.mdx` files and updating navigation in `mint.json`
- Customize the homepage by editing `introduction.mdx`

### Navigation
- Modify the `navigation` array in `mint.json`
- Add new groups or reorder existing ones
- Update page references when adding new content

## Deployment

This documentation can be deployed to:
- Mintlify hosting (recommended)
- Vercel
- Netlify
- Any static hosting service

For Mintlify hosting, connect your repository at [mintlify.com](https://mintlify.com).

## Contributing

1. Create a new branch for your changes
2. Edit the relevant `.mdx` files
3. Test locally with `npm run dev`
4. Submit a pull request

## Support

- Documentation: [Mintlify Docs](https://mintlify.com/docs)
- Community: [Mintlify Community](https://mintlify.com/community)
- Issues: Create an issue in this repository
