# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Vue.js tutorial project for implementing IBM's Carbon Design System. It's a Vue 2.6.12 application created with Vue CLI, designed to teach developers how to use Carbon components in Vue applications.

## Essential Commands

```bash
# Development
yarn serve          # Start dev server at http://localhost:8080
yarn build          # Build for production (creates dist/ folder)

# Code Quality
yarn lint           # Run ESLint
yarn format:diff    # Check Prettier formatting differences
yarn ci-check       # Verify code formatting

# Testing
yarn test:unit      # Run Jest unit tests
```

## Architecture

### Core Structure
- **Vue Router**: Hash mode routing with two routes (/ and /about)
- **Component Structure**: 
  - Root component: `src/App.vue`
  - Page components: `src/views/` (Home.vue, About.vue)
  - Entry point: `src/main.js`
  - Router config: `src/router.js`

### Key Technologies
- **Vue 2.6.12** with Vue CLI service
- **Sass/SCSS** with node-sass for styling
- **Jest** with @vue/test-utils for unit testing
- **ESLint + Prettier** for code formatting

### Build Configuration
- Babel config uses `@vue/app` preset
- Jest config is in `package.json`
- Vue CLI handles webpack configuration internally
- About route uses lazy loading for code splitting

## Development Workflow

When implementing Carbon components:
1. Install Carbon Vue components: `yarn add @carbon/vue`
2. Import components in the files where needed
3. Follow the [Carbon Design System Vue tutorial](https://www.carbondesignsystem.com/tutorial/vue/overview)

## Testing Approach
- Unit tests go in `/tests/unit/`
- Use `@vue/test-utils` for component testing
- Run a specific test: `yarn test:unit <test-file-name>`