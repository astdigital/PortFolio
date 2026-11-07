# Portfolio

Two independent Vite + React apps in one repository.

- public/ — public portfolio website
- admin/ — private content dashboard
- Backend — Supabase project zerunayfwnvflmtihmcl (AST organisation)
- Hosting — Cloudflare Pages projects studio-ast and ast-admin

## Deploy
Public Pages root: public; build: npm run build; output: dist.
Admin Pages root: admin; build: npm run build; output: dist.
Set VITE_SUPABASE_URL=https://zerunayfwnvflmtihmcl.supabase.co and VITE_SUPABASE_PUBLISHABLE_KEY=your publishable key in both projects.

## Grant admin access
Create the owner under Supabase Authentication > Users, then run:
insert into public.admin_users(user_id) values ('AUTH-USER-UUID') on conflict do nothing;

Never expose a service-role key in browser apps. Supabase RLS protects admin writes. Contact submissions use public.contact_messages.
