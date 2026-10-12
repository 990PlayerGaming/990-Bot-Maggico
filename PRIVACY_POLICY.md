# Privacy Policy — 990 Bot Maggico

Last updated: October 12, 2026

## 1. Who operates the Bot

990 Bot Maggico (the “Bot”) is operated by its owner (the “Operator”). Contact for privacy questions and requests: **luca@daniel-iosipescu.dev**.

Before publication, the Operator must insert their legal name or legal entity here: **[Operator's legal name]**. This identifies the person or entity responsible for the processing described below.

## 2. Privacy approach and scope

The Bot does not ask users to register a separate account or provide real names, email addresses, passwords, or payment details. The reviewed implementation contains no advertising, sale of user data, or general-purpose user analytics.

Its initial settings are supplied by the Operator before startup. However, the Bot also processes Discord interactions, saves limited operational state, retrieves information for configured Steam profiles, and can create screenshots and logs during operation. Consequently, its data is not limited to information already present at startup.

This Policy describes the reviewed implementation in `main.py`, `minecraft.py`, and `steam_library.py`. Discord, Steam, and separately operated Minecraft servers have their own processing practices and policies.

## 3. Information processed and why

### Operator-provided configuration

Configuration includes the Bot token, owner/server/channel identifiers, local paths, Minecraft server settings and addresses, and optional Steam API credentials and Steam profile identifiers. These settings connect the Bot to authorized services, route notifications, and enforce owner checks. Credentials are service secrets and are not requested from ordinary users.

### Discord commands and connection data

Discord provides information needed to receive and answer commands, including user identifiers, command arguments, and server/channel context. The Bot uses user identifiers for owner checks, server-start tracking, and user mentions in responses.

The current implementation enables all Discord gateway intents. Depending on Discord permissions and enabled privileged intents, the library may receive or temporarily cache broader server, member, presence, and message information. The reviewed command handlers do not implement a general message-history archive or user profiling. Enabling broad intents does not mean the Bot receives only command data.

### Saved Minecraft preferences and runtime state

The Bot stores a Discord user ID together with that user's last selected Minecraft server in `last_server_by_user.json`, so `/start-server` can reuse the selection. That file also stores a global last-started-server value. Runtime memory tracks which user started a server and the running server processes. Server configuration can be updated with newly added servers and measured startup times.

Minecraft console commands supplied by the owner are forwarded to the selected server. The server may retain them under its own logging settings. Separate Minecraft server logs, player identifiers, and connection IP addresses are outside the Bot's own local preference storage.

### Steam information

If enabled, the Bot queries Steam's API for only the Steam IDs configured by the Operator. It retrieves readable game-library information and display names, stores game application IDs by Steam ID in `steam-library-state.json`, and posts detected additions to the configured Discord channel. This state prevents duplicate notifications. Private or unreadable libraries are skipped. The Operator should configure monitoring only for profiles whose owners have authorized it.

### Screenshots, notifications, and logs

The owner-only screenshot command captures the host computer's screen, temporarily saves the image locally, and uploads it to Discord. Local automation can also supply image files for posting to a configured channel. These images may include personal information visible on the host screen; the Bot does not redact them automatically.

Operational logs record startup, errors, delivery results, server or Steam activity, and related diagnostic information. Depending on the error or event, logs may include identifiers, display names, paths, or API request details. Command inputs and responses can also remain in Discord according to Discord's practices and channel visibility.

## 4. Purposes and legal basis

Information is used to provide requested commands, enforce access restrictions, remember server selections, operate configured integrations, and diagnose failures. It is not used for advertising or automated decisions producing legal or similarly significant effects.

Where the GDPR applies, the Operator must identify and document the appropriate legal basis for each activity before publication. The intended basis for essential command handling, preferences, and security diagnostics is legitimate interests in operating the requested community utility, subject to users' rights and a balancing assessment. Optional Steam monitoring should be based on the monitored person's informed consent. Consent can be withdrawn by contacting the Operator to remove the profile from monitoring. Accepting the Terms does not itself constitute consent to every processing activity.

## 5. Sharing and visibility

The Bot sends responses, notifications, and uploaded images to Discord. Channel content is visible to people who can access that channel. Steam receives API requests for configured profiles; Minecraft servers receive forwarded console commands. The Operator can access files and logs on the host computer. The reviewed implementation does not send these local files to an analytics or advertising provider.

Discord and Steam process information under their own policies, which may include processing outside your country. See [Discord's Privacy Policy](https://discord.com/privacy) and [Steam's Privacy Policy](https://store.steampowered.com/privacy_agreement/). Transfers arranged separately by the Operator, including any hosting or backups, must be described before publication if applicable.

## 6. Storage and retention

Configuration, saved user/server selections, and Steam state are held in local files on the host computer. The implementation has no automatic expiration for saved preferences or Steam state: they remain until the Operator deletes or replaces them. In-memory server ownership lasts for the running session or until the tracked server is stopped or removed from runtime tracking.

The main Bot log is opened in overwrite mode at startup. Other diagnostic or external server logs may have different retention behavior. The Operator must specify a maximum retention period for those logs before publication: **[diagnostic-log retention period]**.

Screenshot files are deleted locally after successful sending in the implemented screenshot paths. A failed operation can leave a file behind; there is no guaranteed automatic cleanup period for such failures. The Operator must establish and state that cleanup period: **[failed-screenshot cleanup period]**. Local deletion does not delete Discord's uploaded copy or copies downloaded by recipients.

Removing the Bot from a Discord server does not automatically erase local files. The Operator should remove personal state when it is no longer needed, including when a monitored profile is removed or a valid deletion request is fulfilled.

## 7. Your choices and rights

You may stop using the Bot, ask administrators to restrict its access, and contact **luca@daniel-iosipescu.dev** to request access, correction, or deletion of information associated with your Discord or configured Steam identifier. The Bot currently has no self-service deletion command. Provide only the identifier needed to locate the relevant record; never send passwords or tokens.

Where applicable, you may also have rights to restrict processing, object to processing based on legitimate interests, request portability, withdraw consent, and complain to your local data-protection authority. Requests will be assessed under applicable law, and proportionate identity verification may be necessary. Withdrawal does not affect processing lawfully carried out before withdrawal. Requests concerning Discord's or Steam's own records must be directed to those providers.

## 8. Security and changes

The Bot uses owner-ID checks for sensitive commands. The Operator is responsible for protecting the host, configuration credentials, local state, and channel access. The reviewed implementation does not provide application-level encryption for its local JSON files or logs.

This Policy must be updated if features or processing practices change. Material updates should be published where users can access them, with a revised date. For questions or suspected disclosure of information, contact **luca@daniel-iosipescu.dev**.
