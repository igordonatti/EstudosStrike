## About the Code node
The Code node has two operational **Modes** that change the way it procesees the data. The **Run Once for All Items** mode allows you to accumulate data from all items on the input list. The **Run Once for Each Items** is used to add custom snippets of JavaScript code that should be executed onde for every item that it receives as the input.

## Scheduled Trigger
To ensure accurate scheduling with the Schedule Trigger node, be sure the timezone is set correctly for your n8n instance or the workflow's settings. The Schedule Trigger node will use the workflow's timezone if it's set; it will fall back to the n8n instance's timezone if it's not.

## Sharing credentials
Exported workflow JSON files include credential names and IDs. While IDs aren't sensitive, the names could be, depending on how you name your credentials. HTTP Request nodes may contain authentication headers when imported from cURL. Remove or anonymize this information from the JSON file before sharing to protect your credentials.