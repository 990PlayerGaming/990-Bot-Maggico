# Terms of Service — 990 Bot Maggico

Last updated: October 12, 2026

## 1. Scope and contact

These Terms govern your use of 990 Bot Maggico (the “Bot”), a Discord bot operated by its owner (the “Operator”). For support, questions, or reports of misuse, contact **luca@daniel-iosipescu.dev**. Personal-data handling is described in [the Privacy Policy](PRIVACY_POLICY.md).

## 2. Purpose and features

The Bot provides utilities for a configured Discord community and the Operator's computer and game servers. Depending on configuration and availability, it can:

- Display Minecraft server addresses and status through `/ip-server` and `/server-status`.
- Start and stop configured Minecraft servers through `/start-server` and `/stop-server`, and remember a user's last selected server.
- Allow the configured owner to execute Minecraft console commands with `/execute` and add server configurations with `/add-server`.
- Allow the configured owner to request a screenshot of the host computer with `/screen` or schedule its shutdown with `/shutdown`.
- Send screenshots and notifications supplied by a local automation process to a configured Discord channel.
- Check explicitly configured Steam profiles and announce newly detected library additions in a configured channel.

The Bot is a community utility and is not affiliated with or endorsed by Discord, Valve, Mojang, Microsoft, or Roblox.

## 3. Eligibility and access

You must meet Discord's minimum-age requirements for your country and comply with [Discord's Terms of Service](https://discord.com/terms) and the rules of the server where you use the Bot. Use the Bot only where the server administrators and the Operator have authorized its use. Installing the Bot requires appropriate Discord server permissions and the Operator's configuration.

Commands may be restricted by Discord permissions, configuration, or owner checks. Sensitive host-computer and configuration commands are intended for the configured owner. Availability of a command does not authorize you to control resources without the relevant owner's permission.

## 4. Acceptable use

Use commands only for their intended purposes and only on resources you are authorized to access. Do not bypass access controls, exploit defects, overload the Bot, repeatedly disrupt servers, send malicious commands, expose credentials or confidential material, or use the Bot for harassment or unlawful activity. Report suspected vulnerabilities privately using the contact above.

Do not submit passwords, authentication tokens, payment information, or other sensitive personal information in commands. Authorized screenshot users must check what is visible on the host screen before requesting or distributing an image. A screenshot can contain private information and may be delivered to Discord.

## 5. Practical operation and risks

Use Discord's available slash commands and supply a configured server name where required. Omitting the server in `/start-server` may use your saved last selection. Availability depends on the host computer, network, server configuration, and external services. Startup estimates and status checks are informational and may be inaccurate.

Starting a server consumes host resources. Stopping a server can forcibly terminate its process and may interrupt players or lose unsaved progress. Host shutdown interrupts services running on the computer. Back up important server data before relying on remote controls.

Responses, server addresses, Steam notifications, and automation screenshots may be visible to people with access to the receiving channel. Some owner-command responses are intended to be ephemeral; do not assume every response is private.

Steam monitoring applies only to profiles explicitly configured by the Operator and readable through Steam's API. It does not unlock private profiles. The first successful check establishes a baseline; later checks may announce newly detected games, including changes that occurred while the Bot was offline.

## 6. Availability, changes, and suspension

The Bot is provided as available, without a guarantee of uninterrupted operation, successful command execution, or continued support. The Operator may update features, restrict access, suspend misuse, or discontinue the Bot. No service fee or payment feature is implemented in the reviewed Bot version; any future paid service would require separate terms.

To the extent permitted by applicable law, the Operator does not guarantee fitness for a particular purpose and is not responsible for losses caused by outages, misuse, third-party failures, or server interruptions. Nothing in these Terms excludes liability or rights that applicable law does not allow to be excluded.

## 7. Ending use and updates to these Terms

You may stop using the Bot at any time. Server administrators may remove it or revoke its permissions. Removal does not automatically delete local state or messages already sent to Discord; contact the Operator about personal-data requests.

Material changes to these Terms should be made available through the same location where these Terms are published, with an updated date, before they apply to future use. These Terms do not replace applicable mandatory law or the terms of the platforms used by the Bot.
