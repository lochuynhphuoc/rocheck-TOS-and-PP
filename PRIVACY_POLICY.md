# Privacy Policy – RoCheck

**Effective Date:** November 9, 2026  
**Last Updated:** November 9, 2026

## 1. Introduction

RoCheck ("the Bot", "we", "our", or "us") is a Discord bot that provides Roblox group membership checks, Robux price calculations, server utilities, and a feedback feature.

This Privacy Policy explains what information the Bot receives or processes, why it is used, where it may be stored or shared, and what choices are available to users and Discord server administrators.

By using RoCheck, you acknowledge the processing described in this Policy. If you do not agree, do not interact with the Bot. Server administrators who invite or configure RoCheck should make this Policy available to their members.

This Policy should be read together with the [RoCheck Terms of Service](./TOS.md).

## 2. Information We Process

The information processed depends on how the Bot is used and which features are enabled.

### 2.1 Discord account and server information

The Bot may receive or process:

- Discord user IDs and usernames, to identify users who issue commands, run checks, interact with menus, or submit feedback.
- Discord server (guild) IDs and names, and channel IDs and names, to identify where an interaction or request originated.
- Message IDs and timestamps, where needed to respond to, manage, or log an interaction.
- Role IDs and channel IDs selected by server administrators when configuring the Bot.
- Server invite codes, where an invite is created or saved for operational support and log access.

### 2.2 Message and interaction information

The Bot receives new Discord server message events while it is present in a server and has the required Discord access. It processes message content to recognize supported prefix commands, direct mentions used for supported features, and requests in the configured group-check and price-check channels.

For group checks, the Bot reads the submitted Roblox username or user ID. For price calculations, it reads the amount or Robux value submitted by the user. The Bot does not intentionally fetch or store a complete historical archive of server messages.

Raw message content is generally handled to process the relevant command or request rather than stored as a permanent message-history record. However, command names and supplied command arguments may appear in operational logs. Feedback submitted through the feedback feature is stored and forwarded as described in Section 4.

Depending on the workflow, the Bot may delete messages in configured channels, such as messages associated with temporary errors or channel-specific processing. This depends on the Bot's permissions and implementation.

### 2.3 Roblox information

When a user requests a group check, the Bot may process:

- Roblox usernames and Roblox user IDs.
- Roblox group IDs, names, and available group metadata.
- Group membership status and membership/join dates returned by Roblox.
- Group verification status, when available.
- Calculated waiting periods and estimated eligibility results. The current group-check logic uses a 14-day threshold for ordinary groups and a 4-day threshold for verified groups; these are informational estimates, not guarantees of payout eligibility.
- Roblox profile, group, avatar, and avatar-item information needed to display the result.

The Bot uses Roblox services and an operator-configured Roblox Open Cloud API key to retrieve relevant information. The Bot does not request Roblox account passwords, session cookies, or login credentials from users.

### 2.4 Configuration and operational records

The Bot stores configuration and operational records needed to provide its features. These may include:

- Server-specific group lists.
- Group-check and price-check channel settings.
- Cooldown and language settings.
- Bot manager role settings.
- Robux price rates configured by server administrators.
- Bot presence, maintenance, and logging preferences.
- Cached Roblox group names and verification metadata.
- Daily group-check statistics, including Roblox user IDs used to count unique Roblox accounts.
- Feedback session status and submitted feedback information.
- Technical error details and timestamps.

### 2.5 Technical information and logs

Operational logs may include Discord usernames and IDs, server and channel names and IDs, command names and arguments, interaction details, Roblox user IDs or profile links associated with an error, timestamps, and error messages or codes.

Logs are used for service operation, debugging, abuse prevention, and support. The Bot's log categories may be enabled or disabled by the Bot operator. Disabling a category prevents the corresponding application log from being sent through that logging feature, but does not remove records already delivered to Discord or retained by infrastructure providers.

## 3. How We Use Information

We use information for purposes directly related to operating and maintaining RoCheck, including:

- Recognizing supported commands, mentions, and requests.
- Looking up Roblox accounts and group membership information.
- Displaying membership status and estimated waiting periods.
- Calculating Robux and currency amounts using rates configured by each Discord server.
- Saving server configuration and group metadata.
- Maintaining cooldowns, preventing repeated or abusive requests, and limiting feedback submissions.
- Maintaining daily usage statistics.
- Receiving, reviewing, and responding to user feedback.
- Diagnosing errors, monitoring service health, and investigating misuse or security issues.
- Providing support and maintaining the Bot.

We do not use message content or Roblox lookup information for advertising or behavioral profiling. The Bot operator does not use this information to train AI or machine-learning models.

## 4. Feedback Submissions

RoCheck provides a feedback command. When a user opens a feedback session and submits a message, the Bot processes and forwards the following information to a designated private Discord channel used by the Bot operator:

- The feedback text.
- The sender's Discord username and user ID.
- The originating Discord server's name and ID.
- The originating channel's name and ID.
- The submission timestamp.

Feedback text is subject to a 4,000-character limit. A user may submit up to five feedback sessions within a one-hour period. An unused feedback session expires after 30 minutes.

The feedback session and submitted feedback record in the Bot's database are scheduled for automatic expiration at the session's original 30-minute expiry time. Database expiry processing may not happen at the exact second. A copy forwarded to the designated Discord channel is a separate Discord message and may remain there until it is deleted by the channel's authorized moderators or administrators, subject to Discord's own systems and retention practices.

