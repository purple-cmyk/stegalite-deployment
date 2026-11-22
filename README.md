# StegaLite deployment

This repository is the complete deployment for the browser-only image encoder/decoder. The site is the root `index.html`; it has no build step, backend, API, or external dependencies.

## Deploy on Vercel

1. In Vercel, select **Add New → Project** and import `purple-cmyk/stegalite-deployment`.
2. Set the project root to the repository root. If prompted for a framework, choose **Other**.
3. Leave the build command unset and deploy.

Vercel will host `index.html` as the website. After connecting the repository, pushes to `main` can trigger new deployments automatically. No Python environment or model checkpoint is needed.

Image and message processing happens in each visitor's browser. The app uses a reversible pixel-residual technique and exports PNG; it does not run the trained neural StegaStamp model. Keep encoded images as PNG to avoid damaging the message.
