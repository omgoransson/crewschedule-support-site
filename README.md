# CrewSchedule support website

Static English/Swedish support and current-beta privacy information. No build step, scripts, forms, analytics or third-party assets. Public contact: ola@omgmedia.se.

GitHub Pages: deploy `main` from `/` using the repository Pages settings. Keep this repository limited to the contents of `Site/` in the private/local app workspace. Do not publish the app repository, rosters, launch documents or test data.

Preview locally: `python3 -m http.server 8765 --directory Site` from the app workspace, or `python3 -m http.server 8765` in the standalone website checkout.

Support: `/`; privacy: `/privacy/`; Swedish: `/sv/` and `/sv/privacy/`. Relative links support GitHub project Pages URLs. No custom domain is configured.

The pages describe current beta behavior, including the absence of complete in-app erasure. Update the policy and support instructions after erasure and phone handover are actually verified, before using the pages for the public release. Keep both languages aligned. GitHub handles hosting traffic under its own privacy statement.
