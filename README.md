# RiceMill - Angular Application

A modern Angular application with TypeScript, routing, and server-side rendering capabilities.

## Project Location

**Repository**: `E:\Source Code\rice-mill` (GitHub cloned repository)

## Project Features

- ✅ Angular with TypeScript
- ✅ Client-side routing configured
- ✅ Server-side rendering (SSR) enabled
- ✅ Modern development toolchain
- ✅ CSS styling support
- ✅ Pre-rendering capabilities

## Getting Started

### Prerequisites

- Node.js (v18 or higher)
- npm (v9 or higher)
- Angular CLI (installed globally)

### Installation

Dependencies have been installed. If you need to reinstall:

```bash
npm install
```

### Development Server

Start the development server:

```bash
ng serve
```

or

```bash
npm start
```

Navigate to `http://localhost:4200/`. The application will automatically reload when you change any of the source files.

### Build

Build the project for production:

```bash
ng build
```

or

```bash
npm run build
```

Build artifacts are stored in the `dist/rice-mill-app` directory.

### Running Tests

Execute unit tests:

```bash
ng test
```

### Linting

Run code linting:

```bash
ng lint
```

## Project Structure

```
rice-mill/
├── src/                       # Source code
│   ├── app/                  # Application components and logic
│   │   ├── app.component.ts
│   │   ├── app.component.html
│   │   ├── app.component.css
│   │   ├── app.routes.ts     # Route definitions
│   │   ├── app.config.ts     # App configuration
│   │   └── app.config.server.ts
│   ├── main.ts               # Client bootstrap
│   ├── main.server.ts        # Server bootstrap
│   ├── server.ts             # Express server configuration
│   ├── index.html            # Main HTML template
│   └── styles.css            # Global styles
├── public/                    # Static assets
│   └── favicon.ico
├── dist/                      # Build output (generated)
├── node_modules/             # Dependencies (generated)
├── angular.json              # Angular CLI configuration
├── package.json              # NPM dependencies
├── tsconfig.json             # TypeScript configuration
├── tsconfig.app.json         # App TypeScript settings
├── tsconfig.spec.json        # Test TypeScript settings
├── .editorconfig             # Editor configuration
├── .gitignore                # Git ignore rules
├── .vscode/                  # VS Code configuration
│   ├── launch.json           # Debug configuration
│   ├── tasks.json            # Build tasks
│   └── extensions.json       # Recommended extensions
└── README.md                 # This file
```

## Configuration Files

### TypeScript Configuration

- **tsconfig.json** - Main TypeScript configuration
- **tsconfig.app.json** - App-specific TypeScript settings
- **tsconfig.spec.json** - Test-specific TypeScript settings

### Routing

Application routing is configured in:
- `src/app/app.routes.ts` - Route definitions
- `src/app/app.component.ts` - Root component

### Server Configuration

Server-side rendering files:
- `src/server.ts` - Express server configuration
- `src/main.server.ts` - Server bootstrap file
- `src/app/app.config.server.ts` - Server-specific app configuration

## VS Code Integration

The project includes VS Code configuration for:

- **Debugging**: Debug Angular applications with breakpoints
- **Tasks**: Run build and serve tasks
- **Extensions**: Recommended VS Code extensions for development

### Recommended VS Code Extensions

- Angular Language Service
- TypeScript Vue Plugin (Volar)
- Prettier Code Formatter
- ESLint

## npm Scripts

Available commands from `package.json`:

- `npm start` - Start development server (`ng serve`)
- `npm run build` - Build for production (`ng build`)
- `npm test` - Run unit tests (`ng test`)
- `npm run lint` - Run linter (`ng lint`)

## Server-Side Rendering

This project includes SSR configuration. Key files:

- `src/server.ts` - Express server
- `src/main.server.ts` - Server entry point
- `src/app/app.config.server.ts` - Server app configuration

The application is pre-rendered by default during the build process.

## Documentation

- [Angular Documentation](https://angular.dev)
- [Angular CLI Documentation](https://angular.io/cli)
- [TypeScript Documentation](https://www.typescriptlang.org)

## Next Steps

1. **Review Components**: Check `src/app/app.component.ts` and templates
2. **Add Routes**: Define routes in `src/app/app.routes.ts`
3. **Create Services**: Add Angular services for data management
4. **Configure API**: Set up API endpoints for backend communication
5. **Add Styling**: Customize styles in `src/styles.css` and component-specific CSS
6. **Environment Setup**: Configure environment-specific settings

## Development Best Practices

- Use Angular components for modularity
- Implement routing for multi-page functionality
- Create services for data and API communication
- Use TypeScript strict mode
- Follow Angular style guide
- Write unit tests for components and services
- Use environment files for configuration

## Security

- Keep Angular and dependencies updated
- Run `npm audit` regularly to check for vulnerabilities
- Use environment variables for sensitive data
- Implement proper authentication and authorization

## Troubleshooting

### Port Already in Use

If port 4200 is already in use, specify a different port:

```bash
ng serve --port 4300
```

### Clear Cache

Clear Angular cache:

```bash
ng cache clean
```

or delete the `.angular/cache` directory

### Dependency Issues

Clear node_modules and reinstall:

```bash
rm -r node_modules package-lock.json
npm install
```

## Git Integration

This project is a Git repository. Common commands:

```bash
git status
git add .
git commit -m "message"
git push
git pull
```

## Support

For issues or questions:

- [Angular GitHub Issues](https://github.com/angular/angular/issues)
- [Angular Discord Community](https://discord.gg/angular)
- [Stack Overflow Angular Tag](https://stackoverflow.com/questions/tagged/angular)

---

**Project Created**: May 22, 2026  
**Angular Version**: v19+  
**Node.js Requirement**: v18+  
**Repository**: GitHub (cloned to E:\Source Code\rice-mill)
