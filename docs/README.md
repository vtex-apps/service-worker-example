# Service Worker Example

Service Workers (SWs) are a poweful tool to handle network requests separate from a web page, as scripts running in the background. They are well known to handle push notifications and background syncronization.

With `service-worker` builder, we can allow an app to expose its own implementation of a Service Worker, enabling VTEX stores to use such Service Worker into their scope.

Service Workers allow us to introduce 6 different functions, which can be implemented inside the `service-workers/` folder:

1. Activate -> `activate.js`
2. Fetch -> `fetch.js`
3. Install -> `install.js`
4. Message -> `message.js`
5. Push -> `push.js`
6. Sync -> `sync.js`

Whatever is outside those 6 files, should be implemented in `header.js`. The implementation result in the VTEX store DevTools should be as follows:

![image](https://user-images.githubusercontent.com/21017429/114235943-84d14600-9946-11eb-8e1a-4a8f19d3d3d8.png)


Each function can be tested according to the behavior of each event handler. When triggering such event handler, the function body will be executed as follows:

![image](https://user-images.githubusercontent.com/21017429/114235975-8e5aae00-9946-11eb-91f8-b1d7f6d92485.png)


An example is provided in this app for exploration purposes.
