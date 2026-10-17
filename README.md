# CrewSchedule support website

Static English/Swedish support and current-beta privacy information. No build step, scripts, forms, analytics or third-party assets. Public contact: ola@omgmedia.se.

GitHub Pages: deploy `main` from `/` using the repository Pages settings. Keep this repository limited to the contents of `Site/` in the private/local app workspace. Do not publish the app repository, rosters, launch documents or test data.

Preview locally: `python3 -m http.server 8765 --directory Site` from the app workspace, or `python3 -m http.server 8765` in the standalone website checkout.

Support: `/`; privacy: `/privacy/`; Swedish: `/sv/` and `/sv/privacy/`. Relative links support both project Pages and custom-domain URLs. The custom domain is `crewschedule.omgmedia.se`; `CNAME` pins that choice. DNS must point the `crewschedule` host to `omgoransson.github.io` (no repository path). HTTPS remains pending DNS and GitHub certificate provisioning. Intended support URL: `https://crewschedule.omgmedia.se/`; privacy: `https://crewschedule.omgmedia.se/privacy/`. Do not treat these as verified live until DNS/TLS checks pass.

The pages describe current beta behavior, including the absence of complete in-app erasure. Update the policy and support instructions after erasure and phone handover are actually verified, before using the pages for the public release. Keep both languages aligned. GitHub handles hosting traffic under its own privacy statement.
