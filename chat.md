# 🗣️ Chat

&#x20;`WEBSOCKET wss://zhmhmce2u6.execute-api.eu-west-3.amazonaws.com/{env}`

| Env  |
| ---- |
| dev  |
| demo |
| prod |



`Method ready (apres la connection)`

{% tabs %}
{% tab title="Body" %}
```json
{
    "action": "ready",
    "authToken": "String"     #Token du patient
    }
```
{% endtab %}

{% tab title="Return Body" %}
```json
{
	"message": "Connection ready"
}
```
{% endtab %}
{% endtabs %}





`Method create_chat (après le ready)`

{% tabs %}
{% tab title="Body" %}
```json
{
    "action": "create_chat",
    "authToken": "String",		#Token du patient
    "message": "try to debug",
    "recipient_ids": [
	"664a5a6acce0dc382e1f3520",
	"664a66e273297bc042149008"
	                ]
}
```
{% endtab %}

{% tab title="Body return broadcast" %}
```json
{
	"action": "create_chat",
	"chat": {
		"id": "string",
		"participants": [
			{
				"participant_id": "string",
				"last_seen": timestamp
			},
			{
				"participant_id": "string",
				"last_seen": timestamp
			}
		],
		"messages": [
			{
				"owner_id": "string",
				"message": "string",
				"sended_time": timestamp
			}
		]
	}
}
```
{% endtab %}
{% endtabs %}

`Method get_message`

{% tabs %}
{% tab title="Body" %}
```json
{
    "action": "get_messages",
    "authToken": "string"        #token utilisateur
}
```
{% endtab %}

{% tab title="Body return" %}
```json
{
	"action": "get_message",
	"chats": [
		{
			"id": "string",		#id chat
			"participants": [
				{
					"participant_id": "string",
					"last_seen": timestamp
				},
				{
					"participant_id": "string",
					"last_seen": timstamp
				}
			],
			"messages": [
				{
					"owner_id": "string",
					"message": "string",
					"sended_time": timestamp
				}
			]
		}
	]
}
```
{% endtab %}
{% endtabs %}



`Method send_message`

{% tabs %}
{% tab title="Body" %}
```json
{
    "action": "send_message",
    "authToken": "string",        #token utilisateur
    "chat_id": "string",
    "message": "string"

}
```
{% endtab %}

{% tab title="Body return brodcast" %}
```json
{
	"action": "receive_message",
	"chat_id": "string",
	"message": "string",
	"owner_id": "string",
	"timestamp": timestamp
}
```
{% endtab %}
{% endtabs %}





`Method read_message`

{% tabs %}
{% tab title="Body" %}
```json
{
    "action": "read_message",
    "authToken": "string",    #token utilisateur
	"chat_id": "string"
}
```
{% endtab %}

{% tab title="Body return broadcast" %}
```json
{
	"action": "read_message",
	"chat": {
		"id": "string",
		"participants": [
			{
				"participant_id": "string",
				"last_seen": timestamp
			},
			{
				"participant_id": "string",
				"last_seen": timestamp
			}
		],
		"messages": [
			{
				"owner_id": "string",
				"message": "string",
				"sended_time": timestamp
			},
			{
				"owner_id": "string",
				"message": "string",
				"sended_time": timestamp
			}
		]
	}
}
```
{% endtab %}
{% endtabs %}
