###############
Getting Started
###############

Auttaja is a fully featured moderation bot for Discord.  You've just added it to your server and want to get going as quick as possible.  Well, you've come to the right place.

This document will cover setting up the bot one feature at a time.  So if we hit a feature you don't want to use, simply skip over the section.

The Basics
==========

Let's start by covering some basics.

Permissions
-----------

Permissions are handled by an internal system.  Each user and each command receives a permissions level from 0-10.  If a user has a level greater than or equal to the required level for a command, they can execute it, pretty simple.  By default, we've assigned commands to certain levels based on a sensible set of roles.  The first level that starts to grant some extra commands is level 4.  We chose commands for this that would be used by junior level staff, or trial staff.  The next step up would be level 6.  At level 6 users have access to the full suite of moderation tools and was designed for trustworthy people.  At level 8 administrative commands start to appear.  These don't grant full access to the config, but allow for some basic maintenance of the bot.  Lastly we have level 10, at level 10 you have full access to every command in the bot, hand this one out wisely.

You might be asking, why have 10 levels if you're only going to use 5 of them?  Auttaja allows for servers to customize the required level for any command.  We left some unused levels so servers can do a bit of customization.

Command structure
-----------------

Until recently Auttaja had only one prefix and every command was tossed in like a mixing pot, with no real organization.

Now, commands are broken up into what we call "plugins".  Each plugin contains one or more commands.  To invoke a command, you use `plugin.command`.  So for example, if you wanted to access the help dialog.  The command name is help, and it is in the Auttaja plugin.  You would simply issue `auttaja.help` in any channel the bot can see, and it will send you a help message.  Let's look at another example.  Let's assume for a moment that you're looking for spam protection.  Well, in the help message, we can see an antispam plugin.  Within that, there is an enable command, so to enable antispam, you would type `antispam.enable`.

.. topic:: Help Command

      The help command allows you to view the contents of each plugin by issuing the plugin name after the help command.  You could do `auttaja.help gatekeeper` to see the contents of gatekeeper

Logging
=======

Logging in Auttaja is one of its most important features, however it is an optional one.  Normally Auttaja will log all punishments, joins/leaves, and messages detected by any of our moderation features.  Joins and leaves can be toggled on and off, or logging and be omitted altogether, but we don't recommend it.

To enable logging, all you have to do is set the logging channel.  It is up to you to create the channel and set the permissions you would like on it.  Once the channel exists, just issue `logging.setchannel #channeltag` replacing channeltag with the actual name of the channel.

Gatekeeper
==========

Gatekeeper is a feature in Auttaja that protects your server from raiders at the point when they join the server.  Gatekeeper runs in one of two modes, the first is called verification.  In this mode, Gatekeeper presents the user with a link that forces them to do a captcha, once the captcha is completed, they are let into the server.  The second mode is agree mode.  In this mode, you can prompt the users to read some guidelines or rules, and then type `gatekeeper.agree` to gain access to the server, thus removing any ability for people to argue that they didn't read the rules.

To enable Gatekeeper, issue `gatekeeper.enable`, by default it will be in verification mode.  To change modes to agree issue `gatekeeper.togglemode`.  Thats about all there is to it.  The bot will create a Gatekeeper role that will be assigned to anyone who joins, and limits their access.  Upon removal, they gain full access to the server.

If you would like Auttaja to assign a different role upon removal of the Gatekeeper role, set one using `gatekeeper.memberrole rolename`

Nick Change Requests
====================

Auttaja also has the ability to allow your moderators to verify every nickname change before allowing the user to set it.  This is done through the `nick` plugin.  To enable nick change requests issue a `nick.setchannel channelname` and it will automatically start working!

Anti-X
======

All of the anti-something features are very similar in how they work, and how they're enabled and disabled.  The only notable one here is antispam.  Antispam watches for users that send 5 or more of a message with the same content in 5 seconds, or 6 messages with different content in 5 seconds, and mutes them.  A role called spammer is created upon enabling, and removes access to all channels when given to someone.

All mutes are automatically undone after 1 hour, to prevent people from being forgotten about.  If someone gets put there for raiding, simply ban them from the server before the hour is up to prevent them from getting access to the server again.

.. topic:: Muting

      At this time, the mute command in the moderation plugin requires antispam to be enabled for it work.
