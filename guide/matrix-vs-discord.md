---
title: Matrix vs. Discord
layout: page-two-col
nav: false
parent: guide
permalink: guide/matrix-vs-discord/
description: It's time to ditch Discord. Imagine a place where users are actually respected. Join Matrix, the federated chat platform that does exactly that.
---

## Matrix против Discord

Спасибо за выбор Matrix.

Matrix является популярной альтернативой для Discord, но многие люди не понимают почему. Мы начнём с того, почему Вы должны перейти с Discord на Matrix, затем сравннения. Давайте начнём с...

## Спор правильного значения слова "Сервер"

Вспомните компьютерное [определение](https://en.wiktionary.org/wiki/server#Noun) слова "сервера":

> 1. Программа, предоставляющяя сервисы другим программам или устройствам, в локальной или глобальной сети.
>
> 2. Компьютер, выделенный для запуска таких программ.

Определения соответствуют игровым серверам (например Minecraft), сервер созданный для общения группы людей (например Mumble и TeamSpeak), сервер, где работают боты Discord/Telegram/итд. В каждом случае, серверное ПО (как файл сервера Minecraft) соответствует определению #1, серверное оборудование (например VDS) соответствует определению #2.

Но не в случае "сервера" Discord: это просто кучка данных, вместе с другими "серверами," лежащие на серверах Discord. "Сервер" Discord - не программа, и не оборудование для "серверов,"[^14] что нарушает оба определения. Скорее это чтобы привлечь геймеров, использующие правильное понятие слова "сервер", Discord пытается приравнять это к чат-группе, загрязняя определение этого технического термина. (Следовательно Discord отсылается к "серверам" как к *гильдиям (guilds)* в документации API.)

### Что про Matrix?

В Matrix, *домашний сервер* - это сервер, поскольку он соответствует обоим определениям: Выделенная инфраструктура (определение №2) под управлением [серверного программного обеспечения](../#set-up-your-own-homeserver-or-join-an-existing-homeserver) (определение №1). Более того, эти домашние серверы, хотя и работают независимо друг от друга и не находятся под контролем одного субъекта, общаются (передают сообщения и т.п.) друг с другом по согласованному протоколу, тем самым поддерживая жизнь платформы Matrix. Платформы, использующие такую структуру, такие как Matrix, [Fediverse](https://fediverse.party/en/fediverse) и электронная почта, называются федеративными платформами.

## Почему не Discord?

Я уверен, что вы можете найти много обоснованной критики Discord, например, [здесь](https://cadence.moe/blog/2020-06-06-why-you-shouldnt-trust-discord) или [здесь](https://austinhuang.me/discord-issues). Прочитайте их, если у вас есть время.

В рамках данного руководства основными причинами для перехода с Discord на Matrix являются:

* **Недостаток конфиденциальности личных сообщений**, так как личные разговоры не только не шифруются, но и активно сканируются (масштабы этого зависят от ваших настроек, но некоторые происходят даже при отключении всех тумблеров фильтрации). [Люди сообщали](https://www.reddit.com/r/discordapp/comments/t5v3of/viruses_now_get_turned_into_recipe_links_funny/), что их сообщения были заменены кулинарными рецептами, когда они пытались отправить что-то, что Discord считает вирусом.
* **Чрезмерное отслеживание, от которого нельзя отказаться в соответствии с ToS**, например, [телеметрия](https://luna.gitlab.io/discord-unofficial-docs/science.html) и регистратор процессов (для статуса активности)[^10]. Большинство сторонних клиентов и некоторые клиентские моды не поддерживают ни телеметрию, ни обнаружение процессов. На сегодняшний день не известно ни одного пользователя, которому бы запретили не отправлять данные телеметрии.
* **Враждебная позиция по отношению к неофициальным клиентам или модификациям клиентов**, что не позволяет пользователям отказаться от некоторых раздражающих факторов или отслеживания совместимым способом.
* **Арбитражные требования к номеру телефона**. Некоторые пользователи, которые считаются подозрительными, и пользователи, которые присоединяются к определенным "серверам", обязаны подтверждать свой номер телефона.
* Discord принимает **решения, противоречащие интересам пользователей**, самыми последними из которых являются:
  * Предвзятые консультации и одностороннее предложение [криптовалютных интеграций](https://www.reddit.com/r/discordapp/comments/qpmhs5/discord_developers_please_do_not_support_nfts/) (которые были отменены только после массового протеста); и
  * Лишение доступа к чтению текстовых сообщений на "серверах" за некоторыми исключениями[^12], что фактически равносильно обязательному внедрению потока взаимодействия на основе команд приложения, а также требований KYC для запуска ботов на более чем 100 "серверах" (которые *не* были отменены, несмотря на [реакцию](https://gist.github.com/Rapptz/4a2f62751b9600a31a0d3c78100287f1)).
* **Закрытый источник**, который не может быть проверен независимо.
* **Отсутствие контроля за частными данными и отсутствие гарантий надежности**, поскольку Discord является централизованным, а не федеративным. См. [здесь](../matrix-vs-al/#centralized-platforms).
* **Более богатые возможности выражения**.[^11] Пользователь с Nitro разблокирует некоторые дополнительные возможности, в основном связанные с тем, что может быть включено в сообщение, а также в два раза больше лимит "серверов", в два раза больше лимит длины сообщения, а также размер файлов до 500МБ.
* **Не предназначено для серьезного использования**. Один из разработчиков Discord прямо сказал: "Мы просто приложение для случайного общения". Маркетинговые кампании Discord, такие как включая игровых компаний, связанных с играми, и использование забавных мемов, похоже, согласны с этой позицией.
 
[Matrix рассматривает все вышеперечисленное](../#why-matrix).

### Специальное примечание

Matrix использует свободное программное обеспечение для своих серверных и клиентских программ.

* Тем, кто использует или планирует использовать функцию Discord "Student Hub", следует обратиться в IT-отдел вашего учебного заведения или в студенческий союз с просьбой установить домашний сервер Matrix, который обеспечивает большую гибкость в общении, гарантируя при этом конфиденциальность и уважение к вашему ведомству. [Немцы уже используют его.](https://doc.matrix.tu-dresden.de/en/why/)
* Сообщества с открытым исходным кодом должны знать, что [использование Discord является противоестественным и дискриминационным](https://drewdevault.com/2021/12/28/Dont-use-Discord-for-FOSS.html).

## Терминологии

### Канал и ЛС против комнаты

В Discord, место где можно отправлять сообщения "канал" (если пренадлежит к "серверу") или ЛС.

В Matrix, место где можно отправлять сообщения, - комната.

### "Сервер" против Пространство

В Discord, текстовые каналы которые не являются ЛС (включая групповые ЛС) должны быть связаны с "сервером." Таким образом, "сервер" может быть понятен как список каналов, к которым применяются настройки сервера.

В Matrix, комнаты *могут* быть включены в пространства. Пространство может быть использовано как похожая мода к "серверу" Discord (управляются админами соответствующих комнат) или папка "серверов" (управляется кем угодно). Пространства могут включать дочерние пространства *(А что если включить пространство Б в пространство А, затем пространство А в пространство Б?)*. Комнаты не имеют общие настройки с пространствами, хотя комнаты могут требовать участие в пространстве для входа.

## Сравнения возможностей

Имейте в виду, что Matrix не (и не может) иметь платных возможности. Таким образом, любые исключения в функциях Discord, для которых требуется подписка Nitro или Nitro Classic, не рассматриваются.

| Возможность | Discord | Matrix |
| ------- | ------- | ------ |
| **Регистрация** | Требует email. Discord может потребовать номер телефона если обнаружит "подозрительную активность." | В зависимости от домашнего сервера (тем более если у Вас свой), **email может быть необязателен**, и номер телефона в больших случаях не требуется/необязателен. Здесь нет *автоматической* проверки на человечность. |
| Цена | Условно бесплатно. | Бесплатно [для многих домашних серверов](../../servers) (пожалуйста, предпочитайте донатить им). Обслуживание собственного домашнего сервера может быть платным (или [бесплатным?](https://matrix.org/docs/guides/free-small-matrix-server)). Заметьте что плата (не только донаты) только имеет разницу к месту, где находятся Ваши данные и производительность сервера; нет эффекта на возможностях. |
| **Username** | Users are identified by display name (maximum 32 characters) + discriminator (4 randomly-assigned digits) to fellow users, and user IDs (Around 18 digits) for programming purposes. | Users are identified by their MXID (eg. `@alice:example.com`), composed of the username (must be ASCII characters, upper case letters are not allowed) and the server name (not exceeding 255 characters when combined, including the introducing at symbol and the colon separating the parts). A display name can be optionally added (up to ~65200 bytes)[^7]. |
| Avatar | Static, maximum 8 MB. Cannot be zoomed unless using a bot or manually entering the URL to higher definition images, in which case the returned avatar has a maximum definition of 1024x1024. | **See "Attachments" for limits.** Can be zoomed (at least in Element/SchildiChat), in which case the avatar will be shown in the uploaded definition. Animated avatars are **supported**. |
| Profile description and background | **Supported**. | Not supported currently, will be supported using profile rooms. |
| Ability to read messages while offline | Official web and desktop clients artificially block viewing anything at all when it loses the real-time connection. No such limitation in official mobile clients. | Messages in client cache can be read without restriction. |
| Profile status | **Supported**. | Effectively not supported[^1]. |
| Nicknames[^2] | Supported. Maximum 32 characters. | **Supported** (`/myroomnick`). Up to ~65200 bytes. |
| Specific avatars[^2] | Requires Nitro. | [**Supported**](../features/#attachments) (`/myroomavatar`). See "Attachments" for limits. |
| 2FA | Email or SMS/TOTP. | Not required for login, but required (QR code, emoji verification, or Security Key) for viewing past encrypted messages. |
| **Text messages** | Maximum 2000 characters. Supports Markdown (with some modifications). | **Up to ~65200 bytes (up to ~21270 bytes if a formatted message with plain text fallback sent).[^7] [Supports Markdown and HTML.](../features/#text)** |
| Attachments | Maximum 8 MB (maximum 100 MB for users with Nitro, and also for all users in a "server" with boost tier 3). | **Maximum 50~100 MB** (for most homeservers; customizable if you run your own homeserver). |
| Custom emotes in messages | Free users can only use static emotes defined within the "server". Using emojis from outside the "server" and using animated emojis are limited to Nitro users only. | It is possible to insert user-defined static emotes in messages, see [here](../features/#attachments). No support for animated emotes. |
| Reactions | Only emotes (Unicode or custom ones) | Unicode emotes and [text](../features/#reactions). |
| Stickers | Only stickers defined within the "server". | **Unlimited with setup.** See [here](../features/#stickers). |
| Public read receipts | Not supported. | **Supported.** |
| **Direct messages** | Not encrypted. | **Encrypted by default**, including VoIP. |
| Starting a DM | Depending on privacy settings, initiating a DM requires the two users to have established "friendship" or have certain mutual "servers." Users are given the choice to accept, remove, or report a DM (since late 2021). | Initiating a DM solely requires the recipient to accept the request[^3]. Users can leave DMs anytime they wish. |
| **Group chats** | A channel is associated with a "server." You can only join 100 "servers," 200 with Nitro. | A room is standalone, but can be optionally included and associated with a Space, which is just a room linking to other rooms. You can join **unlimited** amount of rooms. |
| VoIP in groups | Supported. | Limited Support via integration with Jitsi. Expected to be replaced by a better solution during 2022. |
| Organizing chats | "Servers" can be organized into folders, but each "server" can only belong to 1 folder. Channels in a "server" can only be organized by the "server" owner and moderators with "manage channels" permission, in a many to one fashion, and cannot be moved to another "server" once created. | Rooms can be included within an unlimited amount of Spaces. Spaces may also include other Spaces (similar to Discord's channel categories). |
| Group chat privacy | Denying "View Channel History" permission prevents users from reading messages prior to their most recent login. However the "server" owners cannot enjoy that privacy, as "server" owners cannot deny their own permissions due to how Discord's permission system works. | You may deny new members from reading messages prior to them being invited / joining. You may also allow or deny guest access (such as [Matrix Static](http://view.matrix.org/)) from reading messages. You may also enable encryption[^4]. |
| Server-side deletion guarantees | Messages that are removed from Discord are garbage collected from discord.com databases within less than 2 days.[^9]  Guild messages from deleted users are mapped to the unified ghost user, including mentions to them. Direct messages stay unless explicitly closed by the counterparty. | As Matrix follows an event chain model, there is no true deletion. The closest thing available is redaction, which instructs the users and servers to blank the content but not the metadata of the event. Redactions are best-effort[^13]. |
| Publicity | Although Discord offers its own "server" discovery feature, the requirements are somewhat arbitrary, so third-party services are often used. Only "server" owners can apply to Discord's own "server" discovery directory. Third party directory services may differ. | Each homeserver has a room directory which anyone in that homeserver may publish to. |
| Invite | Through generating invite links or using an OAuth-based integration. | Through directly inviting users, or through shareable [addresses](../features/#promotion). |
| Permissions in group chats | Single-owner, up to 255 roles. How long did it take for you to learn role hierarchy?[^8] A "server" can only be shut down by its owner, and that affects everyone. Members cannot demote their own permissions. Roles of a member are reset when a member leaves hence do not survive rejoin. | Up to 2^54 power levels (-2^53 to 2^53-1, however I highly doubt you will *ever* reach that limit), with minimal permissions. A user acquires a permission if their power level is equal to or higher than the power level required for the specific permission. Rooms are not owned by any user or server, hence cannot usually forcibly be shut down without coordination. Members can demote their own permissions. Power levels of members survive leave and rejoin. |
| Size limits of group chats | 10 in group DMs, several tiers in "servers" ranging from 125 thousands to 1.5 million, subject to manual transition across those tiers.[^15] | No artificial limits, albeit current implementations do not perform well with rooms having more than a few tens of thousands of members and a few dozens of homeservers. | 
| Bans | Bans are only visible to "server" moderators. One can also see their own ban when they attempt to join a "server", but not the ban reason. | Bans are public to all members, along with the reasons. |
| Disabled and deleted account handling | Disabling an account is reversible until 2 years after disabling. Accounts that do not log in for 2 years get automatically deleted every 45 days.  Messages sent to a "server" from deleted accounts stay unless explicitly removed by somebody else. User name and user settings from deleted accounts are removed. Deleted users are coalesced to a single ghost user, with the user ID 456226577798135808. "Servers" owned by accounts shut down before November 2022 may stay. "Servers" owned by a manually deleted accounts have always been automatically shut down, so do any "servers" deleted after November 2022. | Disabling an account is usually irreversible. Users can cause their messages to be forgotten while disabling their account: in that case, their messages are not sent to further users and servers. Rooms created by disabled accounts stay. |
| **Running a bot** | Running a bot in more than 100 "servers" requires a proof of identity, similar in manner to one encountered in international borders. Selfbotting is forbidden, but this is inconsistently enforced. | You can run bots on any user accounts[^5] [^6]. Selfbotting is permitted (but be nice). |
| **Apps to access platform** | By ToS, you are only allowed to use the official Discord app (including its PTB and Canary variants). This is not enforced consistently: some modifications and some third party clients are generally tolerated, while others may be forbidden. Third party clients that do not touch certain user profile related features tend to be not caught. | Element is the main app, but [**you're welcomed to use whatever you wish**](../#what-app-should-i-use). You can even make an app yourself[^6]! |
| **Network access** | **IPv4 only**. Users and bot developers have raised this issue repeatedly, and staff stated this is not urgent at all, despite the fact that IPv4 addresses have been exhausted worldwide: "We of course care of the future of the platform however ipv4<->ipv6 connectivity is not really going away any time soon with the availability of nat64 - and there are much more important things to work on." | **Most if not all homeservers participating in the public federation have IPv4 connectivity but IPv6 connectivity varies from homeserver to homeserver.** The biggest third party identity service, [vector.im](https://vector.im), however, is IPv4-only. |


## Helpful Tips

* There is a [public bridge](https://t2bot.io/discord) that allows you to connect a Discord channel with a Matrix room. There is [another bridge that allows looking at your Discord direct messages from Matrix side](https://github.com/matrix-discord/matrix-appservice-discord), but that one requires self-hosting and more extensive setup than the public t2bot bridge.  (Although, backlinking Matrix data to Discord will reduce its privacy, so please take ethical concerns into account when using them.) 
* Your user colour is chosen by a hash function (varies by app) that takes in your MXID.

## Footnotes

[^1]: Element and SchildiChat has status available as a lab feature, but it is only visible to those who you have a DM with. Statuses are not encrypted.

[^2]: For Discord "servers" and for Matrix rooms.

[^3]: Note that Matrix has no concept of "friends" or "contacts" per se, although the DM list can serve the same purpose. However, user-based contact ignoring exists on Matrix, using two different methods. The former method prevents any and all messages from reaching the recipient, and the latter method using policy rooms hides them client-side by interpreting an ignore list. The latter method is currently only available in Element as a labs feature.

[^4]: Enabling encryption is irreversible for security reasons. Note that it is pointless to enable encryption in a public room, with one exception: the case you want to have a persistent cryptographic trail of who read the messages. Furthermore, enabling encryption means users will not see messages before their invitation (if applicable) or their entry.

[^5]: Matrix has no distinction between user and bot accounts (nor is there any dependency between the two). Unless specifically exempted by the homeserver (not needed in most cases), bots have the same ratelimit as other users. In Element and SchildiChat, the user token of an account is available by accessing "User Settings" then "Help & About." When running an autonomous bot, please be courteous and indicate to others (in username or display name) that the account is a bot. Bots that want to control other user accounts need to create an application service, which needs to be approved by an administrator of the homeserver that the bot is using.

[^6]: If your app/bot is good, then [matrix.org would love to hear from you (with the potential possibility of featuring you on their blog)!](https://matrix.to/#/#thisweekinmatrix:matrix.org)

[^7]: Limited by Matrix event size limits. The current event size limit is specified to be 65536 bytes. Formatted message size limit assuming the formatted body takes approximately twice as much as plain text body.

[^8]: May be more accurately described as ban hierarchy, as the order of roles only affect role changes, nick overrides, kicks and bans. Discord's permission system is otherwise "explicit allow wins".

[^9]: Somebody actually tried to report a message after deleting it and they got "no such message in our database" from T&S. Also backed by [Stanislav Vishnevskiy's blog post on infrastructure of Discord](https://blog.discord.com/how-discord-stores-billions-of-messages-7fa6ec7ee4c7#.fdhp3rxlo). However, deletions are basically a free-for-all matter: users (including bots) may decide to keep or repost deleted messages, and there is nothing stopping this.

[^10]: Process detection only exists in the desktop client. Somebody reverse engineered this process detection. Unlike Steam's similar process detection, this detection only sends the successfully detected games, not the list of every process running. Can be opted out by disabling the game activity detection. Science endpoint is said to drop the data server-side when the relevant toggles are disabled, however no one has verified if that toggle actually works. Hence assumed as "cannot be opted out".

[^11]: Paywalling features related to customisation and expressivity is Discord's core business model, stated repeatedly by themselves and also verified by various third party sources. See [here](https://seoaves.com/how-does-discord-make-money-the-discord-business-model/) and [here](https://moneymodels.org/business-models/how-does-discord-make-money/).

[^12]: The exception is messages that @-mention the bot user can still be seen without the message content event. As many bot developers said, this is still a band-aid and not a useful solution. Direct messages are not affected by message content intent. 

[^13]: Most Matrix servers are known to keep the pre-redaction content of the event for a week, while immediately sending the redaction instruction to their fellow users. Again, redactions are basically a free-for-all matter.

[^14]: More accurately speaking, guilds are mapped to the guild servers in a many-to-one fashion. This can easily be confirmed by "server" outages, which happen when the guild process in the respective server restarts or the guild is being migrated to another server. However, the end users still lack any control on choosing a particular guilds server instance to host a guild.

[^15]: Discord "servers" have an initial limit of 125000 members. "Server" owners can request this limit to be increased by filing a support ticket, in which case Discord engineering team looks at the activity of the guild and manually migrates it to a guilds server instance with a larger member limit. Known tiers are: 125k, 250k (beyond this tier, brand verification and/or partnering required), 500k, 1M, 1.5M.
