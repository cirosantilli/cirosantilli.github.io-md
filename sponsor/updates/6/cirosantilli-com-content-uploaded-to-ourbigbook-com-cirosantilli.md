<h1 id="cirosantilli-com-content-uploaded-to-ourbigbook-com-cirosantilli">cirosantilli.com content uploaded to ourbigbook.com/cirosantilli</h1>

↑ **Parent:** [Advances](advances.md)

<a id="_3"></a>
Managed to upload the content from the static website [https://cirosantilli.com](https://cirosantilli.com) (OurBigBook Markup source at [https://github.com/cirosantilli/cirosantilli.github.io](https://github.com/cirosantilli/cirosantilli.github.io)) to [https://ourbigbook.com/cirosantilli](https://ourbigbook.com/cirosantilli).

<a id="_4"></a>
Although most of the key requirements were already in place since the last update, as usual doing things with the complex reference content stresses the system further and leads to the exposition of several new bugs.

<a id="_5"></a>
The upload of OurBigBook Markup files to ourbigbook.com was done with the newly added [OurBigBook CLI](../../../ourbigbook-cli.md) `ourbigbook --web` option. Although fully exposed to end users, the setup is not super efficient: a trully decent implementation should only upload changed files, and would basically mean reimplementing/using [Git](../../../git.md), since version diffing is what Git shines at. But I've decided not to put much emphasis on CLI upload for now, since it is expected that initially the majority of users will use the Web UI only. The functionality was added primarily to upload the reference content.

<a id="_6"></a>
This is a major milestone, as the new content can start attracting new users, and makes the purpose of the website much clearer. Just having this more realistic content also immediately highlighted what the next development steps need to be.

<a id="_7"></a>
Once v1.0 is reached, I will actually make all internal links of [https://cirosantilli.com](https://cirosantilli.com) to point to [https://ourbigbook.com/cirosantilli](https://ourbigbook.com/cirosantilli) to try and drive some more traffic.

<a id="_8"></a>
The new content blows up by far the limit of the free [Heroku](../../../heroku.md) [PostgreSQL](../../../postgresql.md) database of 10k lines. This meant that I needed to upgrade the Heroku Postgres plugin from the free Hobby Dev to the 9 USD/month Hobby Basic: [https://elements.heroku.com/addons/heroku-postgresql](https://elements.heroku.com/addons/heroku-postgresql), so now hosting costs will increase from 7 USD/month for the dyno to 7 + 9 = 16 UDS/month. After this upgrade and uploading all of cirosantilli.com to ourbigbook.com, Heroku dashboard reads reads:<a id="_9"></a>

<a id="_10"></a>
- 30,918 rows out of 10,000,000
<a id="_11"></a>
- 61.0 MB (out of 10 GB)
so clearly if we are ever forced to upgrade plans again, it means that a bunch of people are using the website and that things are going very very well! Happy how this storage cost turned out so far.

<a id="_12"></a>
One key limitation found was that Heroku RAM memory is quite limited at 512MB, and JavaScript is not exactly the most memory economical language out there. Started investigation at: [https://github.com/ourbigbook/ourbigbook/issues/230](https://github.com/ourbigbook/ourbigbook/issues/230) Initially [working around that by simply splitting the largest files](../../../fix-it-twice.md). We were just on the verge of what could be ran however luckily, so a few dozen splits was enough, it managed to handle 70 kB [OurBigBook Markup](../../../ourbigbook-markup.md) inputs. So hopefully if we manage to optimize a bit more we will be able to set a maximum size of 100 kB and still have a good safety margin.

## ↑ Ancestors (7)

1. [Advances](advances.md)
2. [Ourbigbook.com](ourbigbook-com.md)
3. [Ciro's Edict \#6](../6-split.md)
4. [Sponsor updates](../../../sponsor-updates.md)
5. [Update from Ciro Santilli](../../../update-from-ciro-santilli.md)
6. [Ciro Santilli](../../../ciro-santilli-split.md)
7. [Ciro Santilli's Homepage](../../../split.md)
