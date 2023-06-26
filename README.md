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
