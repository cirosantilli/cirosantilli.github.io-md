# List topics on home page

↑ **Parent:** [Advances](advances.md)

<a id="_12"></a>
The new default homepage for a logged out user how shows a list of the topics with the most articles.

<a id="_13"></a>
This is a reasonable choice for default homepage, and it immediately exposes users to this central feature of the website: the topic system.

<a id="_14"></a>
Doing this required in particular calculating the best title for a topic, since it is possible to have different titles with the same ID, the most common way being with capitalization changes, e.g.:<a id="_15"></a>

```
JavaScript
Javascript
```
would both have topic ID `javascript`.

<a id="_16"></a>
With this in place we also added the preferred topic title to the top topic page.

<a id="_17"></a>
The algorithm chosen is to pick the top 10 most upvoted topics, and select the most common title from amongst them. This should make topic title vandalism quite hard. This was made in a single [SQL](../../../sql-split.md) query, and became the most complext SQL query [Ciro Santilli](../../../ciro-santilli-split.md) has ever written so far: [https://twitter.com/cirosantilli2/status/1549721815832043522](https://twitter.com/cirosantilli2/status/1549721815832043522)

<a id="image-screenshot-showing-the-list-of-topics"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/OurBigBook_topic_index_page.png" alt="" height="800">

**[Figure 2](#image-screenshot-showing-the-list-of-topics). Screenshot showing the list of topics**. The page is: [https://ourbigbook.com](https://ourbigbook.com) for the logged out user, [https://ourbigbook.com/go/topics](https://ourbigbook.com/go/topics) for the logged in user.

<a id="image-screenshot-showing-a-topic-page"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/master/OurBigBook_topic_page_with_title.png" alt="" height="400">

**[Figure 3](#image-screenshot-showing-a-topic-page). Screenshot showing a topic page**. The page is: [https://ourbigbook.com/go/topic/vector-space](https://ourbigbook.com/go/topic/vector-space). Before this sprint, we didn't have the "Vector Space" at the top, as it wasn't necessarily trivial to determine what the preferred title would be.

## ↑ Ancestors (7)

1. [Advances](advances.md)
2. [OurBigBook.com](ourbigbook-com.md)
3. [Ciro's Edict \#8](../8-split.md)
4. [Sponsor updates](../../../sponsor-updates.md)
5. [Update from Ciro Santilli](../../../update-from-ciro-santilli.md)
6. [Ciro Santilli](../../../ciro-santilli-split.md)
7. [Ciro Santilli's Homepage](../../../split.md)
