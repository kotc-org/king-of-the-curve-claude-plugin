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

Search queries, category requests, and exact returned resource or deck IDs are sent to the declared service. OAuth-protected requests for normal accounts retrieve authorized KOTC study information through that service. For the enabled exact designated reviewer, the four private tool results use only the synthetic sample described below. Results return only to the invoking client. The package has no executable scripts, hooks, local servers, background tasks, or additional data destinations. The Daily Challenge component reveals its answer only after a choice; clients without component support can display the question and options without exposing component-only answer metadata. Score projections are educational estimates, not guaranteed exam results or medical advice.

## Designated synthetic reviewer

When the service enables its exact designated reviewer account, all four private tools return only a labeled KOTC-original synthetic reviewer demonstration: dashboard, roadmap, deck list, and deck cards. These tool results do not read upstream private production study data. Three original circuit questions simulate two answered responses, one correct, one incorrect, and one unanswered. Accuracy is 50% among the two answered sample questions; dashboard totalQuestions means answered questions and equals 2, while demonstration.question_count is 3. The sample roadmap has one circuits chapter with 2 of 3 questions answered (66.7% completion). Its category ID must come from demonstration.roadmap_category_id returned by the dashboard, not from a guessed ID or a public Biology category. One separate original circuits deck contains five flashcards; flashcards are not question attempts. Score predictions, percentiles, target score, exam date, and daily study preferences are unavailable/null. This is not real learner history, a completed production exam, a 230-question full-length, official AAMC content, or cohort analytics. Other accounts retain their normal authorized production paths. Public search, fetch, and Daily Challenge still use published educational content.

Existing OAuth, scopes, Firebase account/refresh/revocation checks, and client binding remain required. The gate is optional and disabled by default. It does not create accounts, grant permissions, add a new MCAT membership guard, or write production exams, attempts, study data, flashcards, or analytics. A caller cannot enable it by supplying a UID or email. Unknown sample deck and category IDs fail without an upstream private-data fallback.

## Release status

Version 1.0.2 is a locally prepared submission candidate, not evidence of deployment, hosted-client coverage, submission, approval, or publication. Its sample-only behavior requires the separately reviewed runtime to be released and configured for the exact verified reviewer identity. This packaging task did not deploy code, use credentials, upload packages, connect OAuth, execute host cases, record a walkthrough, or submit a listing. A genuine post-release video URL is intentionally omitted; enter only a verified accessible recording through the review field after actual host tests. The historic video is not current sample-only acceptance evidence.

## Help

- [Connector documentation](https://kotc-mcp-347848146862.us-central1.run.app/docs)
- [Support](https://kotc-mcp-347848146862.us-central1.run.app/legal/support)
- [Privacy](https://kotc-mcp-347848146862.us-central1.run.app/legal/privacy)
- [Terms](https://kotc-mcp-347848146862.us-central1.run.app/legal/terms)

Copyright 2026 King of the Curve LLC. Proprietary; all rights reserved.

## License

This package is proprietary and UNLICENSED. All rights remain reserved. No open-source license is granted.
