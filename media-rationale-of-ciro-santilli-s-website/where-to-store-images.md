<h1 id="media-rationale-of-ciro-santilli-s-website/where-to-store-images">Where to store images</h1>

↑ **Parent:** [Media rationale of Ciro Santilli's website](../media-rationale-of-ciro-santilli-s-website.md)

Since images are large, they bring the following challenges:
- keeping images in the main Git repository with text content makes the repository huge and slow to clone, and should not be done
- storing and serving images could cost us, which we want to avoid

To solve those problems, the following alternatives appear to be stable enough and should be used decreasing preference:
- for all images, use the separate GitHub repository: [https://github.com/cirosantilli/media](https://github.com/cirosantilli/media)

  This way, the entire website is relies on a single third party: GitHub, so we have a simple [single point of failure](https://en.wikipedia.org/wiki/Single_point_of_failure).

  We are at the mercy of GitHub's 1GB size policy: [https://help.github.com/en/articles/what-is-my-disk-quota](https://help.github.com/en/articles/what-is-my-disk-quota), but it will take a while to hit that.

  GitLab however has a 10Gb maximum size: [https://about.gitlab.com/2015/04/08/gitlab-dot-com-storage-limit-raised-to-10gb-per-repo/](https://about.gitlab.com/2015/04/08/gitlab-dot-com-storage-limit-raised-to-10gb-per-repo/) so we could move there is we ever blow up 1Gb on GitHub.

  Both GitLab and GitHub allow uploading files through the web UI, so downloading a large repo is never needed to contribute.

  GitHub does not serve videos like it does images however as of 2019.
- [Wikimedia Commons](https://commons.wikimedia.org/wiki/Main_Page) for videos if the following conditions are met:
  - [in scope](https://commons.wikimedia.org/wiki/Commons:Project_scope): "educational material in a broad sense", but not e.g. "Private image collections, e.g. private party photos, photos of yourself and your friends, your collection of holiday snaps and so on.". I don't think they will be too picky even with low quality photos.
  - allowed format, e.g. images or videos, but not ZIPs
  - allowed license: CC BY SA, but no fair use

  Since Wikimedia Commons has a higher level of curation and is an educational not-for-profit, it is the method most likely to remain available for the longest time.

  For this reason, we highly recommend uploading any acceptable files there as well as an additional backup.

  The downside is that its tooling is not as good, e.g. [there are a bunch of messy unofficial tools for batch operations](https://webapps.stackexchange.com/questions/135251/how-to-download-all-files-from-an-uploader-on-wikimedia-commons), and upload takes more effort.

  Another downside of Wikimedia Commons is that while we can choose the basename of files, it also adds some extra SHA crap to the beginning of URLs, making them harder to predict.

  Another serious downside is that they randomly rename images without redirects... e.g. they renamed [https://upload.wikimedia.org/wikipedia/en/0/03/STJ_SVG_file.svg](https://upload.wikimedia.org/wikipedia/en/0/03/STJ_SVG_file.svg) to [https://upload.wikimedia.org/wikipedia/commons/8/81/Superconducting_tunnel_junction.svg](https://upload.wikimedia.org/wikipedia/commons/8/81/Superconducting_tunnel_junction.svg)

  Another "downside" is that they are extremely strict about copyright compliance. This is good because you can be pretty sure that they are correct in general, but it also means that they are very conservative, and delete things where fair use would be OK. And if those fair uses have no Wikipedia page, they won't show up anywhere.
- [https://archive.org](https://archive.org) for anything else, e.g. videos that Wikimedia commons does not accept.

  All content will be tracked under the `cirosantilli` collection: [https://archive.org/details/cirosantilli](https://archive.org/details/cirosantilli)

  archive.org has a very convenient upload and lax requirements. The generated URLs are predictable (single SHA prefix for the entire collection).

  Never trust a website that is not on [GitHub Pages](../github-pages.md), for-profit companies will take down everything immediately as soon as it stops making them money.

  Every external link to non-GitHub pages must be archived. And GitHub links must be forked.

  We should also backup images that Wikimedia Commons does not accept here in addition to the [https://github.com/cirosantilli/media](https://github.com/cirosantilli/media) repository.

The following alternatives seem impossible because Ciro could not find if they expose direct links to the images:
- [Google Photos](../google-photos.md) [https://webapps.stackexchange.com/questions/92777/how-to-get-the-direct-link-to-an-image-in-my-google-photos](https://webapps.stackexchange.com/questions/92777/how-to-get-the-direct-link-to-an-image-in-my-google-photos)
- Imgur [https://webapps.stackexchange.com/questions/84535/has-imgur-stopped-giving-direct-links](https://webapps.stackexchange.com/questions/84535/has-imgur-stopped-giving-direct-links)

The following do have direct links:
- [https://www.flickr.com](https://www.flickr.com) e.g. [https://live.staticflickr.com/7437/27402357162_7d91b73cd5_z.jpg](https://live.staticflickr.com/7437/27402357162_7d91b73cd5_z.jpg) documented at [https://help.flickr.com/en_us/get-the-url-of-a-flickr-photo-S1Hnnmjym](https://help.flickr.com/en_us/get-the-url-of-a-flickr-photo-S1Hnnmjym) Also does automatic image size conversion. But only provides ugly autogenerated URLs.
- [Instagram](../instagram.md) does not support upload from computer? Lol?

For videos, [YouTube](../youtube.md) does not allow download, even of Creative Commons videos so uploading only there is not acceptable as it prevents reuse:
- [https://law.stackexchange.com/questions/8033/is-it-legal-to-download-and-modify-videos-from-youtube-licensed-under-creative-c](https://law.stackexchange.com/questions/8033/is-it-legal-to-download-and-modify-videos-from-youtube-licensed-under-creative-c)
- [https://www.quora.com/Can-I-download-Creative-Commons-licensed-YouTube-videos-to-edit-them-and-use-them](https://www.quora.com/Can-I-download-Creative-Commons-licensed-YouTube-videos-to-edit-them-and-use-them)

## ↑ Ancestors (4)

1. [Media rationale of Ciro Santilli's website](../media-rationale-of-ciro-santilli-s-website.md)
2. [cirosantilli.com](../cirosantilli-com-split.md)
3. [Ciro Santilli](../ciro-santilli-split.md)
4. [Ciro Santilli's Homepage](../split.md)
