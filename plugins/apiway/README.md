# Apiway — AI Workspace

AI website builder and workspace in chat.

Create a website, a landing page, a one-page presentation of your offer, a portfolio or a business
app — a CRM, a web app with sign-in, a Telegram or Instagram chatbot — by describing it in chat.
Apiway asks a few questions about your business and the look you want and builds it on a hosted
address. Everything lives in your Apiway AI workspace, where you can also draft an email marketing
campaign for the same business.

## What you can ask

- "Create a website for my coffee shop" — Apiway leads you through its brief step by step and builds
  the site into a private preview. Nothing is published.
- "Publish my Bean There site" — the site goes live and you get its public address. Publishing
  happens only when you ask for it.
- "Change the title of my site to a stronger marketing hook" — texts, pictures and blocks change
  without touching code, as a new preview version.
- "Create an email marketing campaign for this website" — a draft is saved in Apiway's Email
  Marketing. No email is sent to anyone.
- "Show me all my apps" — your apps, their preview and live addresses, and the credit balance.
- "Make a landing page for my webinar", "Build a CRM for my beauty salon".

## What is in the plugin

- Two skills: `apiway-apps` (build and change Apiway websites and apps) and `apiway-workspace`
  (mail, tasks, booking links, email marketing drafts, automations).
- One command: `/apiway:apiway` — create or open an Apiway app.
- One remote MCP server, `apiway`, at `https://apiway.ai/api/mcp/directory`.

## What it connects to and sends

The plugin runs no local code, hooks or scripts. It connects to one service: the Apiway MCP server
at `apiway.ai`, over HTTPS, signed in with your own Apiway account through OAuth. What you ask Claude
to do in Apiway — your brief, site texts, files of your apps, and the workspace data you ask about —
is sent to that server and to nowhere else. Sending a message, publishing and deleting need your
explicit yes. Keys and tokens are never asked in the chat.

You need an Apiway account: <https://apiway.ai>. Publishing and some tools depend on your Apiway plan.

## Links

- Support: <https://apiway.ai/contact-us>
- Privacy policy: <https://apiway.ai/legal/privacy-policy>
- Terms of use: <https://apiway.ai/legal/terms-of-use>

## License

MIT
