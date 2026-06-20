---
created: 2025-05-25
---
This guide explains the custom chat mechanics used on the Landfall server, including local suffixes, DM prefixes, and focus switching.

Run `/channel` in game to get more details on the available channels and information on commands.

---

## 💬 Local Chat Suffixes

Local messages are affected by their suffix, which determines their range and tone.

| Suffix   | Example Message                                   | Range (blocks) | Verb / Style  | Description                                                                                    |
| -------- | ------------------------------------------------- | -------------- | ------------- | ---------------------------------------------------------------------------------------------- |
| *(none)* | `Hello`                                           | 50             | **says:**     | Standard message, your default speaking voice.                                                 |
| `!`      | `Hello!`                                          | 75             | **exclaims:** | A bit louder and more expressive.                                                              |
| `!!`     | `Hello!!`                                         | 100            | **shouts:**   | Maximum range, loud and dramatic.                                                              |
| `*`      | `Hello*`                                          | 10             | **whispers:** | Soft-spoken, audible only nearby.                                                              |
| `$`      | `Hello$`                                          | 3              | **mutters:**  | Nearly private, intimate or secretive.                                                         |
| `+`      | `walks out of the tavern and waves. "Hi there!"+` | 50             | *Roleplay*    | An action or emote, italicized and styled. It can also include character speech inside quotes. |
| `))`     | `Hello))`                                         | 50             | **[OOC]**     | Ranged out-of-character message, prefixed appropriately.                                       |

> 💡 *These suffixes go at the **end** of your local message. No prefix is needed to use them.*

When you are just barely outside the range of message chat, you won't be able to fully comprehend the contents. The further you are, the more obfuscated it becomes.
![[chat-distorted.png]]

---

## 🧭 Chat Prefixes

To change your chat focus, use a prefix followed by a colon:

| Prefix           | Usage           | Target                                                             |
| ---------------- | --------------- | ------------------------------------------------------------------ |
| `g:`             | `g: Hello all!` | Sends a message to **global** chat                                 |
| `/msg <player>`  | `/msg Alice Hi` | Sends a **direct message** and sets focus to DM's with that player |
| `d:` *(or `/r`)* | `d: Hi there!`  | Switches focus to the sender of your most recent DM recieved.      |


> 💡 *Chat focus is persistent until changed. Sending a new DM also sets focus to that recipient. It takes a little getting used to, but is so incredibly convenient to use!*

---

## 🧠 Focus Rules Summary

- Receiving a DM updates your `/r` and `d:` target but does **not** change your current focus.
- Sending a DM with `/msg`, `/r`, or `d:` **does** change your focus.
- Messages may follow a prefix to quickly send it, for example `g: Hello global!`
- You may change your focus without sending a message by using only the prefix. For example `g:` will set your focus to general, but not send any message.