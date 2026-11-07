# Deployment configuration

Cloudflare Pages projects are connected to this GitHub repository.

- studio-ast builds from `public/`.
- ast-admin builds from `admin/`.

Both use `main`, `npm run build`, output `dist`, and the Portfolio Supabase project's URL + publishable key.
