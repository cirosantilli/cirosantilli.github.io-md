# Email verification and reCAPTCHA signup protection

↑ **Parent:** [Advances](advances.md)

<a id="_3"></a>
Added this basic but fundamental protection layer to the website.

<a id="_4"></a>
The email setup will of course be reused when notifications are eventually implemented.

<a id="_5"></a>
Currently using [SendGrid](../../../sendgrid.md) as the email provider. Very easy to setup, and has a free plan.

<a id="_6"></a>
Adding [reCAPTCHA](../../../recaptcha.md) immediately after email is a must otherwise an attacker could send infinitely many emails to random addresses, which would lead to the domain being marked as spam. I was pleasantly surprised about how easy the integration ended up being.

## ↑ Ancestors (7)

1. [Advances](advances.md)
2. [Ourbigbook.com](ourbigbook-com.md)
3. [Ciro's Edict \#7](../7-split.md)
4. [Sponsor updates](../../../sponsor-updates.md)
5. [Update from Ciro Santilli](../../../update-from-ciro-santilli.md)
6. [Ciro Santilli](../../../ciro-santilli-split.md)
7. [Ciro Santilli's Homepage](../../../split.md)

## ← Incoming links (1)

- [Article size and count limits](../8/article-size-and-count-limits.md)
