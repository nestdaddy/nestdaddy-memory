# NestDaddy Memory

**Start your AI's memory today. It gets smarter every day you wait.**

If you want your AI projects to perform, you need memory. No memory, no momentum: every session starts from zero. NestDaddy Memory is one memory for every AI you use. Tell it once, and every AI you connect, today's and tomorrow's, already knows your projects, your decisions and how you like things done, on every device. Any app or agent that supports MCP (Model Context Protocol) can read and write it: ChatGPT, Claude, Cursor, Claude Code, VS Code, Windsurf and many more.

**Try it free for 7 days. Love it? Stay. Don't? Cancel before day 7 and pay nothing.**

[![Official MCP Registry](https://img.shields.io/badge/MCP%20Registry-com.nestdaddy%2Fmemory-0a7c4e)](https://registry.modelcontextprotocol.io/v0/servers?search=com.nestdaddy/memory)
[![7 days free](https://img.shields.io/badge/7%20days-free-15181e)](https://nestdaddy.com/memory)

```
https://nestdaddy.com/memory/mcp
```

**Website and sign-up:** https://nestdaddy.com/memory

---

## Why

AI is brilliant for an hour. Then you open a new chat, or switch to another app, and it has no idea who you are.

- You explain your project again in every new conversation.
- You switch from one AI to another and start from zero.
- Your AI forgets the decision you made yesterday, or worse, acts on the old one.
- The built-in memory of each app fills up, and only that one app can read it.

NestDaddy Memory is a memory that lives **outside** any single app. Every AI you connect reads and writes the same memory.

## Built for developers

- **Stop paying tokens to re-explain your own project.** Your AI looks up only what matters, by meaning, instead of you pasting context into every session.
- **Your AI remembers the task. You just ship.** Say "finish yesterday's work" and it knows which work.
- **Smarter models need a memory to show it.** Switch models and the memory comes with you, so the new one starts already knowing you.

A field report from daily terminal work: [I work with an AI that remembers everything](https://nestdaddy.com/blog/i-work-with-an-ai-that-remembers).

## What makes it different

| | Built-in app memory | NestDaddy Memory |
|---|---|---|
| Works across apps | Only inside that app | Every MCP app and agent, any model |
| Works across devices | Per account | Laptop, phone, terminal, all the same memory |
| Room | Small, fills up ("memory full") | Unlimited |
| When a fact changes | Old and new often both stay | **The latest decision wins**: the old version is replaced |
| Finds things by | Exact words | Meaning, in any language and mixes of languages |
| Time | No timeline | "What did I decide last week?" works |
| Past conversations | Stay inside that app | Every chat with every AI, found again from a vague question |
| Yours | Locked to the vendor | See, change, export or delete anything |

## Connect it (about two minutes, no keys to copy)

Every app opens a NestDaddy sign-in. You click **Allow** and it is connected (OAuth). Your first month starts when you connect your first app.

### ChatGPT
Settings, then **Apps & Connectors** (some versions say Connectors). Add a connector with the URL `https://nestdaddy.com/memory/mcp`, sign in, click Allow.

### Claude (claude.ai and the desktop app)
Settings, then **Connectors**, then **Add custom connector**. Name it `NestDaddy Memory`, URL `https://nestdaddy.com/memory/mcp`, then sign in and Allow.

### Claude Code
```bash
claude mcp add --transport http nestdaddy-memory https://nestdaddy.com/memory/mcp
```
Then run `/mcp` inside Claude Code and choose **Authenticate**.

### Cursor
`~/.cursor/mcp.json`:
```json
{
  "mcpServers": {
    "nestdaddy-memory": { "url": "https://nestdaddy.com/memory/mcp" }
  }
}
```

### VS Code
`.vscode/mcp.json`:
```json
{
  "servers": {
    "nestdaddy-memory": { "type": "http", "url": "https://nestdaddy.com/memory/mcp" }
  }
}
```

### Any other MCP app or agent
Add a remote MCP server (Streamable HTTP) with the URL `https://nestdaddy.com/memory/mcp`. Clients that support MCP OAuth find the sign-in by themselves (`/.well-known/oauth-protected-resource/memory/mcp`).

## Make your AI use it every time

AI apps only open a connector when told to. Add one line to your app's custom instructions (ChatGPT: Settings, Personalization, Custom instructions; Claude: your profile preferences; coding apps: the project or user rules):

```
My main memory is the NestDaddy Memory connector. On every message, first call its recall tool with what I said.
When I tell you a lasting fact, preference or decision, save it there; when a decision changes, update the old
memory instead of adding a new one. After each answer, log the turn with log_turn.
```

## What a normal week looks like

- **Monday**, in ChatGPT on your phone: "I'm cutting sugar and training for a 10 km run."
- **Wednesday**, in Claude on your laptop: "Dinner idea?" It suggests something low in sugar and high in protein, without being reminded.
- **Friday**, anywhere: "I switched to the half marathon." The memory updates, and from then on every AI plans for the half marathon.

For developers: tell Claude Code your architecture decisions once, and Cursor tomorrow follows them. Switch models without re-explaining the project.

## What your AI can do with it

- **Save** lasting facts, preferences and decisions, one topic per memory.
- **Recall on every message**: give it what the user said and get back only what clearly relates, from memories and past chats.
- **Search by meaning**, not just keywords, in any language and mixes of languages.
- **Update in place**: when a decision changes, the newest version replaces the old one, and the history is kept.
- **Answer time questions**: "what did I decide about pricing last month?"
- **Remember every conversation**: each chat is logged (passwords and keys removed), so "continue yesterday's work" or "not that one, the other one" finds the exact moment.
- **Keep it tidy**: find duplicates, merge them, archive what is finished.

## Privacy

- Your memory lives in its own separate file, reached only through your own sign-in, over encrypted connections.
- Each connected app can be removed from your account page at any time.
- You can export or delete everything yourself, memories and conversations. Ask your AI to delete one chat at any time.
- Your memory never expires: stop paying and it stays safe and read-only, waiting for you.
- Your own AI writes the memories and our engine stores, finds and updates them, so there are no credits or tokens to pay per save.

Full terms: https://nestdaddy.com/memory#faq

## Price

- **7 days free.** You add a card when you start; cancel before day 7 and you pay nothing.
- Then **USD 9.99 a month**, or USD 99.90 a year (pay for 10 months, get 12). Launch price, kept for as long as you stay subscribed.
- We email you 3 days before the first charge, with a one-click cancel link.

**Start here:** https://nestdaddy.com/memory

## Listing

- Official MCP Registry: `com.nestdaddy/memory` ([server.json](server.json))
- Endpoint: `https://nestdaddy.com/memory/mcp` (Streamable HTTP, OAuth 2.1)

## More from NestDaddy

- [NestDaddy MCP](https://nestdaddy.com/mcp): give your AI today's internet, with live web search, real-time breaking news and full page reading.
- [Blog](https://nestdaddy.com/blog): [I work with an AI that remembers everything](https://nestdaddy.com/blog/i-work-with-an-ai-that-remembers) · [ChatGPT memory full?](https://nestdaddy.com/blog/chatgpt-memory-full) · [Move your ChatGPT memory to Claude](https://nestdaddy.com/blog/move-chatgpt-memory-to-claude) · [One memory for every AI](https://nestdaddy.com/blog/one-memory-for-every-ai)

## Support

hello@nestdaddy.com · Issues and questions are welcome in this repository.
