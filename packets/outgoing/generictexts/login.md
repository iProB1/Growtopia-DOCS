# login packet

login packet you send after receiving SERVER_HELLO (type: 1) net message

### note: this is only for windows rn

## params
`tankIDName` - growtopia accounts name (dont include in packet if you want to use guest account)

`tankIDPass` - growtopia accounts password (dont include in packet if you want to use guest account)

`requestedName` - guest accounts name

`f` - swear filter, (1 or 0, enabled or disabled)

`protocol` - current protocol of growtopias server

`game_version` - growtopia version

`fz` - file size of unmodified Growtopia.exe

`lmode` - login mode (get this from OnSendToServer)

`cbits` - [personal settings](https://github.com/iProB1/Growtopia-DOCS/edit/main/packets/outgoing/generictexts/login.md#) (show chat only from friends etc.)

`player_age` - players age, 0 - 60 years

`GDPR` - is GDPR accepted (1 or 0, accepted or not), not fully sure tho

`category` - world select menu world filter

`totalPlaytime` - gt didn't add this yet, but can be found in save.dat

`hash2` - HashString of mac_address + "RT" (signed integer)

`meta` - some random string from server_data.php

`fhash` - HashString of all login packet params (signed integer)

`rid` - generated using GetSimpleGUIDAsString

`platformID` - what platform player is using (0: windows, 1: ios, 2: macos, 4: android)

`deviceVersion` - devices version, currently GetDeviceOSVersion only returns 0

`country` - devices country code

`hash` - HashString of device_id + "RT" (signed integer)

`mac` - devices mac address

`user` - accounts user id, add only if not empty (get this from OnSendToServer)

`token` - session token, add only if not empty (get this from OnSendToServer)

`UUIDToken` - uuidtoken, add only if not empty (get this from OnSendToServer)

`doorID` - door id, add only if not empty (get this from OnSendToServer)

`wk` - generated in some way by those registry keys, todo: figure out how

`zf` - HashString of unmodified Growtopia.exe's data (signed integer)

### Personal Settings
`adding_friends` - 1

`player_text` - 2

`in_app` - 3

`tapjoy` - 4

`public_broadcast` - 5

`guild_invites` - 6

`guild_flag` - 7

`billboard` - 8

`classic_store` - 9

