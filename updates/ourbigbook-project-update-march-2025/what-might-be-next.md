<h1 id="ourbigbook-project-update-march-2025/what-might-be-next">What might be next</h1>

↑ **Parent:** [OurBigBook Project Update March 2025](../ourbigbook-project-update-march-2025.md)

OK, I need to do content. I know :-) At the university I'm at, the only department that is open is the mathematics one. Both:
- physically, I'm sitting next to some students right now, though they don't yet know that their saviour is just next to them.
- in terms of publishing the course materials online. Many of them even have solution
All other courses extremely closed, notably Physics, which is the other course I'd consider. There are upsides and downsides for going for Mathematics:
- upside:
  - maths doesn't change with time
  - maths doesn't require experiments
- downside: most of it is useless compared to Physics
If I were free to choose, I might go for Physics instead. But maths isn't hard, and I think I'll just go with the hand I'm dealt this time to start with.

Tech wise, the big things are the following ones to which I have given different levels of architectural consideration (i.e. read: I'm afraid they'll be fucking hard and that I'll spend a month on yet another useless feature that won't help get a single user). I don't think I'll do those before at least a little bit of content, we'll see:
- [WYSIWYG](../../wysiwyg.md): this is not a question of if, but when and how. Even I miss it when dealing with images. I was particularly impressed by [Trillium Notes](../../trillium-notes.md), and might consider forking it or reusing some of its components
- perfect two way sync from web to local: [https://github.com/ourbigbook/ourbigbook/issues/326](https://github.com/ourbigbook/ourbigbook/issues/326) 

  Currently, after much effort, publishing from local to web is extremely good.

  But pulling back changes that you make on web UI locally is not really possible. A basic version can be made easily, but a great version requires some thought.

  In particular, preventing accidental rewrite on simultaneous local + web edits require edit history to be in place.

  The rationale here is that users would start editing on Web with a low entry barrier. And as they become more committed to the project, they would eventually transition to having editing most of their content locally from a desktop, with the exception of a few minor edits on the go when they are on a cell phone, and which we want to very easily and automatically be pulled back to local as soon as they open an editor on their laptop.

  I.e. we want to add a downwards arrow to the following diagram:

  <img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/local-editing/bigb-publish-to-web-or-static-editor-logos.svg" alt="" height="600">

Smaller cute tech that I might do before content "real quick" include:
- move more into community tagging rather than just community topic-ing:
  - [https://github.com/ourbigbook/ourbigbook/issues/359](https://github.com/ourbigbook/ourbigbook/issues/359)
  - [https://github.com/ourbigbook/ourbigbook/issues/360](https://github.com/ourbigbook/ourbigbook/issues/360)
- automatic topic rendering for plaintext! [https://github.com/ourbigbook/ourbigbook/issues/356](https://github.com/ourbigbook/ourbigbook/issues/356). In particular this could open the doors for AI generated content.

Another thing I really want to do before time is up is to create a video summarizing my [philosophy of education](../../philosophy-of-education.md). I want it to be as fun and funny and sad as possible, with silly moving animated images and slides, not just me talking to the camera. Although all of the points I intend to talk about have undoubtedly been covered by others, it is something that I feel so strongly about that I would like to tell others about it more personally. If I start it it will likely take a few days to get done, and I'm not sure wha the final quality would be. It is a bit sad to not do "project work", but I think I'll end up doing it regardless. Class it under "fundraising" if you will, as it may help to find other like minded but rich people.

## ↑ Ancestors (4)

1. [OurBigBook Project Update March 2025](../ourbigbook-project-update-march-2025.md)
2. [Updates](../../updates-split.md)
3. [Ciro Santilli](../../ciro-santilli-split.md)
4. [Ciro Santilli's Homepage](../../split.md)
