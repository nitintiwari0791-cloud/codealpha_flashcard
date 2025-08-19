
# Deployment Guide

## Local Development

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Start development server:**
   ```bash
   npm run dev
   ```

3. **Access the application:**
   - Open `http://localhost:5000` in your browser

## Production Deployment

### Option 1: Replit (Recommended)

1. Import this repository to Replit
2. The app will automatically detect configuration
3. Click the "Run" button to start

### Option 2: Vercel

1. Connect your GitHub repository to Vercel
2. Vercel will automatically detect the build settings
3. Deploy with one click

### Option 3: Netlify

1. Connect your GitHub repository to Netlify
2. Set build command: `npm run build`
3. Set publish directory: `dist`
4. Deploy

### Option 4: Heroku

1. Create a new Heroku app
2. Connect your GitHub repository
3. Enable automatic deploys
4. The app will use the provided `Procfile`

## Environment Variables

For production deployment, you may need to set:

- `NODE_ENV=production`
- `PORT=5000` (or your preferred port)

## Build Process

The build process will:
1. Compile TypeScript files
2. Bundle the client-side React application
3. Optimize assets for production
4. Create a `dist` folder with production-ready files

## Health Check

The application includes a health check endpoint at `/api/health` that returns the server status.

## Performance Tips

- Enable gzip compression on your server
- Use a CDN for static assets
- Monitor memory usage for the in-memory storage
- Consider implementing database persistence for production use
