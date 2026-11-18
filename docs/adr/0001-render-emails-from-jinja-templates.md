# Render order emails from Jinja templates

- **Status:** Accepted
- **Date:** 2026-04-02
- **Applies to:** boutique-emailservice
- **Deciders:** @arch-beagel-test/checkout

## Context

Order confirmations are HTML.

## Decision

emailservice renders `templates/confirmation.html` with Jinja and is the only service that sends mail.

## Consequences

Other services ask emailservice; none opens an SMTP connection.
