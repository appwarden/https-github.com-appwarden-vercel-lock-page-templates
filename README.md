# Next.js lock page templates

This repository contains lock page templates that you can use for your Appwarden lock page.

In the event of a security breach, you can issue the `/quarantine lock <domain>` command in Discord to lock your website and prevent external traffic from reaching it, ensuring your users are safe while you diagnose and resolve the issue. While locked, Appwarden renders a lock page instead of your website. If you don't have a lock page, you can use one of ours below.

To learn more, refer to the [Vercel integration guide](https://appwarden.io/docs/guides/vercel-integration) or [Cloudflare integration guide](https://appwarden.io/docs/guides/cloudflare-integration)

## Templates

[`app/maintenance`](https://github.com/appwarden/vercel-lock-page-templates/tree/main/app/maintenance) - A basic lock page template

## Usage

Copy the desired template directory (e.g. `app/maintenance`) into your project's `app` directory and redeploy your project. Then, in your environment variables, set `APPWARDEN_LOCK_PAGE_SLUG` to `/maintenance`.

```typescript
export default withAppwarden({
  lockPageSlug: process.env.APPWARDEN_LOCK_PAGE_SLUG,
})
```
