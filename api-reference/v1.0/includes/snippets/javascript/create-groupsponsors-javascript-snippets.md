---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const directoryObject = {
  '@odata.id': 'https://graph.microsoft.com/v1.0/groups/{group-id}'
};

await client.api('/users/d8ab5060-f636-4cff-ae97-d4687f5c83f3/sponsors/$ref')
	.post(directoryObject);

```