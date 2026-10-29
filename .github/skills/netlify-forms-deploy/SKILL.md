---
name: netlify-forms-deploy
description: "Deploy this static site and verify its Netlify discovery form. Use when deploying on Netlify or troubleshooting discovery-call submissions. Trigger keywords: Netlify deploy, form detection, discovery form, missing submissions."
metadata:
  version: "0.1.0"
  category: workflow
---

# Netlify Forms Deployment

## When to use
Follow the existing manual deployment and submission verification process in README.txt. No build tool or Netlify CLI is required by this repository.

## Steps
1. Read README.txt and inspect contactForm and its submit handler in index.html. Confirm name=discovery, form-name=discovery, the bot-field honeypot, and all submitted field names remain intact.
2. Preview index.html locally. Opening it as file: tests only the interface and redirect, not delivery. A generic HTTP static server also does not implement Netlify Forms.
3. Ask the user to confirm the target Netlify project and authorize deployment before changing hosted state. Do not infer the destination from the local folder or Git credentials.
4. Deploy the directory directly containing index.html and thank-you.html using Netlify's folder deployment interface, as documented in README.txt. No build command is needed. If deploying through an existing Git integration, use that project's configured workflow instead of creating a second project.
5. In that project's Forms settings, enable form detection, then trigger a new deploy. Confirm the production deploy is published and a discovery form is registered. Checking deployed HTML for processed form attributes is a useful diagnostic, not proof of submission delivery.
6. With explicit permission, submit a clearly labeled synthetic request through the deployed browser form at <SITE_URL>. Do not reuse real customer information. Confirm redirect to thank-you.html and the corresponding entry under Forms > discovery; check Spam if absent.
7. If requested, configure notifications to <NOTIFICATION_EMAIL> in Netlify. Dashboard capture and email notification are separate checks; report which was verified.
8. For failures, inspect the browser network response to POST / and the project's deploy/form settings. Keep personal data out of diagnostic output. Never report success solely because a static page returned HTTP 200.

## Allowed tools
Built-in file reading and search; browser navigation and developer tools; read-only HTTP requests. Deployment, dashboard changes, and synthetic POST requests require approval.

## Boundaries
- **Safe:** inspect local files, preview without transmission, and inspect public deployed markup.
- **Ask-First:** deploy, alter Netlify settings or notification recipients, or submit a synthetic lead.
- **Never:** store credentials or customer submissions in the repository; claim local preview confirms delivery; change global Git authentication.

## When NOT to apply
Do not use for another hosting provider, an application backend, or a proposed build pipeline. Reassess the form integration before migrating away from Netlify.

## Provenance
README.txt sections DEPLOY ON NETLIFY, TEST, and LOCAL provide the real manual workflow. index.html defines the Netlify form contract, URL-encoded POST /, redirect, and failure handling. This skill does not invent CI or a CLI deployment command.

<!-- generated-by: poppins · do not remove (poppins-commit re-adds it) -->