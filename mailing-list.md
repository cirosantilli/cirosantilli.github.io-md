# Mailing list

↑ **Parent:** [Website](website-split.md)  
🏷️ **Tags:** [Essays by Ciro Santilli](essays-by-ciro-santilli.md), [Evil](evil.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Mailing_list)

It boggles [Ciro Santilli](ciro-santilli-split.md)'s mind that people use [mailing list](mailing-list.md) to collaborate on projects!

The only explanation is that the dinosaurs who created the projects are unable to adapt to new superior technologies.

Yes, Ciro is talking to you, big fundamental projects from last century: [Linux kernel](linux-kernel.md), [GNU Compiler Collection](gnu-compiler-collection.md) ([https://gcc.gnu.org/lists.html](https://gcc.gnu.org/lists.html)), [Binutils](binutils.md) ([https://sourceware.org/binutils/](https://sourceware.org/binutils/)), etc.

Some of you are already using Bugzilla for the bugs, so kudos. But if you've seen their benefit, why you still use the mailing list for patches?

Advantages of mailing lists:
- threaded replies, which almost no issue tracker has. [GitHub](github.md) feature request: [https://github.com/isaacs/github/issues/837](https://github.com/isaacs/github/issues/837)

Disadvantages: everything else:
- cannot subscribed to a single thread. Which forces you to create an email filter for each one of them you subscribe to.
- no metadata, notably the notion of closing / merging, but also upvotes

  You have to read thirty messages before you can know if the bug was solved or not.
- it is insanely hard to reply to messages from before you were subscribed: [https://webapps.stackexchange.com/questions/23197/reply-to-mailman-archived-message/115088#115088](https://webapps.stackexchange.com/questions/23197/reply-to-mailman-archived-message/115088#115088)

  This forces everyone to subscribe to all lists, and then set up email filters to not be flooded with emails.
- hard to apply patches locally to test them out: [https://stackoverflow.com/questions/5062389/how-to-use-git-am-to-apply-patches-from-email-messages/49082916#49082916](https://stackoverflow.com/questions/5062389/how-to-use-git-am-to-apply-patches-from-email-messages/49082916#49082916)

  Unless they use Patchwork, which adds one more website on top of the mess.

  And then [Gmail](gmail.md) corrupts your patches, and you are forced to use `git send-email`, which does not work on some network configurations: [https://stackoverflow.com/questions/28038662/how-to-solve-unable-to-initialize-smtp-properly-when-using-using-git-send-ema](https://stackoverflow.com/questions/28038662/how-to-solve-unable-to-initialize-smtp-properly-when-using-using-git-send-ema) or setup ThunderBird.
- often have to subscribe to post at all, thus cluttering your inbox further
- you can edit posts to make them clearer.

  Yes, people could vandalize their answers when they get mad, and threads might stop making sense after edits. But this can be solved with an undeletable post history like Stack Overflow has (but not any other tracker does).

  Or archive.org :-)

  In any case, what do you think will happen more often and have greater impact:
  - people vandalize their posts
  - people fix their silly typos and improve content
- searchable by author, keyword, etc. without Google. Yes, mailing list trackers could have decent implementations to overcome that. But no, GNU Mailman which everyone uses does not have it. Google barely indexes it.

  And I don't think Google properly indexes many of the mailing list archives for some reason: I never get hits for my own posts a week later, while I often do on GitHub issues.
- people have to learn about top posting vs inline posting, and this requires infinite education of new users
- Line comments in code reviews like GitHub and GitLab.

  On mailing lists: either put a comment in the middle of a huge patch and let other people find it, or (more likely) copy paste the part of the patch that you are talking about.
- most mail web UIs suck.

  OK, this is not an unsolvable or intrinsic problem, but still a problem.

  E.g.: `ezmlm` it is not possible to see the entire content in a single page: [https://gcc.gnu.org/ml/gcc/2015-07/threads.html](https://gcc.gnu.org/ml/gcc/2015-07/threads.html).

  Unless you like reading threads backwards and with 4 levels of `>` quotations.

  The alternative: do like LLVM and send attachments. Yes, I we all love opening up attachments on our browsers.

  The real solution: everyone can create branches and pull requests. Also has the benefit of running [CI](continuous-integration.md) on the pull requests.

Not sure:
- you can have infinitely many trackers to replicate data in case apocalypse happens in some part of the world.

  Although I'm not sure this is an advantage, as you don't know anymore which one is the canonical trackers an advantage, as you don't know anymore which one is the canonical tracker.

  And all web interfaces already have an API to export messages, and someone has already scripted it to import from any web UI to any web UI for you.

  And GitHub offers infinite precise history transparently on its API.

Smart people who agree with Ciro:
- [https://news.ycombinator.com/item?id=13631069](https://news.ycombinator.com/item?id=13631069)
- [https://softwareengineering.stackexchange.com/questions/191961/why-do-some-big-projects-like-git-and-debian-only-use-a-mailing-list-and-not-a#comment779146_256479](https://softwareengineering.stackexchange.com/questions/191961/why-do-some-big-projects-like-git-and-debian-only-use-a-mailing-list-and-not-a#comment779146_256479)

## ↑ Ancestors (3)

1. [Website](website-split.md)
2. [Art](art-split.md)
3. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (7)

- [Bitcoin whitepaper](bitcoin-whitepaper.md)
- [Carl Victor Page, Jr.](carl-victor-page-jr.md)
- [Ciro Santilli](ciro-santilli-split.md)
- [Protests against larger block sizes](cool-data-embedded-in-the-bitcoin-blockchain/protests-against-larger-block-sizes.md)
- [Evil](evil.md)
- [Mailing list](mailing-list.md)
- [Scott Hassan](scott-hassan.md)
