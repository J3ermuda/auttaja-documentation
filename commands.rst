########
Commands
########

Below you will find a listing of all of Auttaja's plugins and commands, a brief description of what they do, and some example syntax.

Anti-advert
===========

The anti-advert plugin is used to detect and remove messages containing advertisments for other Discord servers.  It includes official Discord links, as well as many of the popular invite link shorteners.

Enable
------

Enables anti-advert

.. code::

  antiadvert.enable

Disable
-------

Disables anti-advert

.. code::

  antiadvert.disable

Anti-grabify
============

The anti-grabify plugin is used to detect and remove messages containing IP grabber links somewhere in the redirect chain.

Enable
------

Enables anti-grabify

.. code::

  antigrabify.enable

Disable
-------

Disables anti-grabify

.. code::

  antigrabify.disable

Anti-IP
=======

The anti-IP plugin is used to detect and remove messages containing publicly routable IP addresses.  The idea is to prevent personal army DDoS requests.

Enable
------

Enables anti-IP

.. code::

  antiip.enable

Disable
-------

Disables anti-IP

.. code::

  antiip.disable

Anti-Shortener
==============

The anti-shortner plugin is used to detect and remove messages containing URL shorteners.

Enable
------

Enables anti-shortener

.. code::

  antishortener.enable

Disable
-------

Disables anti-shortener

.. code::

  antishortener.disable

Anti-Spam
=========

The anti-shortner plugin is used to detect and remove spam.  Users who spam are muted for an hour, but can be unmuted sooner using `mod.unmute`.

Enable
------

Enables anti-spam

.. code::

  antispam.enable

Disable
-------

Disables anti-spam

.. code::

  antispam.disable

Auttaja
=======

The Auttaja plugin contains a lot of informational commands about the bot as well as commands that allow you to manipulate how the bot works at a low level.

Help
----

Displays a listing of all of the plugins, and allows you to list all of the commands in each plugin that you have access to.

.. code::

  auttaja.help
  auttaja.help gatekeeper

SetInvite
---------

Sets your servers invite code for Auttaja's own Discord invite shortener.  Once you set the invite code you can access your server at https://auttaja.io/invitecode

.. code::

  auttaja.setinvite myawesomeserver
  auttaja.setinvite lol

Invite
------

Returns an invite link for Auttaja

.. code::

  auttaja.invite

Ping
----

Tests and displays the time it takes for the message you send to get to the bot for processing

.. code::

  auttaja.ping

Profile
-------

Displays information about the person calling the command, or a tagged member.  Shows information like Username, User ID, Status, Discriminator, Rank, Playing status, Created date, and Join date

.. code::

  auttaja.profile
  auttaja.profile @otheruser
  auttaja.profile 242730576195354624
  auttaja.profile Kelwing#3658

Server Info
-----------

Displays information about the Discord server the command is run in.

.. code::

  auttaja.serverinfo

Server Count
------------

Displays the current amount of shards and the number of servers each shard is in.

.. code::

  auttaja.servercount

Enable Plugin
-------------

Enables a disabled plugin on the server the command is run in

.. code::

  auttaja.disableplugin mod

Disable Plugin
--------------

Disabled an enabled plugin on the server the command is run in

.. code::

  auttaja.enableplugin mod

Info
----

Displays info about the current running version of Auttaja, including a recent changelog

.. code::

  auttaja.info

Custom Commands
===============

Allows you to add custom commands to Auttaja with custom responses.  Required Auttaja to have embed permissions to prevent @everyone and @here abuse.

Add
---

Adds a new custom command

.. code::

  custom.add cmdname | command content | help message
  custom.add coolserverinfo | Visit our website! | Shows info about the server

Remove
------

Removes a custom command

.. code::

  custom.remove coolserverinfo

Deleted messages
================

The deleted messages plugin records deleted messages and allows you to retrieve a list

Logs
----

Returns a text file containing the specified amount of deleted messages

.. code::

  deleted.logs 50
  deleted.logs 1000

Logging
=======

The logging plugin is used to configure and control how and where Auttaja logs to

Toggle Join Leave
-----------------

Toggles join/leave message on and off

.. code::

  logging.togglejoinleave

Set Channel
-----------

Sets the channel the Auttaja logs to

.. code::

  logging.setchannel #logging

