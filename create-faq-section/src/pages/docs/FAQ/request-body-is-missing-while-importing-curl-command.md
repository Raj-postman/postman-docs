### Request body is missing while importing cURL command

While importing cURL with request body using Raw Text functionality, the request body is not imported and the body tab has _none_ option selected instead of _raw_ although the data is present.

  
Currently, this is a known issue which is being tracking on our GitHub link below:

*   GitHub Issue: [Curl imports with --data-raw will not import the body](https://github.com/postmanlabs/postman-app-support/issues/7983 "https://github.com/postmanlabs/postman-app-support/issues/7983")
    

![curl.gif](https://support.getpostman.com/hc/article_attachments/360059875553/curl.gif)

As a workaround, you can change the _\--data-raw_ to _\- d_ and that should get this working.