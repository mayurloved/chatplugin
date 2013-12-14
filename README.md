cordova-plugin-hipmob-android
---------------------------
The Hipmob Cordova plugin for Android provides Phonegap applications access to helpdesk, live chat and support CRM tools using the Hipmob platform. For more information visit https://www.hipmob.com.

It is compatible with Android 2.1 and higher, and works on versions of Cordova greater than 2.9.0.

Installation
---------------------------
Install the plugin using the Cordova command-line interface:

    cordova plugin add https://github.com/mayurloved/chatplugin.git

Usage
---------------------------
To use the Hipmob library, you'll need to get a free account at https://www.hipmob.com/. Once you have an account, visit https://manage.hipmob.com/#apps to get your application ID. You can then open a support chat window from a button:

    if( window.plugins && window.plugins.Hipmob ) {
        var hipmob_app_id = '<HIPMOB APPLICATION ID>';           /*this app id will you get when u register on http://hipmob.com*/
        var Hipmob = window.plugins.Hipmob;
    
        Hipmob.openChat(hipmob_app_id, {
	'title': 'Help',
	'user': '<hipmob user id>',									// userwill also get from site
	'name': 'Femi',
	'email': 'femi@hipmob.com',										// same after register
	'context': 'shopping for shoes',
	'location': 'At home'
	});
    } else {
      alert('Hipmob plugin not available/ready.');
    }

To open a helpdesk search window, you can do:

    if( window.plugins && window.plugins.Hipmob ) {
        var hipmob_app_id = '<HIPMOB APPLICATION ID>';
        var Hipmob = window.plugins.Hipmob;
    
        Hipmob.openHelpdeskSearch(hipmob_app_id, {
	'title': 'Help',
	'query': 'Android',
	'user': '<hipmob user id>',
	'name': 'Femi',
	'email': 'femi@hipmob.com',
	'context': 'shopping for shoes',
	'location': 'At home'
	});
    } else {
      alert('Hipmob plugin not available/ready.');
    }
    
To open an instant help window, you can do:

    if( window.plugins && window.plugins.Hipmob ) {
        var hipmob_app_id = '<HIPMOB APPLICATION ID>';
	var helpdesk_article_url = '<helpdesk article url>';
        var Hipmob = window.plugins.Hipmob;
    
        Hipmob.openHelpdeskArticle(hipmob_app_id, helpdesk_article_url, {
	'title': 'Help',
	'user': '<hipmob user id>',
	'name': 'Femi',
	'email': 'femi@hipmob.com',
	'context': 'shopping for shoes',
	'location': 'At home'
	});
    } else {
      alert('Hipmob plugin not available/ready.');
    }