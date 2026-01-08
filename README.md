# LINK USDC Anchor - Stellar TOML

This repository hosts the Stellar TOML file for LINK's USDC anchor service.

## Service Information

- **Organization**: LINK
- **Asset**: USDC (Circle USD Coin)
- **Network**: Stellar Mainnet
- **Anchor Type**: SEP-24 (Hosted Deposit/Withdrawal)

## TOML File

The Stellar TOML file is accessible at:
```
https://usdc.linkio.world/.well-known/stellar.toml
```

**Note:** When accessing the TOML file directly in a browser, it will download rather than display in the browser. This is the expected behavior per the Stellar SEP-1 specification, as TOML files are meant to be machine-readable. For a human-readable view, visit:
```
https://usdc.linkio.world/toml-viewer.html
```

## Deployment

This repository is designed to be deployed to GitHub Pages with special handling for the `.well-known` directory.

### GitHub Pages Setup

1. Push this repository to GitHub
2. Go to Settings → Pages
3. Set source to "GitHub Actions"
4. Ensure your custom domain is configured: `usdc.linkio.world`

### Important Files for GitHub Pages

This repository includes several special files to ensure proper functionality on GitHub Pages:

- `_config.yml`: Tells GitHub Pages to include the `.well-known` directory
- `.nojekyll`: Prevents Jekyll from ignoring files that start with underscores or dots
- `.github/workflows/deploy-pages.yml`: GitHub Action to properly deploy the site
- `stellar.toml`: Duplicate of the TOML file at the root level for fallback access
- `_headers`: Configures proper CORS and content type headers

### Troubleshooting Access Issues

If the `.well-known/stellar.toml` path returns a 404 error:

1. Use the alternative URL: `https://usdc.linkio.world/stellar.toml`
2. Check that the GitHub Action has run successfully
3. Verify that the `.nojekyll` file exists in the deployed site
4. Ensure all files in this repository are pushed to GitHub

### CORS and Content Type Headers

For proper functionality, the TOML file must be served with:
- `Content-Type: text/plain` or `application/toml`
- `Access-Control-Allow-Origin: *` for CORS support

## SEP Compliance

This anchor implements:
- **SEP-1**: Stellar TOML
- **SEP-10**: Web Authentication
- **SEP-24**: Hosted Deposit and Withdrawal

## Contact

- **Email**: support@linkio.world
- **Website**: https://linkio.world
