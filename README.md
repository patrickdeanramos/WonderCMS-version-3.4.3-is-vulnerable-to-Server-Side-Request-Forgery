# WonderCMS-version-3.4.3-is-vulnerable-to-Server-Side-Request-Forgery-SSRF-
WonderCMS version 3.4.3 is vulnerable to Server-Side Request Forgery (SSRF), allowing an attacker to make requests to unauthorized internal resources through the pluginThemeUrl parameter on the Plugins Page.

<B>Reproduction:</B> 
1. Log in to the admin page.
2. Click on 'Themes' and input http://127.0.0.1:9999 in the custom module field.
3. On the machine where WonderCMS is hosted, start an HTTP server on port 9999. In this example, we use the Python SimpleHTTPServer module.
4. Click 'Add', enter the administrator password, and verify that the request was successful.

Authors:<br>
Patrick Dean Ramos<br>
Nathu Nandwani<br>
Junnair Manla<br>
Kevin Rosales<br>
