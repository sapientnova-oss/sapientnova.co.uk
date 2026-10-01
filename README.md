# sapientnova.co.uk

Official informational website for SapientNova, an early-stage, owner-operated technology venture. It also provides public information, privacy disclosures and terms for the SapientNova Outreach testing application.

## Static structure

- `index.html` — homepage, areas being explored, Outreach overview and contact.
- `privacy/index.html` — privacy policy and intended Google Gmail send authorization.
- `terms/index.html` — short website and application terms.
- `assets/styles.css` — responsive shared styles using system fonts.
- `assets/favicon.svg` — original star mark.
- `.nojekyll` — serve these files without Jekyll processing.

No JavaScript, framework, package manager, build step, analytics, tracking scripts, forms or application credentials are required. Core content works without JavaScript.

## Local preview

Serve this directory with any static HTTP server. For example, if Python is available:

```sh
python -m http.server 8000 --bind 127.0.0.1
```

Visit `http://127.0.0.1:8000/`, `/privacy` and `/terms`. A directory-based static server redirects `/privacy` to `/privacy/`, then serves `privacy/index.html`. Use an HTTP preview to check this routing; opening HTML directly is not a routing test.

## Intended GitHub Pages deployment

After the owner approves activation, use **Settings → Pages → Build and deployment → Deploy from a branch → main → /(root)**. This repository needs no custom Actions workflow. Until a custom domain is configured, the expected project-site URL is `https://sapientnova-oss.github.io/sapientnova.co.uk/`.

Relative page and asset links support both the project-site subdirectory and an apex-domain deployment. Canonical metadata targets the intended custom domain, `https://sapientnova.co.uk`. `/privacy` is served through the directory route, with `/privacy/` as its canonical form.

**The repository files do not activate Pages or configure a domain.** No `CNAME` is included. Custom-domain settings, domain verification, DNS and HTTPS setup require a separate owner-authorized action. Do not treat the target URLs as live until deployment and routing have been checked.

## Google OAuth boundaries

The intended application is **SapientNova Outreach**, currently in testing for owner use. The intended permission is `https://www.googleapis.com/auth/gmail.send`. The website neither authenticates Google Accounts nor sends email.

The privacy policy describes intended use and principles. Before enabling the integration, the owner must verify actual data flows, token storage, access controls, retention and deletion against the policy and Google's requirements. The website is not evidence of OAuth verification or operational compliance.

Current Google policies require a public homepage with app functionality, privacy and terms links on a verified owned domain for production applications. Gmail send is a sensitive scope; Google Workspace Limited Use disclosures apply to data from sensitive scopes. Production eligibility and any verification or exception must be assessed separately before changing the app's testing status.

Never add credentials, tokens, private messages, customer information or internal business files to this public repository.

## Official references

- [GitHub Pages publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [GitHub Pages custom domains](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)
- [Google OAuth 2.0 policies](https://developers.google.com/identity/protocols/oauth2/policies)
- [Gmail API scopes](https://developers.google.com/workspace/gmail/api/auth/scopes)
- [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy)
- [Google Workspace user data and developer policy](https://developers.google.com/workspace/workspace-api-user-data-developer-policy)
- [Managing Google Account access](https://support.google.com/accounts/answer/13533235)

References reviewed on 1 October 2026. Recheck current requirements before deployment or changes to the application.
