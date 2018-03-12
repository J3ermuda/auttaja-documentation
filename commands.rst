########
Commands
########

Below you will find a listing of all of Auttaja's commands, a brief description of what they do, and an example of each command.

Appeal
=========

Allows you to unjustify a strike that the user who recieved the strike thinks that the strike shall not have been given to them.

``-appeal <strike ID>``

Set Prefix
========

Allows you to change the bot's prefix to whatever prefix you desire for the current guild.

``-setprefix <prefixhere>``

Dump Config
========

Allows you to get a JSON config file in which you can edit and reupload for the current guild.

``-dumpconfig``

Load Config
========

Loads a modified JSON config file when this command is put into the description of uploading the config file to Discord.

``-loadconfig``

Setup
========

Enters a configuration mode to setup Auttaja's plugins, and options

``-setup``

Add Command
========

Adds a custom command with a response and help message.

``-addcommand <command> <response> | <help message>``

Remove Command
========

Removes the custom command that you created.

``-rmcommand <command>``

List Commands
========

Lists all possible custom commands that the user has created for the guild.

``-listcommands``

Add Filter
========

Adds a regex filter to the bot where once the regex is typed, that message will be deleted.

``-addfilter <regex>``

Remove Filter
========

Removes the regex filter from the bot

``-removefilter <id>``

List Filters
========

Lists all the regex filters in the current guild.

``-listfilters``

Define
========

Does a dictionary lookup to get a definition of a word.

``-define <word>``

Weather
========

Returns the weather in a certain city.

``-weather <city/post(zip) code>``

Local Time
========

Returns the local time in a city.

``-localtime <city/post(zip) code>``

Agree
========

Agrees to the server guidelines and grants access to the server.

``-agree``

Approve
========

Approves a member and grants them access to the server.

``-approve <member>``

Welcome Test
========

Sends a test welcome message.

``-welcometest [mention]``

Info
========

Shows information about the bot.

``-info``

Help
========

Lists all the commands and their syntax, or a single command if passed as an argument.

``-help [command]``

Ping
========

Tests the response time between a message being sent in Discord and Auttaja handling it.

``-ping``

Role ID
========

Gets the ID of a role given by name.

``-roleid <Role Name>``

Invite
========

Returns an invite link for the bot.

``-invite``

Contributors
========

Lists everyone who has contributed to Auttaja.

``-contributors``

Server Info
========

Lists information about the current Discord server.

``-serverinfo``

Ban
========

Bans a user from a server.

``-ban <@user>``

Kick
========

Kicks a user from a server.

``-kick <@user>``

Strike
========

Strikes a user from a server.

``-strike <@user>``

Mute
========

Mutes a user from speaking in a server.

``-mute <@user>``

Unmute
========

Unmutes a user from a server.

``-unmute <@user>``

Reason
========

Sets a reason for a punishment.

``-reason <id> <reason>``

Search
========

Searches a user for punishments.

``-search <user>``

Purge
========

Deletes messages from a user.

``-purge <user> <number of messages>``

Pin
========

Pins a message to the channel.

``-pin <message id>``

Unpin
========

Unpins a message from the channel.

``-unpin <message id>``

Punish Info
========

Gives info about a punishment that a user recieved.

``-punishinfo <id>``

Purge All
========

Deletes a certain amount of messages in a server.

``-purgeall <number of messages>``

Remove Punishment
========

Removes a punishment from a user.

``-rmpunish <id> <reason>``

Search All
========

Searches all punishments, including deleted ones.

``-searchall <user|none>``

Profile
========

Returns account information for the user.

``-profile <user>``

Nick
========

Requests a change to your nickname.

``-nick <nickname>``

Osu!
========

Fetches information from the osu! API. The sub commands you can currently use are `getuser` or `getrecent`.

``-osu subcommand args``

Attach Permissions
========

Assigns a role to a specific perm group: `User`, `Moderation`, `Admin`, and `Owner`.

``-attachperm PermGroup RoleName``

Detach Permissions
========

Detaches a role from a specific perm group: `User`, `Moderation`, `Admin`, and `Owner`.

``-detachperm PermGroup RoleName``

Twitter Authorization
========

Allows Auttaja to allow you to use Twitter using commands.

``-tauth``

Twitter Pin
========

This completes the twitter authorization process by telling me the OAuth2 pin code.

``-tpin <pincode>``

Test Tweet
========

Sends a test tweet through Auttaja.

``-ttest``

Twitter Post
========

Update your twitter status.

``-tpost <status update>``

Twitter Deauthorization
========

Wipes your authorization from our database.

``-tdeauth``

Move All
========

Moves everyone from the current voice channel to the specified channel.

``-moveall <channelid>``

Call Vote
========

Calls a vote (maximum is 10 options).

``-callvote name | topic | mentions | option 1 | option 2 ...``

End Vote
========

Ends a vote.

``-endvote <channel>``
