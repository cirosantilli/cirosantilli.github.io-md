# The Math Genome Project

↑ **Parent:** [Web-based proof assistant](web-based-proof-assistant.md)  
🏷️ **Tags:** [Closed source software](closed-source-software.md)

[https://www.themathgenome.com/](https://www.themathgenome.com/)

The website was dead as of February 2025. Last archive: [https://web.archive.org/web/20240418004442/http://www.themathgenome.com/](https://web.archive.org/web/20240418004442/http://www.themathgenome.com/) Pings:
- [https://x.com/cirosantilli/status/1890873216551313861](https://x.com/cirosantilli/status/1890873216551313861)
They were seeking help on May 2024:
- [https://x.com/TheMathGenome/status/1792963871193608593](https://x.com/TheMathGenome/status/1792963871193608593)
- [https://www.linkedin.com/feed/update/urn:li:activity:7198688750355259393/](https://www.linkedin.com/feed/update/urn:li:activity:7198688750355259393/)
so its likely the followup death. LinkedIn post gives basic stack: MERN stack, [Heroku](heroku.md), Supabase/[MongoDB](mongodb.md) Atlas.

Appears to support multiple [proof assistant](proof-assistant.md) backends including [Lean](lean-proof-assistant.md), Hol and [Coq](coq-software.md).

A discussion on the [Lean](lean-proof-assistant.md) Zulip: [https://leanprover.zulipchat.com/#narrow/stream/113488-general/topic/The.20Math.20Genome.20Project/near/352639129](https://leanprover.zulipchat.com/#narrow/stream/113488-general/topic/The.20Math.20Genome.20Project/near/352639129). Lean people are not convinced about the model in general it seems however.

TODO [closed source](closed-source-software.md)? Really? [https://www.themathgenome.com/pricing](https://www.themathgenome.com/pricing)

TODO not viewable without login?

Has [conjectures](conjecture.md) feature.

Built by this dude John Mercer:
- [https://www.linkedin.com/in/johnmercer/](https://www.linkedin.com/in/johnmercer/)
- [https://x.com/john_d_mercer](https://x.com/john_d_mercer)
He must be [independently wealthy](independently-wealthy.md) or something to do such a project? What a hero. But he seems to have jobs. On the side? Hardcore.

A failed [Hacker News](hacker-news.md) self post: [https://news.ycombinator.com/item?id=35775071](https://news.ycombinator.com/item?id=35775071) 

[Ciro Santilli](ciro-santilli-split.md) asked: [https://discord.com/channels/1096393420408360989/1096393420408360996/1137047842159079474](https://discord.com/channels/1096393420408360989/1096393420408360996/1137047842159079474)

> Does the website actually automatically check the formal proofs, or is this intended to be implemented at some point? And if yes, is it intended to allow proofs to depend on other proofs of the website (possibly by other people)

Owner:

> Hi Ciro, yes we will be releasing in-browser proof assistant environments/checkers (e.g. Lean). Our goal is not to replace the underlying open-source repos (e.g. Mathlib) so the main dependency will be on the current repos; then when statement formalizations and proofs come in and are certified they can be PR'd to the respective repos. So we will be the source of truth for the informal latex code but only a stepping stone and orchestration layer on the way to the respective formal libraries.

So apparently there will be proof checking, but no dependencies between proofs, you still have to pull request everything back and face the pain.

Bibliography:
- [https://www.reddit.com/r/mathematics/comments/1cpm5kb/math_genome_project/](https://www.reddit.com/r/mathematics/comments/1cpm5kb/math_genome_project/)
- [https://news.ycombinator.com/item?id=35775071](https://news.ycombinator.com/item?id=35775071) by the creator

## ↑ Ancestors (6)

1. [Web-based proof assistant](web-based-proof-assistant.md)
2. [Proof assistant](proof-assistant.md)
3. [Formalization of mathematics](formalization-of-mathematics-split.md)
4. [Area of mathematics](area-of-mathematics.md)
5. [Mathematics](mathematics-split.md)
6. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [Website front-end for a mathematical formal proof system](website-front-end-for-a-mathematical-formal-proof-system.md)
