# Dissonɐnce

XMPP ↔ Discord conference transport done right.

Dissonɐnce is a conference transport bot between XMPP (or, Jabber) multi-user conference and Discord channel. Its purpose is to translate some of Discord functionality into XMPP conferernce, and act as a transparent relay between the two conferencing protocols.

## Features:
 - an individual connection for every Discord channel member (as if channel members are logged into XMPP conference)
 - translation of mentions (a.k.a pings) from XMPP conference to Discord format
 - translation of mentions (a.k.a pings) from Discord format to XMPP conference
 - mentioning @everyone on Discord pings all non-Dissonɐnce-managed XMPP conference members
 - translation of links to attached files and custom emoticons from Discord to XMPP conference
 - some limited command functionality

## Requirements:
The program is written for Python 3, make sure it is installed in your system.
The program also requires SleekXMPP and Discord.py libraries to be installed. They can be installed using following commands:
```
python3 -m pip install -U discord.py
python3 -m pip install -U sleekxmpp
```

## Usage
```
usage: dissonance [-h] configfile

Dissonance: a Discord <> XMPP conference transport done right

positional arguments:
  configfile  an INI configuration file with login information and settings

optional arguments:
  -h, --help  show this help message and exit
```

## INI format
```
[XMPP]
jid = dissonance@bot.jid
jidpw = passwordtojid
conference = nameofthe@conference.jabber.tld


[Discord]
token = your Discord bot OAuth token (given by Discord in "Add Bot" dialog)
channel = number of the channel you want Dissonɐnce to interact with

[UI]

name = Dissonɐnce
greetmsg = Dissonɐnce: XMPP ↔ Discord conference transport done right.
connectionprefix = [
connectionsuffix = ]
loglevel = 60
```

## Special thanks
This goes out to Jade and Sollux of homestuck@conference.jabber.ru
