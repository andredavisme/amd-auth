# amd-auth

Unified authentication portal for all AMD platform properties.

**Live URL:** https://auth.andremauricedavis.com

## Purpose

This is the single sign-in gateway for every site in the AMD ecosystem. All protected properties redirect unauthenticated users here with a `?return=` parameter. After successful authentication, the portal redirects back to the origin.

## Supported Auth Methods
- Google OAuth
- Email + Password

## Adding a New Property

In the new site's auth guard, redirect unauthenticated users to:
```
https://auth.andremauricedavis.com/?return=https://your-site.com/protected-page
```
After login the user will be returned automatically.

## Infrastructure
- **Supabase Project:** `hhyhulqngdkwsxhymmcd` (shared across all AMD properties)
- **Hosting:** GitHub Pages → `auth.andremauricedavis.com` (Hostinger CNAME — pending DNS)
- **storageKey:** Supabase default — no override on any AMD property client
