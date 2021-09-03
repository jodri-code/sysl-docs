## [SYSlang's Discord Lib](https://docs.pipewarp.co.uk/SYSlang)

# The Discord.SYSl lib
### essentially just Discord.js in SYSl

## Class Description
This class is essentially just a Discord Bot API for SYSlang.

For some reason, The CKS Dev Team developed this...

## Class Imports
To call this class, or to use it in your script use `lang-imp Discord.SYSl`. Unless you are using SYStemware v51.7 or above, you will also need to import SYSnd on your machine; just type `lang-imp SYSnd` from the SYSlang CLI.

## Some code definitions & snippets

For a basic bot already written in Discord.SYSl (minus some important files that you will need to import yourself) you can check [SYSbot's GitHub Repo](https://github.com/CKStudios2018/SYSbot/)

- lang requires = token;

This is equal to a const for this lib; only works for const of token.
This allows the lib to use a token provided by Discord's Developer Portal to login to your bot. You can also set it up like SYSbot and make it retrieve the token from a file on a server.
- Discord.ready

Tells the script that this is Discord Lib pendant, and also works as an await.
When used, no matter if top or bottom of script, SYSl will read the token, login and set the status for this check to pass.
- status.set()

Set's the bot's status, if custom. If you simply want the bot to be idle (default) leave this out.
Adding this in your Discord.ready without args will cause the script to crash.

Possible args are: 'idle', 'online', 'offline' & 'odd'. Any of these can be followed by `streaming: 'stream title', 'streamURL'`, `listening: 'track name or whatever you feel like'`, or `watching: 'video name or something'`.
- NSFW management

Discord.SYSl now has integrated NSFW management. You can set up a few parameters here, but we leave the server after sending a message.
- serv

Reference to Guild. Can be used to abandon server, or create a server invite.
- mess

Message.
- content

Message content.
- tag()

Pings. Yeah, that's about it.
- self

Used to reference the bot's self. Only really useful for renaming and pinging self.
- aband

Only used to leave servers. (sometimes the script gets stuck and dupes this command).

## [Return](https://docs.pipewarp.co.uk/SYSlang/class)
