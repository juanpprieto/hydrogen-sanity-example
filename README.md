# Hydrogen template: Skeleton

Hydrogen is Shopify’s stack for headless commerce. Hydrogen is designed to dovetail with [Remix](https://remix.run/), Shopify’s full stack web framework. This template contains a **minimal setup** of components, queries and tooling to get started with Hydrogen.

## Instruction 

This repo is broken, becausde Hydrogen 2025.1.3+ runs under Vite v6. This version fails to resolve `hydrogen-sanity` `worker` export during SSR and instead resolves the `browser` export causing the following error:

![Screenshot 2025-04-08 at 2 48 36 PM](https://github.com/user-attachments/assets/4c302010-3b2a-415c-97ad-ca2872631f42)

### Fix

Modify the hydrogen's version to the snapshot that includes the fix: 

```npm i --force @shopify/hydrogen@0.0.0-snapshot-20250408212515```

then run

`npm run dev` and `setServerClient` should no longer error.

DM  me if you need a `.env` 
