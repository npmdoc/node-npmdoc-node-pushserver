# api documentation for  [node-pushserver (v0.5.4)](https://github.com/Smile-SA/node-pushserver)  [![npm package](https://img.shields.io/npm/v/npmdoc-node-pushserver.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-node-pushserver) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-node-pushserver.svg)](https://travis-ci.org/npmdoc/node-npmdoc-node-pushserver)
#### Cross-platform Push Notifications. A project providing a generic API to push messages using Apple's APN and Google's GCM services.

[![NPM](https://nodei.co/npm/node-pushserver.png?downloads=true)](https://www.npmjs.com/package/node-pushserver)

[![apidoc](https://npmdoc.github.io/node-npmdoc-node-pushserver/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-node-pushserver_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-node-pushserver/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-node-pushserver/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-node-pushserver/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bin": {
        "pushserver": "./bin/pushserver.js"
    },
    "bugs": {
        "url": "https://github.com/Smile-SA/node-pushserver/issues"
    },
    "dependencies": {
        "apn": "~1.3.4",
        "commander": "2.7.1",
        "express": "~3.2.6",
        "lodash": "~1.3.1",
        "mongoose": "~3.6.11",
        "node-gcm": "~0.9.6"
    },
    "description": "Cross-platform Push Notifications. A project providing a generic API to push messages using Apple's APN and Google's GCM services.",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "5a1de6131c55f5e3e897c1c130e58e1fbf99e603",
        "tarball": "https://registry.npmjs.org/node-pushserver/-/node-pushserver-0.5.4.tgz"
    },
    "gitHead": "19b7c37d4ca23a1d2782faa5bc0ed4b6c80051c9",
    "homepage": "https://github.com/Smile-SA/node-pushserver",
    "keywords": [
        "push",
        "gcm",
        "apn",
        "mongodb"
    ],
    "main": "./lib/PushController.js",
    "maintainers": [
        {
            "name": "smile",
            "email": "pole.mobile@smile.fr"
        }
    ],
    "name": "node-pushserver",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/Smile-SA/node-pushserver.git"
    },
    "scripts": {
        "start": "node ./bin/pushserver.js",
        "test": "echo \"Error: no test specified\" && exit 1"
    },
    "version": "0.5.4"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module node-pushserver](#apidoc.module.node-pushserver)
1.  [function <span class="apidocSignatureSpan">node-pushserver.</span>send (pushAssociations, androidPayload, iosPayload)](#apidoc.element.node-pushserver.send)
1.  [function <span class="apidocSignatureSpan">node-pushserver.</span>sendUsers (users, payload)](#apidoc.element.node-pushserver.sendUsers)
1.  [function <span class="apidocSignatureSpan">node-pushserver.</span>subscribe (deviceInfo)](#apidoc.element.node-pushserver.subscribe)
1.  [function <span class="apidocSignatureSpan">node-pushserver.</span>unsubscribeDevice (deviceToken)](#apidoc.element.node-pushserver.unsubscribeDevice)
1.  [function <span class="apidocSignatureSpan">node-pushserver.</span>unsubscribeUser (user)](#apidoc.element.node-pushserver.unsubscribeUser)
1.  object <span class="apidocSignatureSpan">node-pushserver.</span>APNPusher
1.  object <span class="apidocSignatureSpan">node-pushserver.</span>Config
1.  object <span class="apidocSignatureSpan">node-pushserver.</span>GCMPusher
1.  object <span class="apidocSignatureSpan">node-pushserver.</span>PushAssociations
1.  object <span class="apidocSignatureSpan">node-pushserver.</span>Web

#### [module node-pushserver.APNPusher](#apidoc.module.node-pushserver.APNPusher)
1.  [function <span class="apidocSignatureSpan">node-pushserver.APNPusher.</span>buildPayload (options)](#apidoc.element.node-pushserver.APNPusher.buildPayload)
1.  [function <span class="apidocSignatureSpan">node-pushserver.APNPusher.</span>push (tokens, payload)](#apidoc.element.node-pushserver.APNPusher.push)

#### [module node-pushserver.Config](#apidoc.module.node-pushserver.Config)
1.  [function <span class="apidocSignatureSpan">node-pushserver.Config.</span>get (key)](#apidoc.element.node-pushserver.Config.get)
1.  [function <span class="apidocSignatureSpan">node-pushserver.Config.</span>initialize ()](#apidoc.element.node-pushserver.Config.initialize)

#### [module node-pushserver.GCMPusher](#apidoc.module.node-pushserver.GCMPusher)
1.  [function <span class="apidocSignatureSpan">node-pushserver.GCMPusher.</span>buildPayload (options)](#apidoc.element.node-pushserver.GCMPusher.buildPayload)
1.  [function <span class="apidocSignatureSpan">node-pushserver.GCMPusher.</span>push (tokens, message)](#apidoc.element.node-pushserver.GCMPusher.push)

#### [module node-pushserver.PushAssociations](#apidoc.module.node-pushserver.PushAssociations)
1.  [function <span class="apidocSignatureSpan">node-pushserver.PushAssociations.</span>add ()](#apidoc.element.node-pushserver.PushAssociations.add)
1.  [function <span class="apidocSignatureSpan">node-pushserver.PushAssociations.</span>getAll ()](#apidoc.element.node-pushserver.PushAssociations.getAll)
1.  [function <span class="apidocSignatureSpan">node-pushserver.PushAssociations.</span>getForUser ()](#apidoc.element.node-pushserver.PushAssociations.getForUser)
1.  [function <span class="apidocSignatureSpan">node-pushserver.PushAssociations.</span>getForUsers ()](#apidoc.element.node-pushserver.PushAssociations.getForUsers)
1.  [function <span class="apidocSignatureSpan">node-pushserver.PushAssociations.</span>removeDevice ()](#apidoc.element.node-pushserver.PushAssociations.removeDevice)
1.  [function <span class="apidocSignatureSpan">node-pushserver.PushAssociations.</span>removeDevices ()](#apidoc.element.node-pushserver.PushAssociations.removeDevices)
1.  [function <span class="apidocSignatureSpan">node-pushserver.PushAssociations.</span>removeForUser ()](#apidoc.element.node-pushserver.PushAssociations.removeForUser)
1.  [function <span class="apidocSignatureSpan">node-pushserver.PushAssociations.</span>updateTokens ()](#apidoc.element.node-pushserver.PushAssociations.updateTokens)

#### [module node-pushserver.Web](#apidoc.module.node-pushserver.Web)
1.  [function <span class="apidocSignatureSpan">node-pushserver.Web.</span>start ()](#apidoc.element.node-pushserver.Web.start)



# <a name="apidoc.module.node-pushserver"></a>[module node-pushserver](#apidoc.module.node-pushserver)

#### <a name="apidoc.element.node-pushserver.send"></a>[function <span class="apidocSignatureSpan">node-pushserver.</span>send (pushAssociations, androidPayload, iosPayload)](#apidoc.element.node-pushserver.send)
- description and source-code
```javascript
send = function (pushAssociations, androidPayload, iosPayload) {
    var androidTokens = _(pushAssociations).where({type: 'android'}).map('token').value();
    var iosTokens = _(pushAssociations).where({type: 'ios'}).map('token').value();

    if (androidPayload && androidTokens.length > 0) {
        var gcmPayload = gcmPusher.buildPayload(androidPayload);
        gcmPusher.push(androidTokens, gcmPayload);
    }

    if (iosPayload && iosTokens.length > 0) {
        var apnPayload = apnPusher.buildPayload(iosPayload);
        apnPusher.push(iosTokens, apnPayload);
    }
}
```
- example usage
```shell
...
var config = require('./Config')
var _ = require('lodash');
var gcm = require('node-gcm');
var pushAssociations = require('./PushAssociations');


var push = function (tokens, message) {
    gcmSender().send(message, tokens, 4, function (err, res) {
if(err) console.log(err);

if (res) {
    var mappedResults = _.map(_.zip(tokens, res.results), function (arr) {
        return _.merge({token: arr[0]}, arr[1]);
    });
...
```

#### <a name="apidoc.element.node-pushserver.sendUsers"></a>[function <span class="apidocSignatureSpan">node-pushserver.</span>sendUsers (users, payload)](#apidoc.element.node-pushserver.sendUsers)
- description and source-code
```javascript
sendUsers = function (users, payload) {
    pushAssociations.getForUsers(users, function (err, pushAss) {
        if (err) return;
        send(pushAss, payload);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-pushserver.subscribe"></a>[function <span class="apidocSignatureSpan">node-pushserver.</span>subscribe (deviceInfo)](#apidoc.element.node-pushserver.subscribe)
- description and source-code
```javascript
subscribe = function (deviceInfo) {
    pushAssociations.add(deviceInfo.user, deviceInfo.type, deviceInfo.token);
}
```
- example usage
```shell
...
    res.status(406).send();
}
});

// Main API
app.post('/subscribe', function (req, res) {
var deviceInfo = req.body;
push.subscribe(deviceInfo);

res.send();
});

app.post('/unsubscribe', function (req, res) {
var data = req.body;
...
```

#### <a name="apidoc.element.node-pushserver.unsubscribeDevice"></a>[function <span class="apidocSignatureSpan">node-pushserver.</span>unsubscribeDevice (deviceToken)](#apidoc.element.node-pushserver.unsubscribeDevice)
- description and source-code
```javascript
unsubscribeDevice = function (deviceToken) {
    pushAssociations.removeDevice(deviceToken);
}
```
- example usage
```shell
...

app.post('/unsubscribe', function (req, res) {
    var data = req.body;

    if (data.user) {
        push.unsubscribeUser(data.user);
    } else if (data.token) {
        push.unsubscribeDevice(data.token);
    } else {
        return res.status(503).send();
    }

    res.send();
});
...
```

#### <a name="apidoc.element.node-pushserver.unsubscribeUser"></a>[function <span class="apidocSignatureSpan">node-pushserver.</span>unsubscribeUser (user)](#apidoc.element.node-pushserver.unsubscribeUser)
- description and source-code
```javascript
unsubscribeUser = function (user) {
    pushAssociations.removeForUser(user);
}
```
- example usage
```shell
...
res.send();
});

app.post('/unsubscribe', function (req, res) {
var data = req.body;

if (data.user) {
    push.unsubscribeUser(data.user);
} else if (data.token) {
    push.unsubscribeDevice(data.token);
} else {
    return res.status(503).send();
}

res.send();
...
```



# <a name="apidoc.module.node-pushserver.APNPusher"></a>[module node-pushserver.APNPusher](#apidoc.module.node-pushserver.APNPusher)

#### <a name="apidoc.element.node-pushserver.APNPusher.buildPayload"></a>[function <span class="apidocSignatureSpan">node-pushserver.APNPusher.</span>buildPayload (options)](#apidoc.element.node-pushserver.APNPusher.buildPayload)
- description and source-code
```javascript
buildPayload = function (options) {
    var notif = new apn.Notification(options.payload);

    notif.expiry = options.expiry || 0;
    notif.alert = options.alert;
    notif.badge = options.badge;
    notif.sound = options.sound;

    return notif;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-pushserver.APNPusher.push"></a>[function <span class="apidocSignatureSpan">node-pushserver.APNPusher.</span>push (tokens, payload)](#apidoc.element.node-pushserver.APNPusher.push)
- description and source-code
```javascript
push = function (tokens, payload) {
    apnSender().pushNotification(payload, tokens);
}
```
- example usage
```shell
...

var handleResults = function (results) {
var idsToUpdate = [],
    idsToDelete = [];

results.forEach(function (result) {
    if (!!result.registration_id) {
        idsToUpdate.push({from: result.token, to: result.registration_id});

    } else if (result.error === 'InvalidRegistration' || result.error === 'NotRegistered') {
        idsToDelete.push(result.token);
    }
});

if (idsToUpdate.length > 0) pushAssociations.updateTokens(idsToUpdate);
...
```



# <a name="apidoc.module.node-pushserver.Config"></a>[module node-pushserver.Config](#apidoc.module.node-pushserver.Config)

#### <a name="apidoc.element.node-pushserver.Config.get"></a>[function <span class="apidocSignatureSpan">node-pushserver.Config.</span>get (key)](#apidoc.element.node-pushserver.Config.get)
- description and source-code
```javascript
get = function (key) {
    if (!config) initialize('../config.json');
    return config[key];
}
```
- example usage
```shell
...
    notif.badge = options.badge;
    notif.sound = options.sound;

    return notif;
};

var apnSender = _.once(function () {
    var apnConnection = new apn.Connection(config.get('apn').connection);

    apnConnection.on('transmissionError', onTransmissionError);
    initAppFeedback();

    return apnConnection;
});
...
```

#### <a name="apidoc.element.node-pushserver.Config.initialize"></a>[function <span class="apidocSignatureSpan">node-pushserver.Config.</span>initialize ()](#apidoc.element.node-pushserver.Config.initialize)
- description and source-code
```javascript
initialize = function () {
  if (ran) {
    return result;
  }
  ran = true;
  result = func.apply(this, arguments);

  // clear the 'func' variable so the function may be garbage collected
  func = null;
  return result;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.node-pushserver.GCMPusher"></a>[module node-pushserver.GCMPusher](#apidoc.module.node-pushserver.GCMPusher)

#### <a name="apidoc.element.node-pushserver.GCMPusher.buildPayload"></a>[function <span class="apidocSignatureSpan">node-pushserver.GCMPusher.</span>buildPayload (options)](#apidoc.element.node-pushserver.GCMPusher.buildPayload)
- description and source-code
```javascript
buildPayload = function (options) {
    return new gcm.Message(options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-pushserver.GCMPusher.push"></a>[function <span class="apidocSignatureSpan">node-pushserver.GCMPusher.</span>push (tokens, message)](#apidoc.element.node-pushserver.GCMPusher.push)
- description and source-code
```javascript
push = function (tokens, message) {
    gcmSender().send(message, tokens, 4, function (err, res) {
        if(err) console.log(err);

        if (res) {
            var mappedResults = _.map(_.zip(tokens, res.results), function (arr) {
                return _.merge({token: arr[0]}, arr[1]);
            });

            handleResults(mappedResults);
        }
    })
}
```
- example usage
```shell
...

var handleResults = function (results) {
var idsToUpdate = [],
    idsToDelete = [];

results.forEach(function (result) {
    if (!!result.registration_id) {
        idsToUpdate.push({from: result.token, to: result.registration_id});

    } else if (result.error === 'InvalidRegistration' || result.error === 'NotRegistered') {
        idsToDelete.push(result.token);
    }
});

if (idsToUpdate.length > 0) pushAssociations.updateTokens(idsToUpdate);
...
```



# <a name="apidoc.module.node-pushserver.PushAssociations"></a>[module node-pushserver.PushAssociations](#apidoc.module.node-pushserver.PushAssociations)

#### <a name="apidoc.element.node-pushserver.PushAssociations.add"></a>[function <span class="apidocSignatureSpan">node-pushserver.PushAssociations.</span>add ()](#apidoc.element.node-pushserver.PushAssociations.add)
- description and source-code
```javascript
add = function () {
    if (_.isUndefined(PushAssociation)) {
        initialize();
    }

    return func.apply(null, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-pushserver.PushAssociations.getAll"></a>[function <span class="apidocSignatureSpan">node-pushserver.PushAssociations.</span>getAll ()](#apidoc.element.node-pushserver.PushAssociations.getAll)
- description and source-code
```javascript
getAll = function () {
    if (_.isUndefined(PushAssociation)) {
        initialize();
    }

    return func.apply(null, arguments);
}
```
- example usage
```shell
...
    } else {
        res.status(503).send();
    }
});
});

app.get('/users', function (req, res) {
pushAssociations.getAll(function (err, pushAss) {
    if (!err) {
        var users = _(pushAss).map('user').unique().value();
        res.send({
            "users": users
        });
    } else {
        res.status(503).send()
...
```

#### <a name="apidoc.element.node-pushserver.PushAssociations.getForUser"></a>[function <span class="apidocSignatureSpan">node-pushserver.PushAssociations.</span>getForUser ()](#apidoc.element.node-pushserver.PushAssociations.getForUser)
- description and source-code
```javascript
getForUser = function () {
    if (_.isUndefined(PushAssociation)) {
        initialize();
    }

    return func.apply(null, arguments);
}
```
- example usage
```shell
...
    var notificationsValid = sendNotifications(notifs);

    res.status(notificationsValid ? 200 : 400).send();
});

// Utils API
app.get('/users/:user/associations', function (req, res) {
    pushAssociations.getForUser(req.params.user, function (err, items) {
        if (!err) {
            res.send({"associations": items});
        } else {
            res.status(503).send();
        }
    });
});
...
```

#### <a name="apidoc.element.node-pushserver.PushAssociations.getForUsers"></a>[function <span class="apidocSignatureSpan">node-pushserver.PushAssociations.</span>getForUsers ()](#apidoc.element.node-pushserver.PushAssociations.getForUsers)
- description and source-code
```javascript
getForUsers = function () {
    if (_.isUndefined(PushAssociation)) {
        initialize();
    }

    return func.apply(null, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-pushserver.PushAssociations.removeDevice"></a>[function <span class="apidocSignatureSpan">node-pushserver.PushAssociations.</span>removeDevice ()](#apidoc.element.node-pushserver.PushAssociations.removeDevice)
- description and source-code
```javascript
removeDevice = function () {
    if (_.isUndefined(PushAssociation)) {
        initialize();
    }

    return func.apply(null, arguments);
}
```
- example usage
```shell
...
var onTransmissionError = function (errorCode, notification, recipient) {
console.error('Error while pushing to APN: ' + errorCode);
// Invalid token => remove device
if (errorCode === 8) {
    var token = recipient.token.toString('hex').toUpperCase();

    console.log('Invalid token: removing device ' + token);
    pushAssociations.removeDevice(token);
}
};

var onFeedback = function (deviceInfos) {
console.log('Feedback service, number of devices to remove: ' + deviceInfos.length);

pushAssociations.removeDevices(deviceInfos.map(function (deviceInfo) {
...
```

#### <a name="apidoc.element.node-pushserver.PushAssociations.removeDevices"></a>[function <span class="apidocSignatureSpan">node-pushserver.PushAssociations.</span>removeDevices ()](#apidoc.element.node-pushserver.PushAssociations.removeDevices)
- description and source-code
```javascript
removeDevices = function () {
    if (_.isUndefined(PushAssociation)) {
        initialize();
    }

    return func.apply(null, arguments);
}
```
- example usage
```shell
...
    pushAssociations.removeDevice(token);
}
};

var onFeedback = function (deviceInfos) {
console.log('Feedback service, number of devices to remove: ' + deviceInfos.length);

pushAssociations.removeDevices(deviceInfos.map(function (deviceInfo) {
    return deviceInfo.token.toString('hex');
}));
};

var initAppFeedback = function () {
var apnFeedback = new apn.Feedback(config.get('apn').feedback)
...
```

#### <a name="apidoc.element.node-pushserver.PushAssociations.removeForUser"></a>[function <span class="apidocSignatureSpan">node-pushserver.PushAssociations.</span>removeForUser ()](#apidoc.element.node-pushserver.PushAssociations.removeForUser)
- description and source-code
```javascript
removeForUser = function () {
    if (_.isUndefined(PushAssociation)) {
        initialize();
    }

    return func.apply(null, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-pushserver.PushAssociations.updateTokens"></a>[function <span class="apidocSignatureSpan">node-pushserver.PushAssociations.</span>updateTokens ()](#apidoc.element.node-pushserver.PushAssociations.updateTokens)
- description and source-code
```javascript
updateTokens = function () {
    if (_.isUndefined(PushAssociation)) {
        initialize();
    }

    return func.apply(null, arguments);
}
```
- example usage
```shell
...
            idsToUpdate.push({from: result.token, to: result.registration_id});

        } else if (result.error === 'InvalidRegistration' || result.error === 'NotRegistered') {
            idsToDelete.push(result.token);
        }
    });

    if (idsToUpdate.length > 0) pushAssociations.updateTokens(idsToUpdate);
    if (idsToDelete.length > 0) pushAssociations.removeDevices(idsToDelete);
};

var buildPayload = function (options) {
    return new gcm.Message(options);
};
...
```



# <a name="apidoc.module.node-pushserver.Web"></a>[module node-pushserver.Web](#apidoc.module.node-pushserver.Web)

#### <a name="apidoc.element.node-pushserver.Web.start"></a>[function <span class="apidocSignatureSpan">node-pushserver.Web.</span>start ()](#apidoc.element.node-pushserver.Web.start)
- description and source-code
```javascript
start = function () {
    app.listen(config.get('webPort'));
    console.log('Listening on port ' + config.get('webPort') + "...");
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
