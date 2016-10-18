#Frontier

=======================


[<img src="http://fourloopph.bitbucket.org/developers/images/devLogo.png" alt="4LOOP Logo" width="1300px" height="192px" />](http://fourloopph.bitbucket.org/developers/)


Frontier SDK to connect to Frontier's Analytics API


## Installing

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
<script src="https://cdn.rawgit.com/4LOOPph/frontier/v1.0.15/dist/frontier.js"></script>
or
<script src="https://cdn.rawgit.com/4LOOPph/frontier/v1.0.15/dist/frontier.min.js"></script>
```
**Note**:  frontier for  **LOCAL**  is not safe and usable for production nor staging test.

#### JavaScript Usage
In your 'deviceready' handler, set up your Frontier tracker:
```js
	/*
		PARAMETERS
		@accessCode - string
		@trackerName - string
		@encoding - string
	*/

	window.Frontier.Initialize({
		 accessCode: 'XXXXXXXXXXXXXXX',
		 trackerName: 'tracker-name',
		 encoding: 'utf-8'
	});
```
where XXXXXXXXXXXXXXX is your ** Symphony Access Code** base on your subscription

#### To enable verbose logging:
```js
	window.Frontier.enableAppDebugging(true);
```
**Note**: set true to enable debugging mode, default: false
If set to a truthy value then debugging mode is enabled with Frontier.
All trackers with `isEnableDebugging: true` will enable for debugging mode.

#### To enable Event Tracking:
```js
	window.Frontier.enableTrackEvent(true);
```
**Note**: set true to enable Event Tracking, default: false
If set to a truthy value then the event tracking is enable with Frontier Analytics.
All trackers with `IsEnableTrackEvent: true` will enable for Event Tracking with Frontier.

#### To enable Page Tracking:
```js
	window.Frontier.enableTrackPage(true)
```
**Note**: set true to enable Page Tracking, default: false
If set to a truthy value then the page tracking is enable with Frontier Analytics.
All trackers with `IsEnableTrackPage: true` will enable for Page Tracking with Frontier.

#### To enable View / Screen Tracking:
```js
window.Frontier.enableTrackView(true)
```
**Note**: set true to enable View / Screen Tracking, default: false
If set to a truthy value then the event tracking is enable with Frontier Analytics.
All trackers with `IsEnableTrackView: true` will enable for View/Screen Tracking with Frontier.

#### To enable App Tracking:
```js
	window.Frontier.enableTrackApp(true)
```
**Note**: set true to enable App Tracking, default: false
If set to a truthy value then the event tracking is enable with Frontier Analytics.
All trackers with `IsEnableTrackApp: true` will enable for App Tracking with Frontier.

#### To enable Device Tracking:
```js
	window.Frontier.enableTrackDevice(true)
```
**Note**: set true to enable Device Tracking, default: false
If set to a truthy value then the event tracking is enable with Frontier Analytics.
All trackers with `IsEnableTrackDevice: true` will enable for Device Tracking with Frontier.

#### To track a Screen (View):
```js
	/*
		PARAMETERS
		@screenName - string
	*/

	window.Frontier.screenTrack({
		screenName:'Screen Title'
	});
```

#### To track an Event:
```js
	/*
		PARAMETERS
		@category - string
		@action - string
		@label - string
		@value - integer
	*/
	window.Frontier.eventTrack({
		eventCategory:'Category',
		eventAction:'Action',
		eventLabel:'Label',
		eventValue:'Value'
	});
```
**Note**: eventLabel and eventValue are optional

#### To track a Page:
```js
	/*
		PARAMETERS
		@title - string
		@location - string
		@page - string
	*/

	window.Frontier.pageTrack({
		title:'Page Title',
		location:'Page URL',
		page:'Page'
	});
```

#### To track an App:
```js
	/*
		PARAMETERS
		@appName - string
		@appID - string
		@appVersion - string
		@appInstallerID -  stirng
	*/

	window.Frontier.appTrack({
		appName: 'App Name',
		appID: 'XXXX-YYY-ZZZ',
		appVersion:'1.0.0',
		appInstallerID: 'XXX-YY-1.0.0'
	});
```

#### To track a Device:
```js
	/*
		PARAMETERS
		@deviceID - string
		@deviceName - string
		@deviceBrand - string
		@deviceModel - string
		@osName - string
		@osVersion - string
		@screenResolution - string
		@serviceProvider - string
	*/

	window.Frontier.deviceTrack({
		deviceID:'deviceID',
		deviceName:'deviceName',
		deviceBrand:'deviceBrand',
		deviceModel:'deviceModel',
		osName:'osName',
		osVersion:'osVersion',
		screenResolution:'screenResolution',
		serviceProvider:'serviceProvider'
	});
```

#### To set a UserId:
```js
	/*
		PARAMETERS
		@userId - string
	*/
	window.Frontier.setUserId('userId')
```
**Note**:  'userId' must in a string form or type of string even its a number, decimal and other numeric figure

#### To get View Port Size:
```js
	window.Frontier.getViewPortSize()
```

#### To get Screen Resolution:
```js
	window.Frontier.getScreenResolution()
```

#### To get Screen Color Depth:
```js
	window.Frontier.getScreenColorDepth()
```

#### To get Language:
```js
	window.Frontier.getLanguage()
```

#### To get Operating System Info:
```js
	window.Frontier.getOperatingSystem()
```

#### To get Operating System Version:
```js
	window.Frontier.getOperatingSystemVersion()
```

#### To get Device Unique ID:
```js
	window.Frontier.getDeviceID()
```

#### To get Device Name:
```js
	window.Frontier.getDeviceName()
```

#### To get Device Model:
```js
	window.Frontier.getDeviceModel()
```

#### To get Device Brand:
```js
	window.Frontier.getDeviceBrand()
```

#### To get App ID:
```js
window.Frontier.getAppID()
```

#### To get App Name:
```js
	window.Frontier.getAppName()
```

#### To get App Version:
```js
	window.Frontier.getAppVersion()
```

#### To get / check if Frontier is initialized:
```js
	window.Frontier.getInitialized()
```

#### To reset Analytics settings
```js
	window.Frontier.Reset()
```
**Note**: Use Analytics Reset when you want to clear Analytics cache. This means everything on analytics initialization is cleared and a browser reload/refresh is required

#### To signout Analytics Session
```js
window.Frontier.signOut()
```
**Note:** Use Analytics Signout when you want to signout Analytics active session. This means everything on analytics current session will be stop and resetted.  You can use this feature on your application authentication.
