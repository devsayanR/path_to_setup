# Node.js with TypeScript Setup Guide

This README file will guide you through setting up a Node.js project with TypeScript from scratch.

## Prerequisites

- [Node.js](https://nodejs.org/) installed (LTS version recommended).
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/) package manager.
- A code editor (e.g., [Visual Studio Code](https://code.visualstudio.com/)).

---

## Step 1: Initialize the Node.js Project

Run the following command to initialize a new Node.js project:

```bash
mkdir my-node-typescript-project
cd my-node-typescript-project
npm init -y
```

This will create a `package.json` file with default values.

---

## Step 2: Install TypeScript

Install TypeScript and its dependencies:

```bash
npm install typescript --save-dev
```

---

## Step 3: Configure TypeScript

Create a `tsconfig.json` file to configure TypeScript:

```bash
tsc --init
```

Modify the `tsconfig.json` file as needed. Here’s a sample configuration:

```json
{
  "compilerOptions": {
    "target": "ES6",
    "module": "commonjs",
    "strict": true,
    "esModuleInterop": true,
    "outDir": "dist",
    "rootDir": "src"
  },
  "include": ["src"],
  "exclude": ["node_modules"]
}
```

---

## Step 4: Set Up the Project Structure

Create the following directories:

```bash
mkdir src
```

Inside the `src` directory, create an `index.ts` file:

```bash
touch src/index.ts
```

Add a simple TypeScript code snippet in `src/index.ts`:

```typescript
const greet = (name: string): string => {
  return `Hello, ${name}!`;
};

console.log(greet("World"));
```

---

## Step 5: Install Node.js Types

Install the Node.js type definitions:

```bash
npm install @types/node --save-dev
```

---

## Step 6: Add a Build Script

Update the `package.json` file to include a build script:

```json
"scripts": {
  "build": "tsc",
  "start": "node dist/index.js"
}
```

---

## Step 7: Compile the TypeScript Code

Run the TypeScript compiler:

```bash
npm run build
```

This will compile the TypeScript code into JavaScript and output it in the `dist` directory.

---

## Step 8: Run the Application

Start the Node.js application:

```bash
npm start
```

You should see the output:

```bash
Hello, World!
```

---

## Optional: Add ESLint for Linting

To maintain code quality, you can add ESLint:

1. Install ESLint:

   ```bash
   npm install eslint --save-dev
   ```

2. Initialize ESLint:

   ```bash
   npx eslint --init
   ```

3. Configure ESLint for TypeScript.

---

## Optional: Add Prettier for Code Formatting

1. Install Prettier:

   ```bash
   npm install prettier --save-dev
   ```

2. Create a `.prettierrc` file:

   ```json
   {
     "semi": true,
     "singleQuote": true
   }
   ```

---

## Project is Ready!

You now have a Node.js project set up with TypeScript. Happy coding!
