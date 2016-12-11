# One Signal

[![npm](https://img.shields.io/npm/v/onesignal.svg)](https://www.npmjs.com/package/onesignal)
[![npm](https://img.shields.io/npm/l/onesignal.svg)](https://github.com/faressoft/onesignal/blob/master/LICENSE)

<p align="center">
![Logo](/logo.png?raw=true)
</p>

<p align="center">
A Wrapper for   [OneSignal](https://onesignal.com) Push Notification Delivery for Node.js. Provides the minimal functionality to send notifications for **iOS** and **Android**.
</p>

# Installation

```
npm install onesignal --save
```

# Usage

```js
// Create a client object
var oneSignal = require('onesignal')('[apiKey]', '[appID]', true);
```

## OneSignal(apiKey, appID, sandbox)
One Signal Client

| Param | Type | Description |
| --- | --- | --- |
| apiKey | <code>String</code> | REST API Key |
| appID | <code>String</code> | OneSignal App ID |
| sandbox | <code>Boolean</code> | use the sandbox certificate for iOS (default: false) |

## Methods

<dl>
<dt><a href="#addDevice">addDevice(identifier, osType)</a> ⇒ <code>Promise</code></dt>
<dd><p>Register a new device and its identifier to OneSignal and get OneSignal ID</p></dd>
<dt><a href="#editDevice">editDevice(oneSignalId, newIdentifier)</a> ⇒ <code>Promise</code></dt>
<dd><p>Update the identifier of an existing device</p></dd>
<dt><a href="#createNotification">createNotification(message, data, oneSignalIds)</a> ⇒ <code>Promise</code></dt>
<dd><p>Create and send a notification</p></dd>
</dl>

<a name="addDevice"></a>

### addDevice(identifier, osType) ⇒ <code>Promise</code>
Register a new device and its identifier to OneSignal and get OneSignal ID.

**Returns**: <code>Promise</code> - resolve with OneSignal ID  

| Param | Type | Description |
| --- | --- | --- |
| identifier | <code>String</code> | the device token |
| osType | <code>String</code> | ios, android |

<a name="editDevice"></a>

### editDevice(oneSignalId, newIdentifier) ⇒ <code>Promise</code>
Update the identifier of an existing device.


| Param | Type | Description |
| --- | --- | --- |
| oneSignalId | <code>String</code> | the one signal device id |
| newIdentifier | <code>String</code> | the new device token |

<a name="createNotification"></a>

### createNotification(message, data, oneSignalIds) ⇒ <code>Promise</code>
Create and send a notification.


| Param | Type |
| --- | --- |
| message | <code>String</code> | 
| data | <code>Object</code> | 
| oneSignalIds | <code>Array</code> | 

# License

This project is under the MIT license.
