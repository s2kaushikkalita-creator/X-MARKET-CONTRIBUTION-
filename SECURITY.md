## Supported Versions
| Version | Supported |
| :--- | :--- |
| v0.2 | ✅ Active |
| v0.1 | ❌ No longer supported |

## Reporting a Vulnerability
**Do not open a public issue.**

Report privately via:
1. GitHub > Security > Report a vulnerability
2. Or email: `s2kaushikkalita@gmail.com`

We respond within 48 hours.

## Security Overview of v0.2

### 1. Age Verification
- Implemented client-side 18+ gate with `localStorage: xmarket_age_verified`
- Blur overlay `backdrop-filter: blur(28px)` prevents bypass by inspection
- Under-18 users are blocked from DOM entirely
- **Limitation:** Client-side only. For main website launch, we will enforce server-side verification.

### 2. Data Submission
```js
const API_URL = "https://script.google.com/macros/s/.../exec";
fetch(API_URL, { method: 'POST', mode: 'no-cors' })
