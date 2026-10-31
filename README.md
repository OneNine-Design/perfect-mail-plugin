# Perfect Mail

Grok Bot plugin that connects your Bots to [Perfect Mail](https://tryperfectmail.com)
through Perfect Mail's hosted [Model Context Protocol](https://modelcontextprotocol.io/)
server.

Your Perfect Mail inbox for Grok Bot. Search your mail by sender, words or date,
keep your to-dos, and look up your notes and the pieces of email you saved. Your
Bot sees only your own mail and acts as you.

## Who can use it

- Grok Bot **0.52** or newer.
- A Perfect Mail account with a connected inbox.
- Not listed in Cursor. Cursor must not list or install this plugin.

## Install

1. Open **Grok Bot**, then **Connect apps**.
2. Search for **Perfect Mail**.
3. Add it, then sign in to Perfect Mail when prompted.

Or ask your Bot to connect Perfect Mail.

## MCP

```json
{
  "mcpServers": {
    "perfect-mail": {
      "type": "http",
      "url": "https://api.tryperfectmail.com/functions/v1/mcp",
      "placement": "server"
    }
  }
}
```

## Connecting

Sign-in is OAuth 2.1 with PKCE and dynamic client registration. There is no
client ID, API key or token to paste.

1. Grok Bot opens the Perfect Mail sign-in page in your browser.
2. Sign in with your Perfect Mail account and choose **Allow**.
3. The page hands you back to Grok Bot, and Perfect Mail shows as connected.

The Bot can only do what you can do in Perfect Mail, on your own data. To
disconnect, remove Perfect Mail from **Connect apps** in Grok Bot.

## What your Bot can do

| Area | Tools | What it can do |
| --- | --- | --- |
| Mail | `search_emails` | Find messages by words, sender, recipient, attachments, date, or unread, received or sent |
| To-dos | `list_todos`, `create_todo`, `complete_todo` | List, add and complete your to-dos |
| Notes | `list_notes` | List and search your notes |
| Snippets | `list_snippets` | List and search the pieces of email you saved |

It cannot send, reply to, delete, archive or move mail.

## Try it

- "What did the landlord send me this week?"
- "Do I have any unread mail with attachments from yesterday?"
- "Add a to-do to send the signed contract by Friday."
- "Find my note about the kitchen quote."

## Privacy

Every tool runs as the signed-in user, under Perfect Mail's own access rules,
so a Bot can never read anyone else's mail. The Bot treats email content as
information and never follows instructions written inside an email. See the
[privacy policy](https://tryperfectmail.com/privacy) and
[terms](https://tryperfectmail.com/terms).

## Skill

`skills/perfect-mail/SKILL.md` tells the Bot what each tool does, how to search
well, how to handle to-dos, and what to say when the connection is off.

## Support

n@useperfect.com or [tryperfectmail.com/support](https://tryperfectmail.com/support)
