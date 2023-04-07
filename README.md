# OneSignal

[![npm](https://img.shields.io/npm/v/onesignal.svg)](https://www.npmjs.com/package/onesignal)
[![npm](https://img.shields.io/npm/l/onesignal.svg)](https://github.com/faressoft/onesignal/blob/master/LICENSE)

<p align="center">
<img src="/logo.png?raw=true" alt="OneSignal Logo" height="100" />
</p>

<p align="center">
A Wrapper for <a href="https://onesignal.com">OneSignal</a> Push Notification Delivery for Node.js. Provides the minimal functionality to send notifications for <strong>iOS</strong> and <strong>Android</strong>.
</p>

# Installation

```
npm install onesignal --save
```

# Usage

```js
// Create a client object
var oneSignal = require('onesignal')('[apiKey]', '[appId]', true);
```

## OneSignal(apiKey, appId, sandbox)
OneSignal Client

| Param | Type | Description |
| --- | --- | --- |
| apiKey | <code>String</code> | REST API Key |
| appId | <code>String</code> | OneSignal App ID |
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
| oneSignalId | <code>String</code> | the onesignal device id |
| newIdentifier | <code>String</code> | the new device token |

<a name="createNotification"></a>

### createNotification(message, data, oneSignalIds) ⇒ <code>Promise</code>
Create and send a notification.


| Param | Type | Description |
| --- | --- | --- |
| message | <code>String</code> | the notification message | 
| data | <code>Object</code> | any custom data | 
| oneSignalIds | <code>Array</code> | a list of OneSignal devices ids | 

# License

This project is under the MIT license.
