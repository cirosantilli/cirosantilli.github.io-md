# Messaging software

↑ **Parent:** [Software](software.md)

**Table of contents**

- [Messaging software that force you to have a mobile phone](#messaging-software-that-force-you-to-have-a-mobile-phone)
  - [Messaging software that force you to share your mobile phone with contacts](#messaging-software-that-force-you-to-share-your-mobile-phone-with-contacts)
- [Serverless browser P2P chat](#serverless-browser-p2p-chat)
- [Email](#email)
  - [Transactional emai provider](#transactional-emai-provider)
    - [SendGrid](#sendgrid)
  - [Plausible deniability of email password handover](#plausible-deniability-of-email-password-handover)
  - [Privacy focused email provider](#privacy-focused-email-provider)
    - [ProtonMail](#protonmail)
      - [ProtonMail asks for login every time in the browser](#protonmail-asks-for-login-every-time-in-the-browser)
      - [Proton Pass](#proton-pass)
      - [Proton VPN](#proton-vpn)
  - [List of email providers](#list-of-email-providers)
    - [Gmail](#gmail)
      - [Google Chat](#google-chat)
      - [Dots in Gmail address](#dots-in-gmail-address)
    - [Guerrilla Mail](#guerrilla-mail)
    - [Microsoft Outlook](#microsoft-outlook)
- [Instant messaging](#instant-messaging)
  - [Instant messaging vs email](#instant-messaging-vs-email)
  - [The perfect privacy messaging software features](#the-perfect-privacy-messaging-software-features)
  - [Open instant messaging protocols](#open-instant-messaging-protocols)
    - [Internet Relay Chat](#internet-relay-chat)
    - [Signal protocol](#signal-protocol)
    - [XMPP](#xmpp)
  - [List of instant messaging software](#list-of-instant-messaging-software)
    - [Bitmessage](#bitmessage)
    - [Discord (software)](#discord-software)
      - [Discord email notifications](#discord-email-notifications)
    - [Jami (software)](#jami-software)
    - [Jitsi](#jitsi)
    - [Pidgin (software)](#pidgin-software)
    - [Signal (software)](#signal-software)
      - [Signal feature](#signal-feature)
        - [List of Signal features](#list-of-signal-features)
          - [Contact people on Signal without sharing your phone number](#contact-people-on-signal-without-sharing-your-phone-number)
        - [Missing Signal feature](#missing-signal-feature)
          - [Peer to peer file transfer of arbitrary size](#peer-to-peer-file-transfer-of-arbitrary-size)
    - [Slack (software)](#slack-software)
      - [Slack clone](#slack-clone)
        - [Zulip](#zulip)
    - [Skype](#skype)
    - [Telegram (software)](#telegram-software)
    - [WhatsApp](#whatsapp)
      - [Why did Facebook buy WhatsApp?](#why-did-facebook-buy-whatsapp)
      - [WhatsApp profile information is public by default](#whatsapp-profile-information-is-public-by-default)

## Messaging software that force you to have a mobile phone

↑ **Parent:** [Messaging software](messaging-software.md)  
🏷️ **Tags:** [Evil](cirism.md#evil)

Chat programs that don't have a proper web-only operation and force you to have a mobile phone, e.g. [WhatsApp](#whatsapp).

Heck, even [Signal](#signal-software), which is supposed to be super secure and good for your privacy, forces you to disclose your freaking cell phone to all contacts! [https://lifehacker.com/how-to-use-signal-without-revealing-your-private-phone-1818996580](https://lifehacker.com/how-to-use-signal-without-revealing-your-private-phone-1818996580)

What is my phone breaks? What if I don't want to have a [fucking](biology.md#sexual-intercourse) phone? What if I move countries and have to change the [fucking](biology.md#sexual-intercourse) number? Also evil but less because done by all: chat programs that can't send you an email [if you don't see the message in X minutes](https://webapps.stackexchange.com/questions/41528/how-can-i-automatically-forward-facebook-messages-to-my-email-or-phone).

[European Union](continent.md#european-union), time to force those evil [companies](company.md) to use support open standards like [XMPP](#xmpp)?

The solution to "how to prevent spam" is simple: your ID is a public key that you own the private key for. If you start getting spammed, generate a new public key, and send it to all contacts, and dump the previous ID.

### Messaging software that force you to share your mobile phone with contacts

↑ **Parent:** [Messaging software that force you to have a mobile phone](#messaging-software-that-force-you-to-have-a-mobile-phone)

OK, you have to share your phone with the company to prevent spam which forces us into [messaging software that force you to have a mobile phone](#messaging-software-that-force-you-to-have-a-mobile-phone), but why do you also have to share your phone with contacts? So you are then forced to give your phone number away on the [Internet](computer.md#internet).

## Serverless browser P2P chat

↑ **Parent:** [Messaging software](messaging-software.md)

- [https://stackoverflow.com/questions/2463665/how-create-a-p2p-web-chat-without-any-server](https://stackoverflow.com/questions/2463665/how-create-a-p2p-web-chat-without-any-server)

It seems impossible to avoid the signaling server. With signaling server:
- [https://github.com/tom-james-watson/p2p.chat](https://github.com/tom-james-watson/p2p.chat)
- [https://github.com/OTRMan/otr.to-chat](https://github.com/OTRMan/otr.to-chat)
- maybe [Jitsi](#jitsi)

Games:
- [https://github.com/rameshvarun/netplayjs](https://github.com/rameshvarun/netplayjs)

## Email

↑ **Parent:** [Messaging software](messaging-software.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Email)

[Ciro Santilli](ciro-santilli.md)'s email can be found by cloning one of his repositories on [GitHub](software.md#github). It is also given at: [Section "How to contact Ciro Santilli"](ciro-santilli.md#contact).

### Transactional emai provider

↑ **Parent:** [Email](#email)

#### SendGrid

↑ **Parent:** [Transactional emai provider](#transactional-emai-provider)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SendGrid)

The first one [Ciro Santilli](ciro-santilli.md) managed to get working in 2022, and which has a free plan.

You can either verify your sending domain by adding 3 DNS records.

Saw the email on [Gmail](#gmail), but [Microsoft Outlook](#microsoft-outlook) did put it into junk though. Yahoo mail also worked fine.

100 emails a day is not insane, but it is forever and appropriate for a test, I'm happy with that.

### Plausible deniability of email password handover

↑ **Parent:** [Email](#email)

[https://protonmail.uservoice.com/forums/284483-feedback/suggestions/39962275-plausible-deniability](https://protonmail.uservoice.com/forums/284483-feedback/suggestions/39962275-plausible-deniability)

You need a secondary password that when used leads to an empty inbox with a setting set where message are deleted after 2 days.

This way, if the attacker sends a test email, it will still show up, but being empty is also plausible.

Of course, this means that any new emails received will be visible by the attacker, so you have to find a way to inform senders that the account has been compromised.

So you have to find a way to inform senders that the account has been compromised, e.g. a secret pre-agreed canary that must be checked each time as part of the contact protocol.

### Privacy focused email provider

↑ **Parent:** [Email](#email)

- [https://github.com/cirosantilli/cirosantilli.github.io/issues/66](https://github.com/cirosantilli/cirosantilli.github.io/issues/66)
- [https://www.privacytools.io/providers/email/](https://www.privacytools.io/providers/email/)

#### ProtonMail

↑ **Parent:** [Privacy focused email provider](#privacy-focused-email-provider)  
🏷️ **Tags:** [Good](cirism.md#good)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/ProtonMail)

One of the very few encrypted emails... beauty. And they also have an encrypted password manager!!! Using this is a must as of 2023 basically. The only missing thing now is to find a fully [open source](software.md#open-source-software) alternative!!!

Sure, search capabilities have to be somewhat limited: [https://proton.me/blog/engineering-message-content-search](https://proton.me/blog/engineering-message-content-search)

[https://techcrunch.com/2021/09/06/protonmail-logged-ip-address-of-french-activist-after-order-by-swiss-authorities/](https://techcrunch.com/2021/09/06/protonmail-logged-ip-address-of-french-activist-after-order-by-swiss-authorities/) you've fucking got to use [Tor Browser](cryptography.md#tor-browser) with it if you want your IP to remain hidden, learn that...

Their backend is closed source: [https://www.reddit.com/r/ProtonMail/comments/iyjqxf/is_protonmails_backend_open_source/](https://www.reddit.com/r/ProtonMail/comments/iyjqxf/is_protonmails_backend_open_source/)

Are daily notifications without a recovery email possible? [https://www.reddit.com/r/ProtonMail/comments/yjau8f/allow_daily_email_notifications_without_having_a/](https://www.reddit.com/r/ProtonMail/comments/yjau8f/allow_daily_email_notifications_without_having_a/) OK, they do work actually.

The lack of [Gmail dot trick](#dots-in-gmail-address) is tragic however, and you have to pay for multiple aliases. But you can however create separate inboxes with the same cell phone verification however.

##### ProtonMail asks for login every time in the browser

↑ **Parent:** [ProtonMail](#protonmail)

It is fucking annoying!

- [https://www.reddit.com/r/ProtonMail/comments/pn21dn/have_to_log_in_every_time_i_restart_the_browser/](https://www.reddit.com/r/ProtonMail/comments/pn21dn/have_to_log_in_every_time_i_restart_the_browser/)
- [https://www.reddit.com/r/ProtonMail/comments/6qwm9w/automatic_login_to_protonmail_from_browser/](https://www.reddit.com/r/ProtonMail/comments/6qwm9w/automatic_login_to_protonmail_from_browser/)
- [https://protonmail.uservoice.com/forums/945460-general-ideas/suggestions/48228635-mail-proton-me-should-automatically-login-to-last](https://protonmail.uservoice.com/forums/945460-general-ideas/suggestions/48228635-mail-proton-me-should-automatically-login-to-last)

Not just on browser close. Whenever [Ciro Santilli](ciro-santilli.md) pastes [https://proton.me/](https://proton.me/) on the browser bar and click enter. [Chromium](web-technology.md#chromium-web-browser) 123.

More precisely: pasting [https://mail.proton.me](https://mail.proton.me) on the browser bar redirects to [https://account.proton.me/switch](https://account.proton.me/switch) each time. From there, selecting different accounts leads to different [https://mail.proton.me/u/<UID>/inbox](https://mail.proton.me/u/<UID>/inbox), e.g. [https://mail.proton.me/u/41/inbox](https://mail.proton.me/u/41/inbox) is my main one. If I paste [https://mail.proton.me/u/41/inbox](https://mail.proton.me/u/41/inbox) on the browser, then it works directly.

##### Proton Pass

↑ **Parent:** [ProtonMail](#protonmail)  
🏷️ **Tags:** [Password manager](software.md#password-manager)

[https://proton.me/pass](https://proton.me/pass)

##### Proton VPN

↑ **Parent:** [ProtonMail](#protonmail)  
🏷️ **Tags:** [VPN](computer.md#virtual-private-network)

[God](religion.md#god), I love this company so much.

### List of email providers

↑ **Parent:** [Email](#email)

#### Gmail

↑ **Parent:** [List of email providers](#list-of-email-providers)  
🏷️ **Tags:** [Google product](google.md#google-product)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Gmail)

##### Google Chat

↑ **Parent:** [Gmail](#gmail)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Google_Chat)

##### Dots in Gmail address

↑ **Parent:** [Gmail](#gmail)

Ignored: [https://support.google.com/mail/answer/7436150?hl=en-GB](https://support.google.com/mail/answer/7436150?hl=en-GB)

This allows you to create multiple non-anonymous accounts on any website that doesn't account for it, as this is not part of the [email](#email) protocols in general.

#### Guerrilla Mail

↑ **Parent:** [List of email providers](#list-of-email-providers)  
🏷️ **Tags:** [Good](cirism.md#good)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Guerrilla_Mail)

OMG those devs are brutes, it's beautiful.

[https://www.guerrillamail.com/](https://www.guerrillamail.com/)

[https://github.com/flashmob/go-guerrilla](https://github.com/flashmob/go-guerrilla)

#### Microsoft Outlook

↑ **Parent:** [List of email providers](#list-of-email-providers)  
🏷️ **Tags:** [Microsoft product](microsoft.md#microsoft-product)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Microsoft_Outlook)

## Instant messaging

↑ **Parent:** [Messaging software](messaging-software.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Instant_messaging)

### Instant messaging vs email

↑ **Parent:** [Instant messaging](#instant-messaging)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Instant_messaging_vs_email)

- [https://github.com/cirosantilli/cirosantilli.github.io/issues/69](https://github.com/cirosantilli/cirosantilli.github.io/issues/69)
- [https://www.quora.com/unanswered/Why-were-protocols-like-IRC-and-XMPP-created-after-email-if-both-can-send-messages](https://www.quora.com/unanswered/Why-were-protocols-like-IRC-and-XMPP-created-after-email-if-both-can-send-messages)

### The perfect privacy messaging software features

↑ **Parent:** [Instant messaging](#instant-messaging)

Haven't found the one yet:
- [open source software](software.md#open-source-software), doh
- [end-to-end encryption](cryptography.md#end-to-end-encryption)...
- has browser frontend and [Android](systems-programming.md#android-operating-system) app
- public URL without sharing your mobile phone: [messaging software that force you to have a mobile phone](#messaging-software-that-force-you-to-have-a-mobile-phone)
- self-destroying messages (turned on by default please)
- user base large enough to give some confidence that it was reviewed for security issues
- easy/built-in setup over [Tor](cryptography.md#tor-anonymity-network)

Optional but really [ideal](science.md#idealism):
- can delete messages from the device of the person you sent it to, no matter how old
- decentralized, your username is a public key

The state of messaging is ridiculous as of 2020.

### Open instant messaging protocols

↑ **Parent:** [Instant messaging](#instant-messaging)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Open_instant_messaging_protocols)

[Internet Relay Chat](#internet-relay-chat) vs [XMPP](#xmpp): [https://stackoverflow.com/questions/4149380/whats-the-best-open-protocol-for-chat-room-software](https://stackoverflow.com/questions/4149380/whats-the-best-open-protocol-for-chat-room-software)

#### Internet Relay Chat

↑ **Parent:** [Open instant messaging protocols](#open-instant-messaging-protocols)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Internet_Relay_Chat)

#### Signal protocol

↑ **Parent:** [Open instant messaging protocols](#open-instant-messaging-protocols)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Signal_protocol)

#### XMPP

↑ **Parent:** [Open instant messaging protocols](#open-instant-messaging-protocols)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/XMPP)

### List of instant messaging software

↑ **Parent:** [Instant messaging](#instant-messaging)

#### Bitmessage

↑ **Parent:** [List of instant messaging software](#list-of-instant-messaging-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Bitmessage)

[https://github.com/Bitmessage/PyBitmessage](https://github.com/Bitmessage/PyBitmessage)

TODO evaluate. No `pip install`???

#### Discord (software)

↑ **Parent:** [List of instant messaging software](#list-of-instant-messaging-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Discord_(software))

[Ciro Santilli](ciro-santilli.md)'s discord ID: `cirosantilli#8921`. See also: [how to contact Ciro Santilli](ciro-santilli.md#contact).

You gotta be born after the year 2000 to understand it.

This is becoming more and more popular as a group chat with channels and threads possibility as of 2020.

Very similar to [Slack](#slack-software).

No user URLs? [https://support.discord.com/hc/en-us/community/posts/360041519131-UserProfilesLinks](https://support.discord.com/hc/en-us/community/posts/360041519131-UserProfilesLinks)

They force your username to have 4 random digits? [https://www.reddit.com/r/discordapp/comments/43kjdl/whats_the_number_next_to_the_username/](https://www.reddit.com/r/discordapp/comments/43kjdl/whats_the_number_next_to_the_username/)

Not possible to anonymously join just one server without creating a new account? What's the point of servers then! [https://www.reddit.com/r/discordapp/comments/6gmjl7/changing_nick_before_joining_a_new_server/](https://www.reddit.com/r/discordapp/comments/6gmjl7/changing_nick_before_joining_a_new_server/) Oh, also nicks don't hide your username from the server in any way, you can get the original username by just clicking on the person's username.

No proper threaded discussion without creating new channels? As of 2022 there is kind of a way, but it was a bit obtuse.

As of 2022 they also have a school hub: [https://support.discord.com/hc/en-us/articles/4406046651927-Discord-Student-Hubs-FAQ](https://support.discord.com/hc/en-us/articles/4406046651927-Discord-Student-Hubs-FAQ) which auto creates groups by university email access. Good idea, and shows popularity amongst that user group.

Servers don't have an ID to join them? [https://www.reddit.com/r/discordapp/comments/b9zdt6/join_discord_server_from_id/](https://www.reddit.com/r/discordapp/comments/b9zdt6/join_discord_server_from_id/)

Can only make public servers if you have 1000 members?? [https://support.discord.com/hc/en-us/articles/360023968311](https://support.discord.com/hc/en-us/articles/360023968311) Why so much bullshit?? [https://www.reddit.com/r/discordapp/comments/6jouf8/how_do_i_make_my_server_public/](https://www.reddit.com/r/discordapp/comments/6jouf8/how_do_i_make_my_server_public/)

Also asked at: [https://webapps.stackexchange.com/questions/163441/how-to-create-a-public-discord-server-that-anyone-can-join-without-an-invite](https://webapps.stackexchange.com/questions/163441/how-to-create-a-public-discord-server-that-anyone-can-join-without-an-invite)

##### Discord email notifications

↑ **Parent:** [Discord (software)](#discord-software)

Discord is useless if you want to participate in more than one large group because of this. It is impossible to get email notification for selected threads you care about.

No way to get email notifications for missed activity? [https://support.discord.com/hc/en-us/community/posts/360041806392-Can-we-get-an-email-notification-option-for-messages-](https://support.discord.com/hc/en-us/community/posts/360041806392-Can-we-get-an-email-notification-option-for-messages-)

#### Jami (software)

↑ **Parent:** [List of instant messaging software](#list-of-instant-messaging-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Jami_(software))

[Ciro Santilli](ciro-santilli.md) worked on it for a brief time in 2016, when it was still called Ring, before he got fired. :-)

The people were quite nice and the project idea is fine, Ciro hopes they succeed.

<a id="video-ring-peer-to-peer-network-for-real-time-communication-fosdem-2016-by-ciro-santilli"></a>
**[Video 1](#video-ring-peer-to-peer-network-for-real-time-communication-fosdem-2016-by-ciro-santilli). Ring - Peer to peer network for real time communication - FOSDEM 2016 by Ciro Santilli.** [Source](https://www.youtube.com/watch?v=xAyIHhbQt3A).

#### Jitsi

↑ **Parent:** [List of instant messaging software](#list-of-instant-messaging-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Jitsi)

No chat only? .... [https://community.jitsi.org/t/chat-function-only/79067](https://community.jitsi.org/t/chat-function-only/79067)

As of 2020: [end-to-end encryption](cryptography.md#end-to-end-encryption) optional and turned off as default, and marked as experimental...

Appears to be based on [XMPP](#xmpp): [https://community.jitsi.org/t/jitsi-users-is-jitsi-a-regular-xmpp-server/13211](https://community.jitsi.org/t/jitsi-users-is-jitsi-a-regular-xmpp-server/13211)

#### Pidgin (software)

↑ **Parent:** [List of instant messaging software](#list-of-instant-messaging-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Pidgin_(software))

#### Signal (software)

↑ **Parent:** [List of instant messaging software](#list-of-instant-messaging-software)  
🏷️ **Tags:** [Mathematical symbol that looks like a Greek letter but isn't](mathematics.md#mathematical-symbol-that-looks-like-a-greek-letter-but-isn-t)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Signal_(software))

Basic must haves:
- [end-to-end encryption](cryptography.md#end-to-end-encryption): yes
- [open source software](software.md#open-source-software): yes

Other cool stuff:
- sealed sender: [https://signal.org/blog/sealed-sender/](https://signal.org/blog/sealed-sender/) Nice!

TODO what's the fucking official discussion/feature request forum?
- [https://community.signalusers.org](https://community.signalusers.org) appears to be the de-facto non-official one.
- [https://github.com/signalapp/Signal-Android/issues/5372](https://github.com/signalapp/Signal-Android/issues/5372)
- [https://whispersystems.discoursehosting.net](https://whispersystems.discoursehosting.net)
- [https://github.com/signalapp/Signal-Desktop/issues/1318](https://github.com/signalapp/Signal-Desktop/issues/1318) closes and points to discoursehosting
- [https://github.com/signalapp/Signal-Desktop/issues/549](https://github.com/signalapp/Signal-Desktop/issues/549)
- [https://www.reddit.com/r/signal/comments/lipo6z/community_signal_forum_vs_reddit/](https://www.reddit.com/r/signal/comments/lipo6z/community_signal_forum_vs_reddit/) gives some good history, says they pay for [https://community.signalusers.org/](https://community.signalusers.org/) and have admin powers there.

Feature overview:
- [https://security.stackexchange.com/questions/139493/is-signal-still-more-secure-than-whatsapp](https://security.stackexchange.com/questions/139493/is-signal-still-more-secure-than-whatsapp)

##### Signal feature

↑ **Parent:** [Signal (software)](#signal-software)

###### List of Signal features

↑ **Parent:** [Signal feature](#signal-feature)

###### Contact people on Signal without sharing your phone number

↑ **Parent:** [List of Signal features](#list-of-signal-features)  
🏷️ **Tags:** [Messaging software that force you to share your mobile phone with contacts](#messaging-software-that-force-you-to-share-your-mobile-phone-with-contacts)

This is a deal breaker for online acquaintances:
- [https://security.stackexchange.com/questions/231637/signal-contact-people-or-have-people-contact-me-without-revealing-phone-numbe/245665#245665](https://security.stackexchange.com/questions/231637/signal-contact-people-or-have-people-contact-me-without-revealing-phone-numbe/245665#245665)
- [https://community.signalusers.org/t/have-option-to-set-up-username/8723](https://community.signalusers.org/t/have-option-to-set-up-username/8723)
- [https://www.reddit.com/r/signal/comments/8kybil/is_signal_ever_going_to_include_usernames/](https://www.reddit.com/r/signal/comments/8kybil/is_signal_ever_going_to_include_usernames/)
- [https://community.signalusers.org/t/usernames-lets-throw-phone-numbers-in-the-dustbin-of-history/7282](https://community.signalusers.org/t/usernames-lets-throw-phone-numbers-in-the-dustbin-of-history/7282)
- remove need for phone completely:
  - [https://community.signalusers.org/t/a-proposal-for-alternative-primary-identifiers/3023](https://community.signalusers.org/t/a-proposal-for-alternative-primary-identifiers/3023)
  - [https://community.signalusers.org/t/remove-the-need-for-a-mobile-phone/1543](https://community.signalusers.org/t/remove-the-need-for-a-mobile-phone/1543)
  - [https://community.signalusers.org/t/registering-with-an-email-address/919](https://community.signalusers.org/t/registering-with-an-email-address/919)
  - [https://community.signalusers.org/t/username-id-registration-without-phone-number/9800](https://community.signalusers.org/t/username-id-registration-without-phone-number/9800)
  - [https://community.signalusers.org/t/more-reasons-why-signal-should-ditch-phone-numbers-the-guardian-confirmed-the-identity-of-those-in-the-chat-by-cross-checking-phone-numbers-attached-to-the-signal-accounts/7311](https://community.signalusers.org/t/more-reasons-why-signal-should-ditch-phone-numbers-the-guardian-confirmed-the-identity-of-those-in-the-chat-by-cross-checking-phone-numbers-attached-to-the-signal-accounts/7311)
  - [https://community.signalusers.org/t/why-is-phone-and-phone-number-required/1425](https://community.signalusers.org/t/why-is-phone-and-phone-number-required/1425) [https://community.signalusers.org/t/what-is-the-technical-reason-that-i-cannot-use-signal-without-a-phone-number-and-that-i-cannot-use-signal-desktop-without-signal-on-my-phone/11400](https://community.signalusers.org/t/what-is-the-technical-reason-that-i-cannot-use-signal-without-a-phone-number-and-that-i-cannot-use-signal-desktop-without-signal-on-my-phone/11400)
Beta February 2024: [https://signal.org/blog/phone-number-privacy-usernames/](https://signal.org/blog/phone-number-privacy-usernames/)

###### Missing Signal feature

↑ **Parent:** [Signal feature](#signal-feature)

- [Tor](cryptography.md#tor-anonymity-network) routing by default:
  - [https://community.signalusers.org/t/use-the-built-in-tor-project-in-the-program-source/26291](https://community.signalusers.org/t/use-the-built-in-tor-project-in-the-program-source/26291)
- option to enable disappearing messages by default:
  - [https://community.signalusers.org/t/ability-to-set-your-own-default-timer-for-disappearing-messages-on-all-new-conversations/5144](https://community.signalusers.org/t/ability-to-set-your-own-default-timer-for-disappearing-messages-on-all-new-conversations/5144) "Ability to set your own default timer for disappearing messages on all new conversations"
  - [https://www.reddit.com/r/signal/comments/jhknuz/default_disappearing_messages_timeout_for_new/](https://www.reddit.com/r/signal/comments/jhknuz/default_disappearing_messages_timeout_for_new/)
- messages are not encrypted on desktop via the [password manager](software.md#password-manager)!?!?
  - [https://github.com/signalapp/Signal-Desktop/issues/549](https://github.com/signalapp/Signal-Desktop/issues/549)
  - [https://github.com/signalapp/Signal-Desktop/issues/1318](https://github.com/signalapp/Signal-Desktop/issues/1318)
  - [https://www.reddit.com/r/privacy/comments/fwux29/signal_desktop_stores_the_encryption_key_in_a/](https://www.reddit.com/r/privacy/comments/fwux29/signal_desktop_stores_the_encryption_key_in_a/)
  - [https://whispersystems.discoursehosting.net/t/improve-security-of-desktop-apps-encryption-of-data-at-rest/26494](https://whispersystems.discoursehosting.net/t/improve-security-of-desktop-apps-encryption-of-data-at-rest/26494)
  - [https://community.signalusers.org/t/why-cant-we-lock-the-desktop-app-with-a-password/1383](https://community.signalusers.org/t/why-cant-we-lock-the-desktop-app-with-a-password/1383)
- web client:
  - [https://security.stackexchange.com/questions/238011/why-is-there-no-web-client-for-signal](https://security.stackexchange.com/questions/238011/why-is-there-no-web-client-for-signal)
- secure anti-forensic [data erasure](software.md#data-erasure) to attain [plausible deniability](software.md#plausible-deniability) of disappearing messages:
  - [https://www.reddit.com/r/signal/comments/ki5mbn/how_well_does_signal_delete_old_messages/](https://www.reddit.com/r/signal/comments/ki5mbn/how_well_does_signal_delete_old_messages/)
  - [https://community.signalusers.org/t/is-deleting-secure-in-its-current-form/908](https://community.signalusers.org/t/is-deleting-secure-in-its-current-form/908)
  - [https://community.signalusers.org/t/traces-of-messages-that-have-disappeared/5049](https://community.signalusers.org/t/traces-of-messages-that-have-disappeared/5049)

###### Peer to peer file transfer of arbitrary size

↑ **Parent:** [Missing Signal feature](#missing-signal-feature)

- [https://www.reddit.com/r/signal/comments/yzu244/allow_for_peer_to_peer_file_transfer_of_arbitrary/](https://www.reddit.com/r/signal/comments/yzu244/allow_for_peer_to_peer_file_transfer_of_arbitrary/)
- [https://www.reddit.com/r/signal/comments/qoqooh/sending_large_files/](https://www.reddit.com/r/signal/comments/qoqooh/sending_large_files/)

#### Slack (software)

↑ **Parent:** [List of instant messaging software](#list-of-instant-messaging-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Slack_(software))

##### Slack clone

↑ **Parent:** [Slack (software)](#slack-software)

###### Zulip

↑ **Parent:** [Slack clone](#slack-clone)

#### Skype

↑ **Parent:** [List of instant messaging software](#list-of-instant-messaging-software)  
🏷️ **Tags:** [Voice over IP](telecommunication.md#voice-over-ip)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Skype)

#### Telegram (software)

↑ **Parent:** [List of instant messaging software](#list-of-instant-messaging-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Telegram_(software))

Not [end-to-end encrypted](cryptography.md#end-to-end-encryption) by default, WTF... you have to create "secret chats" for that:
- [https://www.quora.com/Why-does-Telegram-not-use-end-to-end-encryption-by-default-so-that-there-are-not-keys-to-give-to-the-government](https://www.quora.com/Why-does-Telegram-not-use-end-to-end-encryption-by-default-so-that-there-are-not-keys-to-give-to-the-government)

You can't sync secret chats across devices, [Signal](#signal-software) handles that perfectly by sending E2EE messages across devices:
- [https://www.reddit.com/r/Telegram/comments/7hx8vd/when_will_telegram_get_secret_chats_crossdevices/](https://www.reddit.com/r/Telegram/comments/7hx8vd/when_will_telegram_get_secret_chats_crossdevices/)
This is a deal breaker because Ciro needs to type with his keyboard.

Desktop does not have secret chats: [https://www.reddit.com/r/Telegram/comments/9beku1/telegram_desktop_secret_chat/](https://www.reddit.com/r/Telegram/comments/9beku1/telegram_desktop_secret_chat/) This is likey because it does not store chats locally, it just loads from [server](computer.md#server-computing) every time as of 2019: [https://www.reddit.com/r/Telegram/comments/baqs63/where_are_chats_stored_on_telegram_desktop/](https://www.reddit.com/r/Telegram/comments/baqs63/where_are_chats_stored_on_telegram_desktop/) just like the web version. So it cannot have a private key.

Allows you to register a public username and not have to share phone number with contacts: [https://telegram.org/blog/usernames-and-secret-chats-v2.](https://telegram.org/blog/usernames-and-secret-chats-v2.)

Has [Reproducible builds](software.md#reproducible-builds) on Android and iOS: [https://core.telegram.org/reproducible-builds](https://core.telegram.org/reproducible-builds) 

Self deleting messages added to secret chats in Q1 2021: [https://telegram.org/blog/autodelete-inv2](https://telegram.org/blog/autodelete-inv2)

Can delete messages from the device of the person you sent it to, no matter how old.

#### WhatsApp

↑ **Parent:** [List of instant messaging software](#list-of-instant-messaging-software)  
🏷️ **Tags:** [Messaging software that force you to have a mobile phone](#messaging-software-that-force-you-to-have-a-mobile-phone)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/WhatsApp)

Claimed to remove metadata from servers unless [legally](law.md) obliged to collect it: [https://www.quora.com/Does-WhatsApp-store-messages-on-its-servers-or-is-all-deleted-after-delivery-and-only-stored-on-recipients-phones/answer/Ciro-Santilli](https://www.quora.com/Does-WhatsApp-store-messages-on-its-servers-or-is-all-deleted-after-delivery-and-only-stored-on-recipients-phones/answer/Ciro-Santilli)

They've had a few breaches: [https://www.whatsapp.com/security/advisories/](https://www.whatsapp.com/security/advisories/)

They claim to delete metadata: [https://www.quora.com/Does-WhatsApp-store-messages-on-its-servers-or-is-all-deleted-after-delivery-and-only-stored-on-recipients-phones/answer/Ciro-Santilli](https://www.quora.com/Does-WhatsApp-store-messages-on-its-servers-or-is-all-deleted-after-delivery-and-only-stored-on-recipients-phones/answer/Ciro-Santilli)

<a id="video-whatsapp-founder-jan-koum-talks-about-their-journey-by-roots-2017"></a>
**[Video 2](#video-whatsapp-founder-jan-koum-talks-about-their-journey-by-roots-2017). WhatsApp founder Jan Koum talks about their Journey by Roots (2017)** [Source](https://www.youtube.com/watch?v=X4YsJt4rIOI). Good talk, explains how everything happened in the perfect location at the perfect time: unemployed people who knew how to code, bought an iPhone, the next big platform, at its very beginning, they had just release the required push notifications [API](software.md#application-programming-interface), and he travelled a lot and knew how much SMS sucked, especially international.

##### Why did Facebook buy WhatsApp?

↑ **Parent:** [WhatsApp](#whatsapp)

Obviously with the single intention of killing a competitor.

It is impossible to make money off WhatsApp as it is because of [end-to-end encryption](cryptography.md#end-to-end-encryption).

Facebook just clearly bought it to prevent it from actually growing further and killing facebook.

It is mindblowing that the sale wasn't cancelled due to anti trust.

The outcome of this is that WhatApp will remain with the same feature set forever, while other competitors have been growing, notably [Discord](#discord-software) and [Slack](#slack-software).

It seems that there is a case looming 10 years after the fact: [https://www.cityam.com/facebook-fails-to-block-antitrust-lawsuit-over-whatsapp-and-instagram-ownership/](https://www.cityam.com/facebook-fails-to-block-antitrust-lawsuit-over-whatsapp-and-instagram-ownership/) Wake up???

##### WhatsApp profile information is public by default

↑ **Parent:** [WhatsApp](#whatsapp)  
🏷️ **Tags:** [Privacy](software.md#privacy)

Your profile picture, name and status are public by default as of 2022!!! OMG!!!

This means that all secret services in the world have alrady scraped this information for everyone that uses WhatsApp!!!

They just have to go incrementally through the list of all phone numbers... 001 0000 0000, 001 0000 0001, 001 0000 0002, etc. and then you can deduce who has which phone number.

OMG... it is analogous to the [Facebook profile face dump](ciro-santilli-s-projects.md#facebook-profile-face-dump).

Sure, it is forbidden in theory: [https://faq.whatsapp.com/general/security-and-privacy/about-harvesting-personal-information/](https://faq.whatsapp.com/general/security-and-privacy/about-harvesting-personal-information/).

## ↑ Ancestors (6)

1. [Software](software.md)
2. [Computer](computer.md)
3. [Information technology](technology.md#information-technology)
4. [Area of technology](technology.md#area-of-technology)
5. [Technology](technology.md)
6. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (1)

- [Governments should provide basic Internet infrastructure](cirism.md#governments-should-provide-basic-internet-infrastructure)
