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

## Deployment

This repository is designed to be deployed to GitHub Pages or any static hosting service.

### GitHub Pages Setup

1. Push this repository to GitHub
2. Go to Settings → Pages
3. Set source to "Deploy from a branch"
4. Select the `main` branch and `/ (root)` folder
5. Configure your custom domain: `usdc.linkio.world`

### Important Notes

- The `.well-known` directory must be served at the root level
- CORS headers should allow access from any origin
- The TOML file must be served with `Content-Type: text/plain` or `application/toml`

## SEP Compliance

This anchor implements:
- **SEP-1**: Stellar TOML
- **SEP-10**: Web Authentication
- **SEP-24**: Hosted Deposit and Withdrawal

## Contact

- **Email**: support@linkio.world
- **Website**: https://linkio.world