Do not include passwords, API keys, payment details, account recovery information, or other sensitive information in feedback.

## 5. Data Storage and Retention

RoCheck uses MongoDB to store configuration and operational data. The Bot operator may also use hosting infrastructure and Discord channels for application logs and feedback delivery.

Retention depends on the type of information:

- **Server configuration and group settings:** Retained while needed to operate the Bot for the relevant server. Some configuration records may remain in the database after the Bot leaves a server unless they are separately deleted.
- **Cached Roblox group metadata:** Retained to avoid repeatedly retrieving group information. It may remain until updated or removed as part of database maintenance.
- **Daily group-check statistics:** Roblox user IDs used for daily unique-user counts are retained for approximately seven days and then removed by the Bot's cleanup process.
- **Feedback database records:** Scheduled to expire at the feedback session's original 30-minute expiry time, subject to database expiry delays.
- **Feedback messages and application logs delivered to Discord:** Retained according to the relevant Discord channel's settings and the actions of its authorized moderators or administrators. The Bot operator may not control all copies or backups maintained by Discord.
- **Technical logs and hosting records:** Retained according to operational needs and the retention capabilities and policies of the relevant providers.

We do not intend to retain raw message histories for unrelated purposes. Exact retention of third-party copies, backups, and infrastructure records may differ from the periods described above.

## 6. Data Sharing and Third-Party Services

RoCheck relies on third-party services to operate. Depending on the feature being used, information may be transmitted to or processed by:

- **Discord:** Receives Bot messages and interactions and delivers Bot responses. Feedback and operational logs may be sent to designated Discord channels.
- **Roblox:** Receives lookup requests needed to retrieve Roblox account, group, and related public or API-accessible information.
- **MongoDB and database infrastructure:** Stores server configuration, cached group information, feedback session records, and operational statistics.
- **Hosting and infrastructure providers:** Runs the Bot and may process technical information required to maintain the service.

### Server invite links

When the Bot joins a server or performs certain support and logging operations, it may attempt to create a non-expiring Discord invite if it has the required Create Instant Invite permission. The invite code may be stored with that server's configuration and the invite link may be sent privately to the Bot operator for server access, support, or log-location purposes.

Server administrators should consider this behavior when granting invite permissions. If they do not want the Bot to create invite links, they should not grant it the Create Instant Invite permission unless that functionality is needed.

We do not sell users' personal information or share it with third parties for their advertising purposes. Third-party services process information under their own terms and privacy policies.

## 7. AI and Machine Learning

RoCheck does not include an AI conversation feature and the Bot operator does not use information processed by RoCheck to train AI or machine-learning models.

This statement concerns the Bot operator's use of RoCheck data. It does not change how Discord, Roblox, database providers, or hosting providers process information under their own policies.

## 8. User Choices and Data Requests

Users can choose not to use RoCheck, submit Roblox identifiers, or send feedback. Users who do not want a message processed should avoid using the Bot's commands, mentions, feedback feature, or designated group-check and price-check channels.

Users may contact the Bot operator to request access to or deletion of information associated with their use of RoCheck. To help locate relevant records, include the relevant Discord user ID, Roblox user ID if applicable, server name or ID, and a description of the request. Do not send passwords or account credentials.

We will review reasonable requests and take appropriate action where the information can be identified and where deletion is technically and legally possible. Some information may remain in Discord messages, third-party backups, security logs, or records that must be retained for legitimate operational or legal reasons. Server administrators may also control messages and configuration within their own servers.

Removing the Bot from a server does not necessarily delete configuration, logs, feedback messages, or other records already stored by the Bot operator or third-party services. Contact the Bot operator for a data-related request.

## 9. Data Security

We take reasonable measures intended to protect information processed by RoCheck against unauthorized access, disclosure, alteration, or destruction. Access to operational systems and credentials should be restricted to authorized persons.

No online service, network transmission, database, or electronic storage system can be guaranteed to be completely secure. Users and server administrators should not submit secrets or sensitive account credentials to the Bot.

## 10. Children's Privacy

RoCheck is a general-purpose Discord utility and is not designed to knowingly collect personal information from children in violation of applicable law or platform age requirements.

Users must meet the minimum age requirements that apply to Discord, Roblox, and their location. If a parent or guardian believes a child has provided personal information to RoCheck inappropriately, they may contact the Bot operator using the details below.

## 11. International Processing

The Bot operator may run RoCheck using database, hosting, and platform services located in countries other than the user's country of residence. As a result, information may be processed or stored internationally, subject to the terms and privacy practices of those providers and applicable law.

## 12. Changes to This Privacy Policy

We may update this Privacy Policy when RoCheck's functionality, data practices, service providers, or legal requirements change.

The updated version will be published at the same public URL. The Last Updated date at the top of this document will show when it was most recently revised. Continued use of RoCheck after an updated Policy takes effect means that the updated Policy applies to subsequent use.

## 13. Contact

For privacy questions, concerns, or data-related requests regarding RoCheck, contact:

**Bot Operator:** Huỳnh Phước Lộc  
**Contact Email:** phuocloc222005@gmail.com

---

This Privacy Policy applies to RoCheck's own information-processing activities. It does not replace the privacy policies, terms, or data practices of Discord, Roblox, MongoDB, hosting providers, or other third-party services.
