---
description: "Automatically generated file. DO NOT MODIFY"
---

```bash


mgc-beta teams channels patch --team-id {team-id} --channel-id {channel-id} --body '{\
    "displayName": "UpdateChannelModeration",\
    "description": "Update channel moderation.",\
    "moderationSettings": {\
        "userNewMessageRestriction": "moderators",\
        "replyRestriction": "everyone",\
        "allowNewMessageFromBots": true,\
        "allowNewMessageFromConnectors": true\
    }\
}\
'

```