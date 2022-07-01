# Chat Reports Writeup
What are chat reports? How do I secure my server and myself from it?

# Part I: What are chat reports and why do they exist?
Chat Reports are a feature made by Microsoft for adding payments by players to the game.<br>
Essentially, their function is to report people's chat messages with specifying some reasons. Example: Imminent harm, hate speech.

And it seems, like its a nice feature? But actually, its not. It has a couple of reasons because they are not.

Unlike Minecraft Bedrock, Minecraft Java does not have any microtransactions, so Microsoft only gets money from people buying new accounts.<br>
By this feature, Microsoft wants to ban people's accounts for them to buy the new ones.<br>
And probably, they are not going to care if someone is going to fake and/or hide messages for Microsoft to ban people.<br>
### Great examples:
- https://cdn.discordapp.com/attachments/991320599844622336/991777030020534412/message-fake-change.mp4
- https://cdn.discordapp.com/attachments/991320599844622336/991777030259617925/message-fake-cut.mp4<br>
<sub><sup>Credits to Azistral for discovering the bug</sup></sub><br>
<sub><sup>Credits to Jimmy Hoke for making the videos</sup></sub>

And it would be okay if the ban would only block Realms, but it doesn't.<br>
### One person wrote a mod to force Minecraft to show the ban screen, here's how it looks:
![Ban Screen](https://i.redd.it/hoyh22jsh9791.png "Image")
<sub><sup>Credits to EnderCreeperYT for writing the mod</sup></sub>

### Banned accounts on 1.19+ versions will not be able to join any multiplayer servers in any version.<br>
### It is like that because authentication servers will ignore your account.

Bans are also cross-platform and you can get banned for writing "bad stuff" in books and signs. (Taken from Minecraft website)

And so, it would be nice, if the reports are sent to server admins, but its not!<br>
On your private server, with your own rules, where you can agree some of the forbidden stuff, you can get banned because of a random chat report.

# Part II: How does it work?

### Basically, on the reports the Microsoft moderators will receive a JSON-file containing the message, that was reported and 3 previous messages. Also, they are going to receive the timestamp of every message.

### The encryption is working like this:
![Encryption System](https://media.discordapp.net/attachments/990870051722756196/990879172949864448/unknown.png?width=1440&height=643 "Image")

### The chat messages are working like this:
![Chat Messages System](https://media.discordapp.net/attachments/990870051722756196/990880992476684308/unknown.png?width=1335&height=676 "Image")

And keep it mind, you can get reported even if you are offline on the server and the message was completely fake!

# Part III: How do I secure myself and my server from chat reports?
Well, there are some ways!

### As first, you should disable enforce-secure-profile feature in your server.
It is located in server.properties.<br>
In 1.19.1, its enabled by default. If you are on 1.19, no worries, its already disabled.

### As second, you could install NoEncryption on your server.
It's a plugin for spigot-related servers. 

Keep in mind, it might be buggy, work is still in progress.

SpigotMC: https://www.spigotmc.org/resources/noencryption.102902/<br>
Source code: https://github.com/Doclic/NoEncryption

### As third, you could install No Chat Reports on your server.
It's a mod for forge or fabric servers.

This is not that buggy, as NoEncryption, but the work is still in progress.

### It is also a mod for clients, so you definitely recommend your players to install it.
Or, if you are just a player, then install it, he-he.

CurseForge: https://www.curseforge.com/minecraft/mc-mods/no-chat-reports<br>
Source code: https://github.com/Aizistral-Studios/No-Chat-Reports

# That's it, thanks for reading my little writeup for letting you know about this feature.
Please leave a star, if you liked it.
