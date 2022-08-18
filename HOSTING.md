# You can run different commands depending on the target

target: server (default value)

- **npx nuxi dev** - Launch the development server.
- **npx nuxi build** - Build and optimize your application with webpack for production.
- **npx nuxi start** - Start the production server (after running npx nuxi build). Use it for Node.js hosting like Heroku, Digital Ocean, etc.

target: static

- **npx nuxi dev** - Launch the development server.
- **npx nuxi generate** - Build the application (if needed), generate every route as a HTML file and statically export to dist/ directory (used for static hosting).
- **npx nuxi start** - serve the dist/ directory like your static hosting would do (Netlify, Vercel, Surge, etc), great for testing before deploying.
