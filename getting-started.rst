###############
Getting Started
###############

Auttaja is a fully featured moderation bot for Discord.  You've just added it to your server and want to get going as quick as possible.  Well, you've come to the right place.

This document will cover setting up the bot one feature at a time.  So if we hit a feature you don't want to use, simply skip over the section.

The Basics
==========

Let's start by covering some basics.  First, you need to have Auttaja in your server, if you haven't already added it you can do so by `clicking here <https://discordapp.com/oauth2/authorize?client_id=242730576195354624&scope=bot&permissions=1576270967>`_

Throughout this guide we will be using the bots default prefix, but you can change this on your server using `-setprefix`

It is possible to set prefixes that can stop the bot from responding on your server.  If this happens, you can also mention the bot to change it again.  For example: `@Auttaja setprefix -` to reset it back to the default.

Setup
-----

Most of the configuration in Auttaja is done through the setup command.  Running `-setup` will bring up a configuration menu allowing your to browse through the configurable options, and give you a chance to change them.


Permissions
-----------

Permissions are handled by a role based system.  We split commands into 5 command groups.  Everyone, Helper, Moderation, Admin, Owner, and Helper.  You only need to be concern with the former 4 options.  You can assign roles in your server to each of the 4 command groups.  Having access to a specific command group will give you access to all commands in that group and the ones under that.  For example, if someone has a role that is attached to the Admin group, they will have access to commands in the Everyone, Moderation, and Admin groups.

You can use the `-attachperm` command to start assigning roles in your server to command groups.  For example, if you had a role called "Moderators", you could assign them to the Moderation group by running `-attachperm Moderation Moderators`.

.. topic:: Automatic Permissions

      Anyone you add to that role will automatically gain moderation permissions on Auttaja.  If you remove the role from someone, they will automatically lose moderation permissions on Auttaja.


Logging
=======

Logging in Auttaja is one of its most important features, however it is an optional one.  Normally Auttaja will log all punishments, joins/leaves, and messages detected by any of our moderation features, as well as audit logs of all Auttaja commands run.  Joins and leaves, and auditing can be toggled on and off, or logging and be omitted altogether, but we don't recommend it.

Logging can be configured through the `-setup` command.


Gatekeeper
==========

Gatekeeper is a feature in Auttaja that protects your server from raiders at the point when they join the server.  Gatekeeper runs in one of two modes, the first is called verification.  In this mode, Gatekeeper presents the user with a link that forces them to do a captcha, once the captcha is completed, they are let into the server.  The second mode is agree mode.  In this mode, you can prompt the users to read some guidelines or rules, and then type `gatekeeper.agree` to gain access to the server, thus removing any ability for people to argue that they didn't read the rules.

Gatekeeper can be configured through the `-setup` command.

Nick Change Requests
====================

Auttaja also has the ability to allow your moderators to verify every nickname change before allowing the user to set it.

Check out the "Nick Requests" part of the `-setup` command.

Automod
=======

Auttaja has a collection of auto-moderation features that are all part of the automod part of the `-setup` command.

The automod features currently available are
* Anti-advert - Removes advertisments for other Discord servers from chat automatically.
* Anti-spam - Detects spam, automatically removes it, and mutes the person spamming.
* Anti-zalgo - Removes annoying zalgo text from chat automatically.
* Anti-raid - Automatically mutes users if more than 3 join within a 5 second period.  A common thing that happens when your server is posted in a Discord raiding community.
* Anti-shortener - Automatically removes messages from chat that contain shortened links from many popular shortening services.
* Bad link protection - Scans links for possible dangerous links like IP grabbers, malware sites, etc, and removes them from chat.

All mutes are automatically undone after 1 hour, to prevent people from being forgotten about.  If someone gets put there for raiding, simply ban them from the server before the hour is up to prevent them from getting access to the server again.

.. topic:: Muting

      If a spammer role is not set when you try to mute someone, it will be created automatically.
