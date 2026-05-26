<!-- Use this file to provide workspace-specific custom instructions to Copilot. For more details, visit https://code.visualstudio.com/docs/copilot/copilot-customization#_use-a-githubcopilotinstructionsmd-file -->

## RiceMill - Angular Application Project

### Project Overview

A modern Angular application with TypeScript, routing, and server-side rendering capabilities.

### Project Location

**Repository**: `E:\Source Code\rice-mill` (GitHub cloned repository)

### Technology Stack

- **Framework**: Angular v19+
- **Language**: TypeScript
- **Styling**: CSS
- **Routing**: Angular Routing (enabled)
- **Server**: Node.js / Express
- **SSR**: Enabled
- **Package Manager**: npm

### Setup Status

- [x] Project scaffolded with Angular CLI
- [x] Routing configured
- [x] Server-side rendering enabled
- [x] Dependencies installed
- [x] Build verified
- [x] Project moved to GitHub cloned repository

### Key Directories

- `/src` - Application source code
- `/src/app` - Angular components and routing
- `/public` - Static assets
- `/dist` - Build output
- `/.vscode` - VS Code configuration

### Common Commands

- `npm start` or `ng serve` - Start development server (http://localhost:4200)
- `npm run build` or `ng build` - Production build
- `npm test` or `ng test` - Run unit tests
- `npm run lint` or `ng lint` - Run linter

### Configuration Files

- `angular.json` - Angular CLI configuration
- `tsconfig.json` - TypeScript configuration
- `package.json` - NPM dependencies
- `.vscode/tasks.json` - VS Code build tasks
- `.vscode/launch.json` - VS Code debug configuration

### Development Workflow

1. Start development server: `npm start`
2. Open http://localhost:4200 in browser
3. Edit files in `/src/app`
4. Changes auto-reload in browser
5. Commit and push to GitHub

### Architecture Notes

- Root component: `src/app/app.component.ts`
- Routes defined in: `src/app/app.routes.ts`
- Server configuration: `src/server.ts`
- Main entry point (client): `src/main.ts`
- Main entry point (server): `src/main.server.ts`

### Documentation

- README.md - Comprehensive project documentation
- [Angular Official Docs](https://angular.dev)
- [Angular CLI Reference](https://angular.io/cli)

<!-- SPECKIT START -->
For additional context about technologies to be used, project structure,
shell commands, and other important information, read the current plan
<!-- SPECKIT END -->
