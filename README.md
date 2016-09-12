#Frontier

=======================


[<img src="http://fourloopph.bitbucket.org/developers/images/devLogo.png" alt="4LOOP Logo" width="1300px" height="192px" />](http://fourloopph.bitbucket.org/developers/)


Frontier SDK to connect to Frontier's Analytics API


#Installing

You have several options:
```sh
# Bower
bower install frontier
```

```sh
# NPM (Coming soon)
npm i frontier
```

```html
// PRODUCTION
<script src="https://cdn.rawgit.com/4LOOPph/frontier/v1.0.4b/dist/frontier.js"></script>
or
<script src="https://cdn.rawgit.com/4LOOPph/frontier/v1.0.4b/dist/frontier.min.js"></script>
// STAGING
<script src="https://cdn.rawgit.com/4LOOPph/frontier/v1.0.4b/dist/frontier-test.js"></script>
or
<script src="https://cdn.rawgit.com/4LOOPph/frontier/v1.0.4b/dist/frontier-test.min.js"></script>
// LOCAL
<script src="https://cdn.rawgit.com/4LOOPph/frontier/v1.0.4b/dist/frontier-dev.js"></script>
or
<script src="https://cdn.rawgit.com/4LOOPph/frontier/v1.0.4b/dist/frontier-dev.min.js"></script>
```
Note:  frontier for  **LOCAL**  is not usable for production.

#JavaScript Usage
In your 'deviceready' handler, set up your Frontier tracker:

* `window.Frontier.Initialize({ accessCode: 'XXXXXXXXXXXXXXX',trackerName: 'tracker-name',encoding: 'utf-8'})` 
where XXXXXXXXXXXXXXX is your Symphony Access Code base on your subscription 

To track a Screen (View):
* `window.Frontier.screenTrack({screenName:'Screen Title'})`

To track an Event:
* `window.Frontier.eventTrack({eventCategory:'Category', eventAction:'Action', eventLabel:'Label', eventValue:'Value'})` 
Label and Value are optional

To track a Page:
* `window.Frontier.pageTrack({title:'Page Title', location:'Page URL',page:'Page')`

To track an App:
* `window.Frontier.appTrack({appName: 'App Name', appID: 'XXXX-YYY-ZZZ',appVersion:'1.0.0',appInstallerID: 'XXX-YY-1.0.0'})`

To track a Device:
* `window.Frontier.deviceTrack({deviceID:'deviceID',deviceName:'deviceName', deviceBrand:'deviceBrand',deviceModel:'deviceModel',osName:'osName',osVersion:'osVersion',screenResolution:'screenResolution',serviceProvider:'serviceProvider'})` 

To set a UserId:
* `window.Frontier.setUserId('my-user-id')`
Note:  'my-user-id' must in a string form or type of string even its a number, decimal and other numeric figure

To enable verbose logging:
* `window.Frontier.enableAppDebugging(true)` set true to enable debugging mode, default: false

To enable Event Tracking:
* `window.Frontier.enableTrackEvent(true)` set true to enable Event Tracking, default: false

To enable Page Tracking:
* `window.Frontier.enableTrackPage(true)` set true to enable Page Tracking, default: false

To enable View / Screen Tracking:
* `window.Frontier.enableTrackView(true)` set true to enable View / Screen Tracking, default: false

To enable App Tracking:
* `window.Frontier.enableTrackApp(true)` set true to enable App Tracking, default: false

To enable Device Tracking:
* `window.Frontier.enableTrackDevice(true)` set true to enable Device Tracking, default: false

To get View Port Size:
* `window.Frontier.getViewPortSize()`

To get Screen Resolution:
* `window.Frontier.getScreenResolution()`

To get Screen Color Depth:
* `window.Frontier.getScreenColorDepth()`

To get Language:
* `window.Frontier.getLanguage()`

To get Operating System Info:
* `window.Frontier.getOperatingSystem()`

To get Operating System Version:
* `window.Frontier.getOperatingSystemVersion()`

To get Device Unique ID:
* `window.Frontier.getDeviceID()`

To get Device Name:
* `window.Frontier.getDeviceName()`

To get Device Model:
* `window.Frontier.getDeviceModel()`

To get Device Brand:
* `window.Frontier.getDeviceBrand()`

To get App ID:
* `window.Frontier.getAppID()`

To get App Name:
* `window.Frontier.getAppName()`

To get App Version:
* `window.Frontier.getAppVersion()`

To get / check if Frontier is initialized:
* `window.Frontier.getInitialized()`
