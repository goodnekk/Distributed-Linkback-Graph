## Protocol

The protocol is minimal and underspecified by design.

### Node
Every Node is required to have the following requests:

**GET**

This will return a JSON object of the following format:
```json
{
  "DLBG": "0.1",
  "value": {value},
  "link": [
    {
      "href":"{url}",
      "type": "{url}"
    }
  ],
  "linkback":[
    {
      "href":"{url}",
      "type": "{url}"
    }
  ]
}
```

`Value` can be a String, Number, or Array. (Preferably not an Object)

**POST**

This will allow anyone to request a linkback on this Node. The post should be in this format:
```json
{
  "DLBG": "0.1",
  "href": "{url}",
  "type": "{url}"
}
```
The server will respond with the following:
```json
{
  "DLBG": "0.1",
  "message": "{received/accepted/rejected}"
}
```
### Linktype
**GET**

This will return a special Node that describes a link type. It does not have links or linkback
```json
{
  "DLBG": "0.1",
  "name": "{name}",
  "inverse": "{inverse name}",
  "description": "{short description}"
}
