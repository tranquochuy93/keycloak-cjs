## Problem
I try to import the package @keycloak/keycloak-admin-client@26.1.4 and it throws ERR_REQUIRE_ESM with my NestJS server application (use commonjs).

Github Issue: https://github.com/keycloak/keycloak-nodejs-admin-client/issues/523

## Solution
I setup an npm package and use esbuild to bundle keycloak-nodejs-admin-client and then export the js file with its index.d.ts file.
Then I install my package and use it in my source code.
esbuild takes the keycloak classes and bundles them into one single index.js file. For the types, I just created the index.d.ts file and it looks exactly as my index.ts file.

## run
### build index.js file
```bash
npm run build
```

### Test package
```bash
git init
```

Push source to your github repository. Then init package information
```bash
npm init
```

Input package name, git repository. Then link your package to global
```bash
npm link
```

Go to your test project and install this package
```bash
npm link <name-of-package-which-you-inputted-when-init-npm>
``` 

### Publish your package
```bash
npm login
```

```bash
npm publish --access public
```

