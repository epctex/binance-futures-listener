# Actor - Binance Futures Listener

## Binance Futures Listener

The Binance Futures Listener supports the following features:

-   Listen traders - You can listen any trader with their ID and check their positions every second.

-   Always be aware on open or closed positions - Always get informed whenever the trader opens or closes a position. Instantly!

-   Get notified by email - Put your email address and get notified via email by the open or closed positions.

-   Custom integrations via Webhook URL - Do you need custom integrations? Put your webhook URL and immediately transfer the data!

## Bugs, fixes, updates and changelog

This scraper is under active development. If you have any feature requests you can create an issue from [here](https://github.com/epctex/binance-futures-listener/issues).


## Input Parameters

The input of this scraper should be JSON containing the list of pages on Binance Futures Listener. Possible fields are:

- `traderId`: (Required) (String) Trader ID that you want to listen via Binance Futures Listener.

- `email`: (Optional) (String) Email address you want to get notified by.

- `webhookURL`: (Optional) (String) Webhook URL that you want to trigger on the notifications.

- `proxy`: (Required) (Proxy Object) Proxy configuration.

This solution requires the use of **Proxy servers**, either your own proxy servers or you can use [Apify Proxy](https://www.apify.com/docs/proxy).


### Binance Futures Listener Scraper Input example

```json
{
  "traderId": "347E5D94D2F0F988A7CE7D552A0FB2FB",
  "proxy": {
    "useApifyProxy": true
  },
  "email":"email@email.com",
  "webhookURL":"webhook.url.com/api",
}
```

## During the Run

During the run, the actor will output messages letting you know what is going on. Each message always contains a short label specifying which page from the provided list is currently specified.
When items are loaded from the page, you should see a message about this event with a descriptive message for each request.

If you provide incorrect input to the actor, it will immediately stop with failure state and output an explanation of what is wrong.

## Binance Futures Listener Export

During the run, the actor stores results into a key value store. Each position is a separate item in the key value store.

You can manage the results in any languague (Python, PHP, Node JS/NPM). See the FAQ or <a href="https://www.apify.com/docs/api" target="blank">our API reference</a> to learn more about getting results from this Binance Futures Listener actor.

## Tips

The actor runs indefinitely. It automatically caches the data per each trader and preserves the positions for that specific user. The automation retrieves the data every second. Meaning that you'll be immediately notified whenever a change happens.

## Contact
Please visit us through [epctex.com](https://epctex.com) to see all the products that is available for you. If you are looking for any custom integration or so, please reach out to us through the chat box in [epctex.com](https://epctex.com). In need of support? [devops@epctex.com](mailto:devops@epctex.com) is at your service.
