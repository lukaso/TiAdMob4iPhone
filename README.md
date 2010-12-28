TiAdMob4iPhone
===========================================

This is a AdMob integration module for Titanium Mobile iPhone.



HOW TO USE IT
-----------------------------

	var window = Ti.UI.createWindow({
	  backgroundColor: '#0000ff'
	});
	
	var Ad = require('jp.masuidrive.ti.admob');
	var admob = Ad.createAdMob({
	    publisher: "Your Publisher ID", // required
	    top: 0,
	    left: 0,
	    width: 320, // required
	    height: 48, // required
	    adBackgroundColor: "#ffffff",
	    primaryTextColor: "#000000",
	    secondaryTextColor: "#000000",
	    refresh: 30.0,
			latitude: 51.0,
			longitude: -0.180,
			locationTime: new Date()
	});
	admob.addEventListener('error', function(error) {
	    alert(error.message);
	    window.remove(admob);
	});
	window.add(admob);
	window.open();


INSTALL TiAdMob4iPhone
--------------------

1. Open `Terminal`
2. Run below command

	`python build.py && unzip jp.masuidrive.ti.admob-iphone-0.1.zip -d /Library/Application\ Support/Titanium/`


REGISTER TO YOUR PROJECT
---------------------

Register your module with your application by editing `tiapp.xml` and adding your module.
Example:

	<modules>
		<module version="0.1">jp.masuidrive.ti.admob</module>
	</modules>

When you run your project, the compiler will know automatically compile in your module
dependencies and copy appropriate image assets into the application.


LICENSE
---------------------
MIT License

Copyright 2010 Yuichiro MASUI (masuidrive)
http://masuidrive.com/
Twitter: @masuidrive_en