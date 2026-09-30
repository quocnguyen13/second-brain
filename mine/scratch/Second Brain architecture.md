
# Folder Tree

```
Second-Brain/                
├── CLAUDE.md                The rules Claude loads every session; imports system/context.md and system/conventions.md
├── index.md                 One line per wiki page; how /ask finds pages
├── log.md                   Append-only record of every operation
├── inbox/                   Input zones
│   ├── sources/             → /ingest. The Web Clipper saves here
│   ├── questions.md         → /ask. "- [ ] YYYY-MM-DD question"
│   └── checks.md            → /lint. "- [ ] YYYY-MM-DD what to verify"
├── raw/                     Sources, never edited. <author>-<short-title>.<ext>; Markdown and PDF
│   └── assets/              Images, as attachments only
├── wiki/                    What Claude compiles. Every claim cites raw/
│   ├── overview.md          The whole picture, rewritten at every ingest
│   ├── sources/             One page per source
│   ├── entities/            People, organisations, things
│   ├── concepts/            Ideas, and where the sources agree or disagree
│   └── analyses/            Answers you chose to file
├── mine/                    Your thinking layer
│   ├── insights/            Your conclusions, linked to wiki/ through Relations
│   ├── decisions/           Your own decisions (decisions about the system go in doc 07)
│   ├── drafts/              Claude's insight drafts only, waiting for your call
│   ├── scratch/             Where your new notes start
│   ├── journal/             Daily notes
│   └── projects/            thinking-system/ holds docs 00–22, the only folder synced to this Project
├── system/
│   ├── context.md           Yours: current focus and your domains
│   ├── conventions.md       How Claude writes: templates, naming, formats
│   ├── templates/           9 page templates (doc 10)
│   ├── views/Review.base    The two review views: Needs attention and Draft queue
│   ├── lint/                Lint reports
│   └── test-results.md      Every test run
├── .claude/
│   ├── settings.json        Permissions and modes
│   ├── settings.local.json  Your "don't ask again" approvals; git ignores it
│   └── skills/              ingest, ask, file-answer, lint, drafts
├── .obsidian/               Obsidian's own settings
└── .gitignore, .gitattributes
```

