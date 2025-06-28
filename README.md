# Learn Vite + Express

This is a sample full-stack application demonstrating the integration of Vite (for frontend development with React) and Express (for the backend API) using TypeScript.

## Features

*   **Frontend**: React with Vite
*   **Backend**: Express.js
*   **Language**: TypeScript
*   **Development Server**: Integrated Vite development server with Express middleware for a unified development experience.
*   **Build Tool**: Vite for optimized production builds.
*   **Code Formatting**: Biome with pre-commit hooks via Husky and Lint-staged.

## Prerequisites

Before you begin, ensure you have the following installed:

*   Node.js (v18.17.0 or later recommended)
*   npm (Node Package Manager)

## Installation

1.  Clone this repository:
    ```bash
    git clone <repository-url>
    cd learn-vite-express
    ```
2.  Install the project dependencies:
    ```bash
    npm install
    ```

## Development

To start the development server:

```bash
npm run dev
```

This will start the Express server on `http://localhost:5173`. The Vite development server is integrated as middleware, providing hot module replacement (HMR) for frontend changes.

### Endpoints:

*   **Frontend Application**: Access the main React application at `http://localhost:5173/test-site`.
*   **API Endpoint**: Access the sample API at `http://localhost:5173/api/hello`.

## Building for Production

To build the frontend for production:

```bash
npm run build
```

This command will compile your React application and output the production-ready static files into the `dist/` directory.

## Running in Production

To run the application in production mode (serving the built frontend and the Express API):

```bash
npm run start
```

This will start the Express server, serving the static files from the `dist/` directory and handling API requests.

## Project Structure

```
.gitignore
.husky/
├── pre-commit
package.json
package-lock.json
README.md
server.ts             # Express backend server
src/
├── App.tsx           # Main React component
└── main.tsx          # React application entry point
tsconfig.json         # TypeScript configuration for client and server
tsconfig.node.json    # TypeScript configuration for Node.js specific files (e.g., vite.config.ts)
vite.config.ts        # Vite configuration
gemini-logs/          # Logs of interactions with Gemini CLI
```

## Code Formatting

This project uses [Biome](https://biomejs.dev/) for code formatting. A pre-commit hook is configured to automatically format `.js`, `.jsx`, `.ts`, and `.tsx` files before each commit. You don't need to run the formatter manually.
