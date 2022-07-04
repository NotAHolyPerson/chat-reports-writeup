# Chat Reports Writeup
What are chat reports? How do I secure my server and myself from it?

# Part I: What are chat reports and why do they exist?
Chat Reports are a feature made by Microsoft in order to globally moderate servers and make them more "PG".<br>
Essentially, it allows people's chat messages to be reported with a specific reason. Examples: Imminent harm, hate speech.

And it seems like a nice feature, right? Well actually, its not. There are a couple of reasons why.

Unlike Minecraft Bedrock, Minecraft Java does not have any microtransactions, so Microsoft only gets money from people buying new accounts.<br>
By this feature, Microsoft wants to ban people's accounts for them to buy the new ones.<br>
And probably, they are not going to care if someone is going to fake and/or hide messages for Microsoft to ban people.<br>

There is also an active exploit allowing players to abuse the way reports are sent and alter the context of messages by reordering them/adding messages sent by author in the middle. A mod has already been made to abuse this (https://github.com/nodusclient/gaslight)

### Videos related to the exploit:
- https://www.youtube.com/watch?v=hYAUEMlugyw&ab_channel=Aizistral
- https://www.youtube.com/watch?v=JVpfqXxMke0&t=634s1
- https://cdn.discordapp.com/attachments/991320599844622336/991777030020534412/message-fake-change.mp4
- https://cdn.discordapp.com/attachments/991320599844622336/991777030259617925/message-fake-cut.mp4<br>
<sub><sup>Credits to Aizistral for discovering the exploit and making the explanation videos</sup></sub><br>
<sub><sup>Credits to Jimmy Hoke for making the other videos</sup></sub><br>
<sub><sup>Credits to the Nodus devs for making the gaslight mod</sup></sub>

And it would be okay if the report system only affected Realms, but it doesn't.<br>
### One person wrote a mod to force Minecraft to show the ban screen, here's how it looks:
![Ban Screen](https://i.redd.it/hoyh22jsh9791.png "Image")
<sub><sup>Credits to EnderCreeperYT for writing the mod</sup></sub>

### Accounts can only be banned on 1.19+ versions, but clients running versions starting from 1.6 wont be able to join online-mode servers once they are banned.<br>
### It is like that because authentication servers (even for versions under 1.19) will ignore your account.

Bans will also be cross-platform (thanks to Microsoft accounts) and you can get banned for writing "bad stuff" in books and signs. (Taken from Minecraft website). Right now (as of 1.19.1 pre2) book and sign packets in JE are still unsigned.

Also, currently reports are not sent to server admins, and only to the "highly trained moderation team" at Microsoft<br>
On your private server, with your own rules, where some of the forbidden stuff can be accepted, you can get banned because of a random chat report.

# Part II: How does it work?

### Basically, on the reports the Microsoft moderators will receive a JSON-file containing the message, that was reported and 3 previous messages. Also, they are going to receive the timestamp of every message.

### The encryption works like this:
![Encryption System](https://media.discordapp.net/attachments/990662695399333950/993560730995531776/unknown.png?width=1440&height=645 "Image")

### The chat messages work like this:
![Chat Messages System](https://media.discordapp.net/attachments/990662695399333950/993560270028943400/unknown.png?width=1337&height=676 "Image")

# Part III: How do I secure myself and my server from chat reports?
Well, thankfully there are some ways!

### 1. You should disable enforce-secure-profile feature in your server.
It is located in server.properties.<br>
In 1.19.1, its enabled by default. If your server is still on 1.19, no worries, its already disabled.
Note: This does not stop chat reporting altogether! It only allows non signed chat messages to go through and work normally.

### 2. You could install NoEncryption on your Spigot-based server.
This does disable signatures on all messages (turns them into null), effectively blocking any reports from being made on that server.

Keep in mind, it might not fully work as expected, it's still a WIP.

SpigotMC: https://www.spigotmc.org/resources/noencryption.102902/<br>
Source code: https://github.com/Doclic/NoEncryption

### 3. You could install NoChatReports on your server.
It's a mod for forge or fabric servers (incompatible with spigot-based servers).

This is not as buggy as NoEncryption, but it's still a WIP.

### It is also a mod for clients, so you definitely recommend your players to install it.
Or, if you are just a player, then you should also install it, he-he.

Modrinth: https://modrinth.com/mod/no-chat-reports<br>
CurseForge: https://www.curseforge.com/minecraft/mc-mods/no-chat-reports<br>
Source code: https://github.com/Aizistral-Studios/No-Chat-Reports

# That's it, thanks for reading my little writeup about this feature!
Please leave a star if you liked it!
