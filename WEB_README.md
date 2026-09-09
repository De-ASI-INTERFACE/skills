# Web Interface

This directory contains the static web interface for the Solana Skills repository, deployed on Vercel with Web Analytics enabled.

## Structure

- `public/index.html` - Main landing page showcasing all available skills
- `package.json` - Project dependencies including @vercel/analytics
- `vercel.json` - Vercel deployment configuration
- `pnpm-lock.yaml` - Lock file for consistent dependencies

## Vercel Web Analytics

The site has Vercel Web Analytics installed and configured. The analytics script is automatically injected by Vercel when deployed:

```html
<script defer src="/_vercel/insights/script.js"></script>
```

### Setup

1. **Enable Analytics on Vercel Dashboard**
   - Go to your Vercel dashboard
   - Select this project
   - Navigate to Analytics in the sidebar
   - Click "Enable" button

2. **Deploy**
   ```bash
   vercel deploy
   ```

3. **Verify Installation**
   - After deployment, visit your site
   - Open browser DevTools → Network tab
   - Look for requests to `/_vercel/insights/*`
   - View analytics data in your Vercel dashboard

## Development

### Install Dependencies
```bash
pnpm install
```

### Run Locally
```bash
pnpm dev
```

This will serve the `public` directory on a local development server.

### Build
```bash
pnpm build
```

## Deployment

The site is configured to deploy automatically on Vercel when pushed to the main branch.

### Manual Deployment
```bash
vercel deploy --prod
```

## Analytics Features

Once enabled, Vercel Web Analytics provides:
- Page views and visitor statistics
- Top pages and referrer tracking
- Browser and device analytics
- Geographic visitor distribution
- Privacy-friendly (no cookies, GDPR compliant)

## Learn More

- [Vercel Web Analytics Documentation](https://vercel.com/docs/analytics)
- [Vercel Deployment Documentation](https://vercel.com/docs)
