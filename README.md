# tilt-bridge


## Configuration
There are a few different mechanisms that can be used when running this application.  
  

### Brewers Friend
To run the application and push to brewers friend run the following command
```bash
docker run -e BREWERS_FRIEND_API_KEY=<YOUR API KEY> --net=host --privileged overtheairbrew/tilt-bridge
```
  

### Webhook
```bash
docker run -e WEBHOOK_URLS=<YOUR WEBHOOK URL> --net=host --privileged overtheairbrew/tilt-bridge
```

with webhooks you can pass more than one url to the same variable, all you need to do is seperate them with a `,`

e.g.
```bash
WEBHOOK_URLS=http://localhost:8080,http://localhost:8081
```
  
  
## Logging
If you are having issues with the app you can set the `LOG_LEVEL` variable (default value is `error`), it can be one of the following values

- debug
- info
- warn
- error
- verbose

```bash
-e LOG_LEVEL=info
```