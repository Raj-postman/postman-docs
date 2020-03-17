### Parse error on monitors

If the collection runs successfully via the collection runner and fails while on monitors then check in the console logs if this fails with Parse Error.

![Parse_Error.png](https://support.getpostman.com/hc/article_attachments/360058986934/Parse_Error.png)

The reason for the monitors to fail is that in recent versions, Node.js limited the header limit to 8 KB for security reasons ([NodeJS - Change Logs](https://github.com/nodejs/node/blob/master/doc/changelogs/CHANGELOG_V10.md#2018-11-27-version-10140-dubnium-lts-rvagg) ). 

Do check if the cookie size in the request header exceeds 8 KB. Run the collection using the collection runner with the console window open then copy the Cookie of your request header to this link: [http://bytesizematters.com](http://bytesizematters.com/)

![Header.gif](https://support.getpostman.com/hc/article_attachments/360049107393/Header.gif)

  
Also, the reason for the run to succeed in the collection runner is that it’s using an older version, in which the header limit is 80 KB (this might get upgraded in the future), but monitors use the newer version with the 8 KB limit. Hence reducing this cookie size from your end should help you run the monitors without any issues.

This GitHub thread should help you know more on the same: [https://github.com/nodejs/node/issues/24692](https://github.com/nodejs/node/issues/24692)

* * *

Ticket reference (Internal - will not be published):

*   [https://postman.zendesk.com/agent/tickets/45742](/agent/tickets/45742)
    
*   [https://postman.zendesk.com/agent/tickets/45437](/agent/tickets/45437)
