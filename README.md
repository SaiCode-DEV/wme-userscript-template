# WME React Userscript Template

A modern template for creating Waze Map Editor (WME) userscripts using TypeScript, React, and Rollup.

## Features

- React + TypeScript support
- Rollup for efficient bundling
- WME SDK type definitions included
- Source maps support
- Automatic userscript header generation
- ESLint and Prettier configuration

## Getting Started

### Prerequisites

- Node.js (v18 or higher recommended)
- npm or yarn
- Tampermonkey or similar userscript manager

### Setup

1. Create a new repository using this template
2. Clone your repository:
   ```bash
   git clone <your-repo-url>
   cd <your-repo-name>
   ```
3. Install dependencies:
   ```bash
   npm install
   ```

### Configuration

1. Edit `package.json` to set your script details:
   ```json
   {
     "name": "your-script-name",
     "author": "your-name",
     "displayName": "Your Script Display Name", // optional
     "shortDisplayName": "Short Name", // optional
     "version": "1.0.0",
     "description": "Your script description"
   }
   ```

2. Create your React components in the `src` directory
   - `App.tsx` is your main component
   - Use the `asScriptTab` HOC to create WME tabs
   - Import WME types from `wme-sdk-typings`

### Development

1. Write your script code starting with `src/App.tsx`
2. Build the script:
   ```bash
   npm run build
   ```
3. Find the compiled script in `dist/`:
   - `your-script-name.user.js` - readable version
   - `your-script-name.min.user.js` - minified version

### Using WME SDK

The template includes TypeScript definitions for the WME SDK. More information here:

[Waze Map Editor JavaScript SDK](https://web-assets.waze.com/wme_sdk_docs/production/latest/index.html)

### Project Structure

```
├── src/
│   ├── index.tsx       # Entry point
│   ├── App.tsx         # Main component
├── rollup.config.ts    # Rollup configuration
└── package.json        # Project configuration
```

## Building for Production

Run the build command to create production-ready scripts:

```bash
npm run build
```

The compiled userscripts will be available in the `dist` directory.

## License

This template is MIT licensed. See the LICENSE file for details.
