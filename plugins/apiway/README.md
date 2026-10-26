# Apiway

Create a website, a landing page, a portfolio or a business app — a CRM, a web app with sign-in, a
Telegram or Instagram chatbot — by describing it in chat. Apiway asks a few questions about your business
and the look you want, builds a private preview on a hosted address, and publishes it when you ask. The
same account keeps your Apiway workspace: mail, tasks, booking links, email marketing drafts and
automations.

## Try it

- "Create a website for my coffee shop"
- "Make a landing page for my webinar"
- "Build a CRM for my beauty salon"
- "Show me all my apps"

## What is inside

- **Connector** `apiway` — Apiway's remote MCP server, `https://apiway.ai/api/mcp/directory`. You sign in to your own Apiway
  account with OAuth the first time a tool is used; a free account is enough to build a preview.
- **Skill** `apiway-apps` — how to lead you through the brief, build the preview and change the site or app.
- **Skill** `apiway-workspace` — how to work with mail, tasks, email marketing and automations.
- **Command** `/apiway` — create or open an Apiway app.

## What it runs and sends

The plugin runs nothing on your computer: no hooks, no scripts, no local server. Claude calls the Apiway
connector over HTTPS, and only what a tool call carries leaves the chat — your answers to the brief, the
texts and files of the app you are building, the message you asked to draft. Everything is stored in your
Apiway account. Sending a message and deleting happen only after your explicit yes; publishing a site
happens only when you ask for it.

## Links

- Documentation: https://apiway.ai/mcp
- Support: https://apiway.ai/contact-us · info@apiway.ai
- Privacy policy: https://apiway.ai/legal/privacy-policy
- Terms of use: https://apiway.ai/legal/terms-of-use
