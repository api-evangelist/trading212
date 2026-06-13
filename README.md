# Trading 212

Trading 212 is a commission-free investing platform with a REST API for accessing portfolio data, managing orders, viewing positions, retrieving instruments, and accessing account information.

## API

The Trading 212 Public API (currently in beta) is available to users with a General Invest Account or Stocks and Shares ISA Account. It provides programmatic access to:

- **Account Data** — account summary, cash availability, and investment metrics
- **Orders** — place and cancel market, limit, stop, and stop-limit equity orders
- **Positions** — retrieve all open positions with P&L details
- **Instruments** — browse tradable instruments and exchange working schedules
- **Pies** — create and manage diversified Pie portfolios
- **History** — access historical orders, dividends, transactions, and CSV exports

### Environments

| Environment | Base URL |
|---|---|
| Live (real money) | `https://live.trading212.com/api/v0` |
| Paper trading (demo) | `https://demo.trading212.com/api/v0` |

### Authentication

HTTP Basic Authentication using an API Key and API Secret generated in the Trading 212 app under Settings > API (Beta). The `Authorization` header is constructed by Base64-encoding `API_KEY:API_SECRET` and prepending `Basic `.

### Rate Limits

Rate limits are applied per account and vary by endpoint. The system uses a burst-allowance model. Every response includes `x-ratelimit-*` headers. See [rate-limits/rate-limits.yml](rate-limits/rate-limits.yml) for a full breakdown.

## Resources

- [API Documentation](https://docs.trading212.com/api)
- [Authentication](https://docs.trading212.com/api/section/authentication)
- [Rate Limiting](https://docs.trading212.com/api/section/rate-limiting/how-it-works)
- [API Terms and Conditions](https://www.trading212.com/legal-documentation/API-Terms_EN.pdf)
- [Help Centre — API Key](https://helpcentre.trading212.com/hc/en-us/articles/14584770928157-Trading-212-API-key)
- [Community Forum](https://community.trading212.com/)

## Profile

- [apis.yml](apis.yml)
- [plans/plans.yml](plans/plans.yml)
- [rate-limits/rate-limits.yml](rate-limits/rate-limits.yml)
- [finops/finops.yml](finops/finops.yml)
