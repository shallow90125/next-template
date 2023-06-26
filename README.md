## Packages

```json
{
  "dependencies": {
    "@types/node": "20.3.1",
    "@types/react": "18.2.13",
    "@types/react-dom": "18.2.6",
    "autoprefixer": "10.4.14",
    "eslint": "8.43.0",
    "eslint-config-next": "13.4.7",
    "next": "13.4.7",
    "postcss": "8.4.24",
    "react": "18.2.0",
    "react-dom": "18.2.0",
    "tailwindcss": "3.3.2",
    "typescript": "5.1.3"
  },
  "devDependencies": {
    "eslint-config-prettier": "^8.8.0",
    "prettier": "^2.8.8",
    "prettier-plugin-organize-imports": "^3.2.2",
    "prettier-plugin-tailwindcss": "^0.3.0"
  }
}
```

## Modification

### Create Next App

```bash
pnpm create next-app

√ Would you like to use TypeScript with this project? ... Yes
√ Would you like to use ESLint with this project? ... Yes
√ Would you like to use Tailwind CSS with this project? ... Yes
√ Would you like to use `src/` directory with this project? ... Yes
√ Use App Router (recommended)? ... Yes
√ Would you like to customize the default import alias? ... No
```

### Add Packages

```bash
pnpm install -D
  eslint-config-prettier
  prettier
  prettier-plugin-organize-imports
  prettier-plugin-tailwindcss
```

### Modify Files

- `.eslintrc.json`
  ```json
  {
    "extends": ["next/core-web-vitals", "prettier"]
  }
  ```

- `next.config.js`
  ```javascript
  /** @type {import('next').NextConfig} */
  const nextConfig = {
    experimental: {
      serverActions: true,
    },
  };

  module.exports = nextConfig;
  ```

- `prettier.config.js`
  ```javascript
  module.exports = {
    plugins: ["prettier-plugin-organize-imports", "prettier-plugin-tailwindcss"],
    pluginSearchDirs: false,
  };

  ```
