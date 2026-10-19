# CrewSchedule support website

Static product, support, privacy and setup pages in all seven app languages: English, Swedish, Norwegian Bokmål, Danish, Finnish, Dutch and German. Committed HTML is served directly, with no runtime scripts, forms, analytics or third-party assets. Public contact: ola@omgmedia.se.

GitHub Pages: deploy `main` from `/` using the repository Pages settings. Keep this repository limited to the contents of `Site/` in the private/local app workspace. Do not publish the app repository, rosters, launch documents or test data.

Preview locally: `python3 -m http.server 8765 --directory Site` from the app workspace, or `python3 -m http.server 8765` in the standalone website checkout.

Product landing: `/` and `/sv/`; support: `/support/` and `/sv/support/`; privacy: `/privacy/` and `/sv/privacy/`. Relative links support both project Pages and custom-domain URLs. The custom domain is `crewschedule.omgmedia.se`; `CNAME` pins that choice. DNS must point the `crewschedule` host to `omgoransson.github.io` (no repository path). HTTPS is enforced and GitHub reports the certificate approved (verified 17 October 2026). Intended support URL: `https://crewschedule.omgmedia.se/`; privacy: `https://crewschedule.omgmedia.se/privacy/`. All four page routes and the stylesheet return HTTP 200 and match reviewed source over valid TLS at the GitHub origin. Verification used an explicit GitHub origin IP because the local resolver still cached the old Loopia answer; public DNS success was reported by the owner.

The pages describe current beta behavior, including the absence of complete in-app erasure. Update the policy and support instructions after erasure and phone handover are actually verified, before using the pages for the public release. Keep both languages aligned. GitHub handles hosting traffic under its own privacy statement.

The iOS/iPadOS 26 guide is at `/automatic-import-ios26/` and `/sv/automatic-import-ios26/`, with ten anchors matching the app’s `path26.*` sequence. Each locale has nine expandable screenshots captured in the iPhone 17 simulator on iOS 26.5 (23F77), in light appearance, at 1206 × 2622. The English and Swedish guide pages are included in the 19 October 2026 Pages publication. The screenshots use the confirmed sender `eFlightApplication@bristowgroup.com` and subject filter `Schedule For`; they do not establish real incoming-mail or locked-device delivery. See `docs/launch/ios26-guide-captures.md` in the app workspace for the capture record and shared asset manifest. Keep those internal capture notes outside the public website repository.


## Product landing redesign — 19 October 2026

The homepages now present the app before the help content: Today/Week screenshots, original/current comparison, optional Calendar/iCloud and paired Watch, then a beta enquiry link to ola@omgmedia.se. There is no public TestFlight or App Store link for CrewSchedule yet. Support content is retained on its own routes; the automatic-import guides and privacy pages link there. `assets/landing.css` is independent of the support-page stylesheet. All fonts/assets are local; animation respects reduced motion.

The six required product images are `assets/product/{en,sv}/{today,week,detail}.png`, sourced from the ordinary app on the isolated iPhone 17 simulator. The intended example data are entirely fictional (`Design/LandingPage/demo-roster.txt` in the app workspace). All six genuine captures are included, with provenance and hashes in `assets/product/captures.json`. Both languages have been inspected on desktop and in the iPhone simulator’s Safari. Eight HTML pages and 196 local link/asset references pass validation; image alt text, dimensions and matching section anchors are checked. The original and updated fictional rosters pass the app’s real parser/import validation. Published to the existing GitHub Pages repository on 19 October 2026; no native app update is required. The homepages are the product presentation, and the support articles remain at their dedicated routes.


## Seven-language website — 19 October 2026

English uses the root paths. Swedish, Norwegian Bokmål, Danish, Finnish, Dutch and German use `/sv/`, `/nb/`, `/da/`, `/fi/`, `/nl/` and `/de/`. Each language has a product landing page, `support/`, `privacy/` and `automatic-import-ios26/`: 28 pages in total. The native language menu keeps the visitor on the matching page. All pages include alternate-language and canonical metadata. No automatic language detection, tracking cookie or JavaScript is added.

The existing Swedish captures are retained; the five new languages use the genuine English screenshots with an explicit English-interface caption. Names such as CrewSchedule Import, the sender filter and Schedule For stay unchanged. Public contact remains ola@omgmedia.se. Translation does not change the privacy policy's beta limitations or data flows.

In the app workspace, `Site/translations/en.json` owns the 200 source messages for the five new language catalogs; English and Swedish HTML remain the authored page templates. Regenerate using `python3 scripts/build-site-localizations.py`, then run `python3 scripts/check-site-localizations.py`. The check compares the seven website languages with the app catalog, checks all 28 page routes/sections, 875 local references, language-preserving navigation, image descriptions and source literals. Repeated generation must be identical. The public website repository needs no build step; update translations in the app workspace and publish only Site.
