#PatternLock.js
A simple 3kb js script to create Pattern Lock for your web app.

`patrernlock.js` creates a **number combination** based on the patter created by a user, Which can then be used as a _password_/_pin_ to **authorise/Login** a user.

##Why PatternLock?

Simply because it is **easy** and **Fast** to draw pattern than typing a pin.

##Usage

First **Download** the `src/patternlock.js` file.
Then include it into your html file like:

```html
<script src='path/to/patternlock.js></script> //change 'path/to/' to the real folder.
```

Once included, initilise the patternlock by calling `new PatternLock()` function, like this:

```javascript
var patternLock = new PatternLock(
	'canvasId': 'YOUR CANVAS ELEMENT ID' //you must provide the canvas id
	'dotColor': 'COLOR SCHEMA', //Default light green(#00FF26)
	'dotSize': 'NUMBER', //Default 10, Radius of the dots
	'vibrate': 'TRUE OR FALSE', //Default true
	'minJoinDots': 'NUMBER' //Default 3 Dots to be joined for valid pattern
);
```

After that call the method `.creatLock()` to creat the pattern lock, it takes a callback as a parameter.

```javascript
parrernLock.createLock(function(err, comb){
	if(err)
		console.log(err);
	else
		//do something with the combination provided

	});
```

The `callback` function gets two parameters `error` and `combination`. The `combination` is a unique number of the pattern, which then can be used to **authenticate** the user or to set the **New User pattern**.
