# ContextGuard

**Privacy that understands context.** ContextGuard is a prototype concept for a privacy gateway between people and AI tools. It checks who is asking, what information is being shared, and why before allowing, masking, redacting, pseudonymizing, or blocking a request.

This repository contains a static landing page for the Devhack Syndicate project at NMAMIT, developed for **PS 2.2 — Context-Aware Data Privacy**.

## Website

- Live site: https://nroboai.github.io/contextguard-site/
- Source: [index.html](index.html)

## What the concept covers

- **Sensitive data detection:** names, phone numbers, Aadhaar, PAN, email, and card details.
- **Context-aware decisions:** consider requester role, document type, nearby text, and intent.
- **Policy actions:** allow, mask, redact, pseudonymize, or block, with a reason and audit record.
- **Response scanning:** check AI output for exposed data and hidden exfiltration instructions.
- **Harassment safeguards:** block requests that sexualize, expose, or profile real, named people, including deepfake and doxxing requests.

The page includes a small simulated role-based example. It is an illustrative frontend demo; it does not connect to an AI model or implement the privacy gateway.

## Run locally

No build step or dependencies are required. Open `index.html` in a browser, or serve the repository directory with any static file server, for example:

```bash
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Prototype goals

The figures shown on the site (0 raw personal data reaching the model after pseudonymization, 100% of AI replies scanned, 20+ contextual test cases, and two role outcomes) are **prototype targets, not measured field results**.

## Proposed technical approach

The project deck proposes Microsoft Presidio, spaCy NER, and regular expressions for detection; an LLM API or small classifier for context judgment; Python and FastAPI for policy enforcement and audit logging; a response scanner for output checks; and Streamlit for an internal dashboard. These are proposed components, not dependencies of this static website.

## Team

**Devhack Syndicate · NMAMIT**

- Niranjan M — Team Leader
- Yarukone Manish
- Nikhil N

## License

No license has been added yet. Until the repository includes a license, reuse is not granted by this README.
