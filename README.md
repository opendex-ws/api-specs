# OpenDEX API specs

Canonical YAML. Do not mix hosts or keys.

## Files

| API | File | Host | Auth |
|---|---|---|---|
| Platform REST | [`openapi/opendex.v2.openapi.yaml`](openapi/opendex.v2.openapi.yaml) | `https://api.opendex.ws` | JWT or `X-API-Key: odx_b2b_...` |
| Platform realtime | [`asyncapi/opendex.v2.asyncapi.yaml`](asyncapi/opendex.v2.asyncapi.yaml) | `wss://api.opendex.ws` | same as Platform |
| Owner REST | [`openapi/opendex.owner.openapi.yaml`](openapi/opendex.owner.openapi.yaml) | `https://portal-api.opendex.ws/v1/owner` | `X-API-Key: odx_owner_...` |

## Which spec

- **Platform** — trading, scanner, watchlists, bots. Credits-metered.
- **Owner** — your org’s users, trades, fees, CORS, custom domains. Org is on the key; never pass an org id.

Mint Owner keys in the portal: **API Keys → Owner API**. Default scopes are `users:read`, `trades:read`, `analytics:read`. Endpoint scopes are opt-in.
