# RiceMill Constitution
<!-- Angular-based secure and scalable application -->

## Core Principles

### I. Component-First Architecture
All UI logic MUST be encapsulated in reusable, standalone Angular components. Components must be independently testable with clear input/output contracts via `@Input()` and `@Output()` properties. Each component has single responsibility; complex UI decomposed into smaller composable units. No organizational-only components—every component must deliver measurable value.

### II. Type Safety (Strict TypeScript)
`noImplicitAny: true` and `strict: true` enabled in `tsconfig.json` (non-negotiable). No `any` types permitted without explicit justification and TSLint suppression. All data contracts defined via interfaces or types. Generic types used to ensure compile-time type checking. Template binding validates against component types.

### III. Test-Driven Development
TDD mandatory: tests written → developer approval → tests initially fail → implement → tests pass. Minimum unit test coverage 80% per component. All business logic, services, and utilities require unit tests. Integration tests cover component interaction and routing. E2E tests cover critical user journeys. Angular Testing Utilities (TestBed, fakeAsync, fixture) required.

### IV. Performance Optimization
Initial bundle size < 500KB (main bundle). Lazy loading for feature modules enforced. Change detection strategy `OnPush` used where applicable. Async pipe preferred over manual subscriptions in templates. Core Web Vitals monitored: LCP < 2.5s, FID < 100ms, CLS < 0.1. Build optimization enabled (dead code elimination, minification, compression).

### V. Security & Accessibility First
XSS prevention via Angular's built-in sanitization and DomSanitizer. CSRF protection enforced via Angular HTTPClientXsrfModule. WCAG 2.1 Level AA compliance required: semantic HTML, ARIA labels, keyboard navigation, color contrast. SSR security: no browser-only APIs in universal code. Dependency audits run on every build; critical vulnerabilities must be resolved before release.

## Code Quality Standards

**Linting & Formatting**: ESLint + Prettier enforced via pre-commit hooks. No console.log in production code. Naming conventions: PascalCase for classes/components, camelCase for functions/variables, CONSTANT_CASE for immutable values.

**Code Review Requirements**: All PRs require minimum 2 approvals. Code review focuses on: type safety, test coverage, performance impact, security implications, accessibility compliance, consistency with established patterns.

**Documentation**: JSDoc comments for public APIs. README in each feature folder explaining purpose and usage. Architecture Decision Records (ADRs) for significant technical decisions. Complex business logic includes inline comments explaining the "why", not the "what".

## Security Requirements

**XSS Prevention**: Angular sanitization enabled by default. DomSanitizer used for HTML, style, URL, and resource URL contexts. No `innerHTML` property binding without sanitization. User input validated on both client and server.

**CSRF Protection**: Angular's HTTPClientXsrfModule configured. CSRF token included in X-XSRF-TOKEN header for state-changing requests (POST, PUT, DELETE, PATCH).

**Dependency Management**: Weekly dependency audit via `npm audit`. Critical and high vulnerabilities must be patched immediately. Outdated dependencies updated quarterly. Subresource Integrity (SRI) for CDN resources if applicable.

**SSR Security**: No sensitive data embedded in pre-rendered HTML. Environment variables not leaked in server code. Server-side API calls use secure authentication. Rate limiting on server endpoints.

## Performance Standards

**Bundle Size**: Main bundle < 500KB (gzipped). Vendor bundle lazy loaded where possible. Tree-shaking enabled via Angular production build. Unused CSS purged via PurgeCSS or similar. Third-party library selection prioritizes size and performance.

**Runtime Performance**: Change detection optimized with `OnPush` strategy. Large lists use virtual scrolling (CDK Virtual Scroll). Image lazy loading enforced. Network requests debounced/throttled. Excessive DOM manipulation avoided.

**Core Web Vitals**: LCP (Largest Contentful Paint) < 2.5s. FID (First Input Delay) < 100ms. CLS (Cumulative Layout Shift) < 0.1. Monitored via Chrome DevTools and Web Vitals library. Performance budgets defined in Angular configuration.

## Accessibility Guidelines

**WCAG 2.1 Level AA**: All interactive elements keyboard accessible. ARIA labels for screen readers on custom components. Semantic HTML (use `<button>` not `<div>` for buttons). Color contrast ≥ 4.5:1 for normal text, 3:1 for large text.

**Navigation**: Focus management in modal dialogs and single-page navigation. Skip links for keyboard users. Announcements for dynamic content updates via `aria-live`. Testing with screen readers (NVDA, JAWS) required for complex UI.

**Testing**: Automated accessibility testing via axe-core. Manual testing with keyboard only. User testing with accessibility-focused participants for major features.

## SSR/Build Requirements

**Server-Side Rendering**: Universal module configured. No browser-only APIs (localStorage, window, document) in shared code; protect with `isPlatformBrowser()` checks. Prerendering for static routes where applicable. Server response time < 1s for pre-rendered pages.

**Build Process**: Angular production build enforced for releases. No source maps shipped to production. Environment-specific configurations maintained (dev, staging, prod). Build artifacts reproducible and traceable to Git commit. CI/CD pipeline validates build success before deployment.

## Governance

**Constitution Authority**: This constitution is the source of truth for development practices. All PRs, design decisions, and technical choices must align with these principles. Constitution supersedes informal guidelines.

**Code Review Compliance**: Code reviewers verify adherence to all five core principles. Violations block merging until resolved. Exceptions require explicit documentation and approval from tech lead.

**PR/Code Review Process**: All changes via pull requests (no direct main branch commits). Automated checks must pass (lint, type check, tests). Minimum 2 human approvals from CODEOWNERS. Squash-and-merge strategy to maintain clean history.

**Versioning & Release Policy**: Semantic Versioning (MAJOR.MINOR.PATCH). MAJOR for breaking API changes or architectural shifts. MINOR for new features, principle additions, or significant enhancements. PATCH for bug fixes, documentation, and non-semantic improvements. Version bumps documented in CHANGELOG.md with migration guide if applicable.

**Breaking Changes Protocol**: Breaking changes require explicit documentation in PR description. Migration guide and deprecation period (1+ minor version) provided where possible. Changelog prominently features breaking changes. Approval from tech lead mandatory before merging.

**Documentation Requirements**: Every feature includes: functional description, usage examples, API documentation, test coverage report, performance impact analysis, accessibility compliance checklist. Architecture decisions documented in ADRs.

**Deployment Approval**: Staging environment validation required before production deployment. Performance and accessibility regression tests must pass. Security audit for sensitive features. Manual smoke testing on staging. Approval from team lead or designated reviewer.

**Amendment Procedure**: Constitution amendments require consensus from core team (>50% approval). Proposed changes submitted as issues with detailed rationale. Discussion period minimum 1 week. Approved amendments trigger version bump. All team members notified of changes. Existing code aligned with amendments within 1 month unless exemption granted.

**Version**: 1.0.0 | **Ratified**: 2026-05-26 | **Last Amended**: 2026-05-26
