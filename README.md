# King of the Curve

King of the Curve helps MCAT learners discover public KOTC topic resources, practice with the interactive Daily Challenge, and review their connected KOTC study account. It does not access AAMC accounts or retrieve official full-length exam content.

## Try it

- “Find the King of the Curve biology topics and open the matching resource.”
- “Open today's MCAT Daily Challenge without revealing the answer.”
- “Show my King of the Curve study dashboard.”
- “Show up to 10 chapters of my biology study roadmap.”
- “List my KOTC flashcard decks, then help me review a deck I choose.”

## Connection and permissions

The plugin sends requests to the existing [King of the Curve MCP service](https://kotc-mcp-347848146862.us-central1.run.app/mcp). Public `search`, `fetch`, and `get_daily_challenge` tools do not need a linked account. The dashboard and roadmap require OAuth `study.read`; flashcard tools require OAuth `flashcards.read`. Sign in through the KOTC authorization screen, not in chat. Account information is limited to the connected account. No tool creates, edits, deletes, or saves study progress, decks, cards, or account details.

Search queries, category requests, and exact returned resource or deck IDs are sent to the declared service. OAuth-protected requests retrieve the requested KOTC study information through that service and return it to the client where the tool was invoked. The package has no executable scripts, hooks, local servers, background tasks, or additional data destinations. The Daily Challenge component reveals its answer only after a choice; clients without component support can display the question and options without exposing component-only answer metadata. Score projections are educational estimates, not guaranteed exam results or medical advice.

## Help

- [Connector documentation](https://kotc-mcp-347848146862.us-central1.run.app/docs)
- [Support](https://kotc-mcp-347848146862.us-central1.run.app/legal/support)
- [Privacy](https://kotc-mcp-347848146862.us-central1.run.app/legal/privacy)
- [Terms](https://kotc-mcp-347848146862.us-central1.run.app/legal/terms)

Copyright 2026 King of the Curve LLC. Proprietary; all rights reserved.
