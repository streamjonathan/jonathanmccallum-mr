# AGENTS.md — jonathanmccallum-mr (Marathi mirror of jonathanmccallum.com)

Marathi mirror site. Same theme and design as the main site (Paper Light),
content translated into Marathi, meaning-first. Repo: streamjonathan/jonathanmccallum-mr.
Live (when approved): mr.jonathanmccallum.com. Proof: jonathanmccallum-mr.pages.dev.

## Mission

Mirror jonathanmccallum.com in Marathi — every article translated for meaning,
not word for word, in Jonathan's voice: plain short sentences, friendly, positive,
never preachy. An average person interested in Jesus, not an expert or theologian.

## Roles

- **Bobby (Muse) is the lead builder.** He coordinates, builds, pushes to GitHub
  and deploys to Cloudflare. He is the ONLY one who pushes or deploys.
- **Claude advises and reviews** translation quality. He does not push or deploy.
- **Helper Muses translate** one article at a time, drafts only.

## The one rule above all

**Never publish or alter live production assets without Jonathan's clear
permission.** The Marathi site goes live on mr.jonathanmccallum.com only when
he says so, after reading the pilot article(s). Drafts stay drafts until he
approves them. Work on a branch, never straight on main. Give Bobby a preview URL.

## Translation rules

- English repo (streamjonathan.github.io) is the source of truth. Articles are
  translated from the English Markdown, keeping the same date, slug, source_video
  and shareImage. Only the title and body are translated.
- Lewis quotations: use the published Marathi translation where one exists
  (cite it); otherwise translate fresh and mark it "translated for this site".
- Bible verses: use the पवित्र शास्त्र (Marathi Bible – Old Version, re-edited, Bible Society of India, 2015 edition) wording, never re-translate from the English article. No direct verse quotations appear in the 5 proof articles; the 'bread of life / water of life' lines are Jonathan's paraphrase, translated meaning-first.
- Names (never vary): यीशु, देव, अस्लान, नार्निया, लुसी, डिगरी, टिरियन, आदाम आणि हव्वा. Book titles use the site translations (नार्नियाच्या कथा, जादूगाराचा पुतण्या, महान घटस्फोट, अंतराळ त्रयी, शेवटची लढाई) — flagged for Jonathan, as no published Marathi edition of any Lewis book was found.
- Voice: Register: respectful तुम्ही, warm and personal, short plain sentences, no preaching.
- No emojis, no newsletter form, no links the English article does not have.
- Never invent facts, dates, links or details.

## Site facts

- Eleventy 3, Cloudflare Pages, Paper Light theme (Fraunces + Newsreader).
- No Ask chat and no note Worker on this site yet — search (Pagefind) works,
  Ask and notes come later. The Ask floating button and ask.js are removed.
- CSS is preloaded, not inlined (CSP blocks inline style). Bump the `?v=` query
  on any CSS/JS file you change.
