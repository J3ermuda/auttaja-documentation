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

Returns the local time in a city

``-localtime <city/post(zip) code>``

Agree
========

Agrees to the server guidelines and grants access to the server

``-agree``

Approve
========

Approves a member and grants them access to the server

``-approve <member>``

Welcome Test
========

Sends a test welcome message

``-welcometest [mention]``


