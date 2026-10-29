# mazelprime

> Canonical repository identity and operational context. Keep concise and operationally focused.

## Purpose & scope
Public MazelPrime Technologies website: service information, portfolio stories, a project-readiness calculator, and discovery-call requests. This is a single static HTML/CSS/JavaScript site, not a Node application or a backend service. The working folder is named mazelprime-site; the GitHub repository is gowthambittu/mazelprime.

## Operating boundaries
- **Safe:** inspect and edit local HTML or documentation; preview pages; run read-only checks.
- **Ask-First:** add dependencies or a build system; change form providers, business claims, or contact details; submit live test leads; initialize external tooling; commit, push, or deploy.
- **Never:** embed credentials or personal submissions; delete user changes; treat a local thank-you redirect as proof of delivery; change global Git authentication to fix this personal repository.

## Key architectural flows & constraints
- Page interaction: index.html contains inline styles and scripts for navigation, service tabs, portfolio filtering, story dialogs, and scroll reveals. Preserve the IDs and data attributes consumed by those handlers.
- Readiness: index.html inputs s1-s4 feed score(), the gauge, tier copy, and attachScore. Four default values of 3 produce 12/20 immediately; the current form submits that default even without interaction. This behavior is intentional documentation of the current code, not an instruction to change it.
- Discovery request: index.html contactForm validates name/email, attaches readiness_score, and POSTs URL-encoded FormData to / through Netlify Forms. A successful response redirects to thank-you.html; failure restores the button and shows contact alternatives.
- Local preview: index.html opened with file: skips the POST and redirects directly to thank-you.html. HTTP preview on a generic static host does not provide Netlify Forms.
- Deployment: README.txt describes Netlify folder deployment, enabling form detection before redeploying, and optional notification setup. The discovery form must be registered on the deployed site.

## Conventions
<!-- sce:conventions:start -->
- Keep both HTML pages directly deployable from the repository root. No package manifest, build command, CI pipeline, linter, or automated test suite is committed.
- Follow the existing inline CSS and vanilla JavaScript; preserve embedded image data rather than reformatting large base64 lines.
- Check readiness at its minimum, default, and maximum values: 4/20, 12/20, and 20/20. Tier thresholds are 11 and 16.
- Check story dialog close behavior, keyboard navigation, responsive layout, and form success/failure states when touching their handlers.
- This single-stack site does not currently need scoped instructions. Introduce them only when distinct areas emerge.
<!-- sce:conventions:end -->

## Security constraints
- Netlify receives name, email, company, need, budget, message, and readiness_score. Do not copy real lead data into source, screenshots, logs, or specifications.
- Preserve form-name=discovery, data-netlify, the bot-field honeypot, and URL-encoded submission unless deliberately changing the provider contract. Browser validation is not a server-side security guarantee.
- No application authentication or authorization is implemented. Form access and notification recipients are managed outside this repository in Netlify.
- Google Fonts is requested externally by the HTML pages; embedded images do not make the pages fully offline-independent.

## Maintenance Matrix
<!-- sce:maintenance-matrix:start -->
_None yet - run poppins-maintenance-matrix._
<!-- sce:maintenance-matrix:end -->

## References
<!-- sce:references -->
- Deployment and manual testing: README.txt
- Site and request handler: index.html
- Confirmation page: thank-you.html
- Netlify workflow: .github/skills/netlify-forms-deploy/SKILL.md
- Spec-driven changes: openspec/README.md
- Architecture brief: docs/architecture-brief.md
- Specs: openspec/specs/

<!-- Repository metadata -->
- Repository: mazelprime
- DevHub-Application-ID: N/A - personal project, confirmed by owner.

*Last reviewed: 2026-10-29*

<!-- generated-by: poppins · do not remove (poppins-commit re-adds it) -->