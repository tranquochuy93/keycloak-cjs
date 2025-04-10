## Problem
I try to import the package @keycloak/keycloak-admin-client@26.1.4 and it throws ERR_REQUIRE_ESM with my NestJS server application (use commonjs).

## Solution
I setup an npm package and use esbuild to bundle keycloak-nodejs-admin-client and then export the js file with its index.d.ts file.
Then I install my package and use it in my source code