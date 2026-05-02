# FlowX React App

FlowX is a frontend-only Vite, React, and TypeScript application with a local
JSON mock API for development and role-based UI flows.

## Features

- Vite-powered React 19 application
- TypeScript project setup
- Reusable UI components in `src/components/ui`
- FlowX application screens under `src/flowx`
- Mock API data in `db.json`
- Local JSON server for frontend development
- Deployment notes for Vercel and other static hosts

## Requirements

- Node.js 20 or newer recommended
- npm

## Getting Started

Install dependencies:

```bash
npm install
```

Create a local environment file from the example:

```bash
cp .env.example .env
```

Start the frontend:

```bash
npm run dev
```

In a second terminal, start the mock API:

```bash
npm run server
```

The mock API runs on port `5000`.

## Available Scripts

```bash
npm run dev        # Start the Vite development server
npm run server     # Start json-server using db.json
npm run build      # Build for production
npm run build:dev  # Build in development mode
npm run preview    # Preview the production build locally
npm run lint       # Run ESLint
npm run format     # Format files with Prettier
```

## Project Structure

```text
src/
  app/          App-level routing and guards
  components/   Shared UI components
  core/         Core providers, hooks, and services
  flowx/        FlowX screens and workspace UI
  services/     API clients and service wrappers
```

Other useful files:

- `db.json` - mock API data
- `.env.example` - environment variable template
- `vite.config.ts` - Vite configuration
- `vercel.json` - Vercel routing configuration

## Documentation

- `ARCHITECTURE.md`
- `FLOWX_README.md`
- `MOCK_API_READY_README.md`
- `DEPLOYMENT_VERCEL.md`
- `README_DEPLOYMENT.md`

## Deployment

Build the app before deploying:

```bash
npm run build
```

The production output is generated in `dist/`. See `DEPLOYMENT_VERCEL.md` and
`README_DEPLOYMENT.md` for deployment-specific notes.

## License

No license has been specified for this project.