Toggle Command Auditing
-----------------------

Toggles whether or not commands run will be logged to the log channel

.. code::

  logging.togglecmdaudit

Moderation
==========

The moderation plugin contains all of the moderation commands Auttaja has to offer

Ban
---

Bans a user by tag, User#Discrim, or snowflake ID.  Can also be used to hackban people who aren't in the server by using the ID.

.. code::

  mod.ban @Kyle2000
  mod.ban Kyle2000#1009
  mod.ban 337329813897347072

Kick
----

Kicks a user from the server by tag, User#Discrim, or snowflake ID.

.. code::

  mod.kick @Kyle2000
  mod.kick Kyle2000#1009
  mod.kick 337329813897347072

Strike
------

Gives the user a strike.  Strikes are essentially a warning and a note on their account you can lookup with `mod.search`

.. code::

  mod.strike @Kyle2000
  mod.strike Kyle2000#1009
  mod.strike 337329813897347072

Reason
------

Adds a reason to a given punishment by punishment ID

.. code::

  mod.reason 342 Known raider, spamming gore

Purge All
---------

Purges the given number of messages from the channel, regardless of who sent them

.. code::

  mod.purgeall 20

Purge
-----

Purges the given number of messages from the given member

.. code::

  mod.purge @Kyle2000 10

Remove Punishment
-----------------

Marks a punishment as deleted, it will no longer show up in `mod.search`

.. code::

  mod.rmpunish 342

Unban
-----

Unbans the given member

.. code::

  mod.unban @Tom#0131
  mod.unban Tom#0131
  mod.unban 188092131376758784

Search
------

Lists all non-deleted punishments for the given user

.. code::

  mod.search @Tom#0131
  mod.search Tom#0131
  mod.search 188092131376758784

Search All
----------

Lists all punishments, included deleted, for the given user

.. code::

  mod.searchall @Tom#0131
  mod.searchall Tom#0131
  mod.searchall 188092131376758784

PunishInfo
----------

Lists all of the information for the given punishment

.. code::

  mod.punishinfo 342

Mute
----

Mutes the given member by removing all of their roles, and giving them the spammer role.  Requires anti-spam to be enabled.

.. code::

  mod.mute @Tom#0131
  mod.mute Tom#0131
  mod.mute 188092131376758784

Unmute
------

Unmutes the given member by removing the spammer role and returning their previous roles

.. code::

  mod.unmute @Tom#0131
  mod.unmute Tom#0131
  mod.unmute 188092131376758784

Pin
---

Pins the given message to the current channel

.. code::

  mod.pin 382377051191115777

Unpin
-----

Unpins the given message from the current channel

.. code::

  mod.unpin 382377051191115777

Nicknames
=========

The nicknames plugin handles nickname change requests

Request
-------

Requests a nickname change

.. code::

  nick.request MyCoolNickname

Cancel
------

Cancels a nick request by ID

.. code::

  nick.cancel 457

Accept
------

Accepts a given nickname request by ID.  A back up for when Discord fails to send reaction notifications to Auttaja

.. code::

  nick.accept 457

Deny
----

Denies a given nickname request by ID.  A back up for when Discord fails to send reaction notifications to Auttaja

.. code::

  nick.deny 457

Permissions
===========

The permissions plugin is used to configure user, role, and command permissions

Set User
--------

Sets a users permission level

.. code::

  perm.setuser @Jet#0038 10

Set Role
--------

Sets a roles permission level

.. code::

  perm.setrole Moderator 6

Set Command
-----------

Sets the required permission level for a command

.. code::

  perm.setcommand auttaja.help 1

Vote
====

The vote plugin introduces a democratic voting system, where a user can call a vote, and people vote on the topic using reactions.  You can specify which users are included in the vote by tagging them individually or by roles.  Once the vote is complete, a PDF is generated with the results and posted into the channel of your choice.

Call
----

Calls a vote

.. code::

  vote.call

End
---

Ends a vote, must be done in the channel created specifically for that vote

.. code::

  vote.end

Wikipedia
=========

The wikipedia plugin allows you to query wikipedia for articles, and returns a short summary of the article

Search
------

Search for a term on wikipedia and return the first result.  Won't return anything if the term is too ambiguous

.. code::

  wiki.search discord app
