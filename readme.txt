[fb sso login]
docs:
https://developers.facebook.com/docs/facebook-login/login-flow-for-web/v2.0 -- with js sdk
https://developers.facebook.com/docs/facebook-login/manually-build-a-login-flow/v2.0 -- manual

1.registe fb app for sso
https://developers.facebook.com/apps/1442730812642323/dashboard/

2.implement sso by java script

	sample url: http://irvingdp2014.azurewebsites.net/fb_sso_login.html

	fb/ping
		'connected' -> Logged into your app and Facebook. -> fb/me
		'not_authorized' -> The person is logged into Facebook, but not your app. -> login process
		else ->The person is not logged into Facebook ->  login process

	login process -> request fb/oauth -> login success -> callback redirect_uri(with token) -> request fb/me by fb_token  ->　get user's public_probile


	fb/ping:
	https://www.facebook.com/connect/ping?client_id=1442732685975469&domain=irvingdp2014.azurewebsites.net&origin=1&redirect_uri=http%3A%2F%2Fstatic.ak.facebook.com%2Fconnect%2Fxd_arbiter%2FdgdTycPTSRj.js%3Fversion%3D41%23cb%3Df141239a5c%26domain%3Dirvingdp2014.azurewebsites.net%26origin%3Dhttp%253A%252F%252Firvingdp2014.azurewebsites.net%252Ff2a20b9594%26relation%3Dparent&response_type=token%2Csigned_request%2Ccode&sdk=joey

	fb/oaut:
	https://www.facebook.com/dialog/oauth?client_id=1442730812642323&display=popup&response_type=token&redirect_uri=https://www.facebook.com/connect/login_success.html

	fb/me
	https://graph.facebook.com/v2.0/me?access_token=CAAUgJZCGYFBMBAPKs2uwiMnYP7J4gGUdocm87nZBfVDZBqYHOHZCSOTiHWcVGpjA8ZC9nnPKQPIUcVFsgBE9nZCyhOmgN5YUZBiVJoukq6ldWH7uflXN8PfZCrcpCZA3bZC1QpmCERacVY8xtP53QpXIJK0YrSt0oXtNXD8zcPiPPlnOlZAjjHVWXbX1JHaZCXBVLBZA96e5lC0FZCiAZDZD


[goolge sso login]
docs:
使用 Google APIs Client Library for JavaScript - https://developers.google.com/api-client-library/javascript/features/authentication?hl=zh-tw
原理 - https://developers.google.com/accounts/docs/OAuth2UserAgent?hl=zh-tw#overview

1.create google project & create OAuth 2.0 API & create publick API access's key 
(google console: https://console.developers.google.com/project/apps~primal-insight-583/apiui/credential?authuser=0)
(教學: http://blog.kenyang.net/2012/09/google-oauth-20-google-api.html)
https://console.developers.google.com/project
	Client ID	66287016993-569ofvd3svmu77d9ig3h4a60l2olkb8j.apps.googleusercontent.com
	Client secret	d7jpuBs3OORk2OyHAxvP8wHD
	api key:AIzaSyACKUbcdy39z2H-kMPiP8vjS2p2TA0W57k

2.implement sso by java script
	sample url: http://irvingdp2014.azurewebsites.net/google_sso_login.html











