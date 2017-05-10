I Changed your routes on the Server side in server.ts, and a little bit in Home Module though you shouldn't have to.

The Main differences are, you need to import HttpModule into the app.module and app.server.module files if you're going to use Http, before injecting it in the service.  Also added isPlatformBrowser() to the homeComponent, so it only makes the API call when it knows it is the browser.
