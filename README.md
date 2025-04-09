# Hydrogen template: Skeleton

Hydrogen is Shopify’s stack for headless commerce. Hydrogen is designed to dovetail with [Remix](https://remix.run/), Shopify’s full stack web framework. This template contains a **minimal setup** of components, queries and tooling to get started with Hydrogen.

## Instruction 

This repo is broken because Hydrogen `2025.1.3+` uses Vite v6. This version fails to resolve `hydrogen-sanity` `worker` export during SSR and instead resolves the `browser` export causing the following error (this was not an issue in vite 5)

###  To reproduce: 

`npm i && npm run dev`

The following error should occur:

![Screenshot 2025-04-08 at 2 48 36 PM](https://github.com/user-attachments/assets/4c302010-3b2a-415c-97ad-ca2872631f42)

### Fix

Modify the hydrogen's version to the snapshot that includes the fix: 

```rm -rf package-lock.json && npm i --force @shopify/mini-oxygen@0.0.0-snapshot-20250408225709```

then run

`npm run dev` and `setServerClient` should no longer error out.

PS. DM if you need the test `.env` 
