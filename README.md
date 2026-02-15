# GitHub Release Analytics Next

[Live Demo](https://elca.is-a.dev/gh-release-stats-next/)

A serverless, client-side dashboard for analyzing GitHub release metrics. This tool provides master-detail visualization of asset downloads, release velocity, and version adoption trends without backend infrastructure.

## Key Features

- **Master-Detail Visualization:** Interactive charts tracking total release velocity with granular per-asset drill-down.
- **Client-Side Architecture:** Zero-dependency vanilla JavaScript implementation; no build steps or bundlers required.
- **API Rate Limit Handling:** Supports Personal Access Tokens (PAT) to bypass unauthenticated limits (60 req/hr to 5,000 req/hr).
- **Advanced Filtering:** Configurable Regex-based exclusion for non-binary assets (checksums, logs, source code).
- **Performance Optimization:** LocalStorage caching (1-hour TTL) and virtualized table rendering for high-cardinality repositories.
- **Responsive Layout:** Adaptive grid system with sticky table headers optimized for mobile and desktop viewports.

## Usage

1. **Target:** Enter repository in `username/repository` format (e.g., `Elcapitanoe/Komodo-Build-Prop`).
2. **Auth (Optional):** Input a GitHub PAT to increase rate limits for large repositories or private access. Tokens are stored in browser memory only.
3. **Filter:** Modify the default Regex pattern to exclude specific file types.
   - Default: `\.(txt|md|sha256|asc|sig)$`
4. **Export:** Download parsed dataset as CSV for external analysis.
