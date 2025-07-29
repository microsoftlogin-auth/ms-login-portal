# Microsoft-Phishing-Campaign
A ready-to-use Microsoft login page for Gophish

This folder includes solutions to challenges I’ve faced while designing phishing campaigns with appropriate permissions:

1.	A current and operational Microsoft login page.
2.	Compatibility between .html and .js files to enable Gophish to capture credentials.
3.	A resolution to the inherent issue of redirections:

In the Gophish HTML, you need to ensure the following in order to capture credentials and redirect:

•	Set the action to an empty string (“”)
•	Set the method to “POST”
•	Ensure the input elements have a “name” attribute.

The issue arises when you apply these settings to both Microsoft login screens (the email input screen with “next” button and the credential input screen with “sign in” button). If the redirection option is enabled on the Gophish server, it redirects you after the first screen, not allowing you to enter passwords.


In order for this to work with Gophish, remember to:
1. Put the assets in /static/endpoint.
2. Change the HTML for each and every asset from assets/everyasset to boughtdomain.com/static/everyasset.
3. Set the landing page to capture credentials.
4. Set the landing page to redirect.

