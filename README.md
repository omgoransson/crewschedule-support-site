# CrewSchedule support website

Static English/Swedish product, support and current-beta privacy information. No build step, scripts, forms, analytics or third-party assets. Public contact: ola@omgmedia.se.

GitHub Pages: deploy `main` from `/` using the repository Pages settings. Keep this repository limited to the contents of `Site/` in the private/local app workspace. Do not publish the app repository, rosters, launch documents or test data.

Preview locally: `python3 -m http.server 8765 --directory Site` from the app workspace, or `python3 -m http.server 8765` in the standalone website checkout.

Product landing: `/` and `/sv/`; support: `/support/` and `/sv/support/`; privacy: `/privacy/` and `/sv/privacy/`. Relative links support both project Pages and custom-domain URLs. The custom domain is `crewschedule.omgmedia.se`; `CNAME` pins that choice. DNS must point the `crewschedule` host to `omgoransson.github.io` (no repository path). HTTPS is enforced and GitHub reports the certificate approved (verified 17 October 2026). Intended support URL: `https://crewschedule.omgmedia.se/`; privacy: `https://crewschedule.omgmedia.se/privacy/`. All four page routes and the stylesheet return HTTP 200 and match reviewed source over valid TLS at the GitHub origin. Verification used an explicit GitHub origin IP because the local resolver still cached the old Loopia answer; public DNS success was reported by the owner.

The pages describe current beta behavior, including the absence of complete in-app erasure. Update the policy and support instructions after erasure and phone handover are actually verified, before using the pages for the public release. Keep both languages aligned. GitHub handles hosting traffic under its own privacy statement.

The local iOS/iPadOS 26 guide is at `/automatic-import-ios26/` and `/sv/automatic-import-ios26/`, with ten anchors matching the app’s `path26.*` sequence. Each locale has nine expandable screenshots captured in the iPhone 17 simulator on iOS 26.5 (23F77), in light appearance, at 1206 × 2622. The English and Swedish pages remain local drafts and have not been published. The screenshots use the confirmed sender `eFlightApplication@bristowgroup.com` and subject filter `Schedule For`; they do not establish real incoming-mail or locked-device delivery. See `docs/launch/ios26-guide-captures.md` in the app workspace for the capture record and shared asset manifest. Keep those internal capture notes outside the public website repository.


## Product landing redesign — local draft, 19 October 2026

The homepages now present the app before the help content: Today/Week screenshots, original/current comparison, optional Calendar/iCloud and paired Watch, then a beta enquiry link to ola@omgmedia.se. There is no public TestFlight or App Store link for CrewSchedule yet. Support content is retained on its own routes; the automatic-import guides and privacy pages link there. `assets/landing.css` is independent of the support-page stylesheet. All fonts/assets are local; animation respects reduced motion.

The six required product images are `assets/product/{en,sv}/{today,week,detail}.png`, sourced from the ordinary app on the isolated iPhone 17 simulator. The intended example data are entirely fictional (`Design/LandingPage/demo-roster.txt` in the app workspace). All six genuine captures are included, with provenance and hashes in `assets/product/captures.json`. Both languages have been inspected on desktop and in the iPhone simulator’s Safari. Eight HTML pages and 196 local link/asset references pass validation; image alt text, dimensions and matching section anchors are checked. The original and updated fictional rosters pass the app’s real parser/import validation. This source snapshot is ready for the existing GitHub Pages deployment; no native app update is required.
