# Send free emails from Heroku

↑ **Parent:** [Heroku](heroku.md)

Arghh, why so hard... tested 2021:
- [SendGrid](sendgrid.md): this one is the first one I got working on free tier!
- Mailgun: the Heroku add-on creates a free plan. This is smaller than the flex plan and does not allow custom domains, and is not available when signing up on mailgun.com directly: [https://help.mailgun.com/hc/en-us/articles/203068914-What-Are-the-Differences-Between-the-Free-and-Flex-Plans-](https://help.mailgun.com/hc/en-us/articles/203068914-What-Are-the-Differences-Between-the-Free-and-Flex-Plans-) And without custom domains you cannot send emails to anyone, only to people in the 5 manually whitelisted list, thus making this worthless. Also, gmail is not able to verify the DNS of the sandbox emails, and they go to spam.

  Mailgun does feel good otherwise if you are willing to pay. Their Heroku integration feels great, exposes everything you need on environment variables straight away.
- CloudMailin: does not feel as well developed as Mailgun. More focus on receiving. Tried adding TXT xxx.\_domainkey.ourbigbook.com and CNAME mta.ourbigbook.com entires with custom domain to see if it works, took forever to find that page... [https://www.cloudmailin.com/outbound/domains/xxx](https://www.cloudmailin.com/outbound/domains/xxx) Domain verification requires a bit of human contact via email.

  They also don't document their Heroku usage well. The envvars generated on Heroku are useless, only to login on their web UI. The send username and password must be obtained on their confusing web ui.

## ↑ Ancestors (11)

1. [Heroku](heroku.md)
2. [Platform as a service](platform-as-a-service.md)
3. [Type of cloud computing](type-of-cloud-computing.md)
4. [Cloud computing](cloud-computing.md)
5. [Computer form factor](computer-form-factor.md)
6. [Computer hardware](computer-hardware-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)
