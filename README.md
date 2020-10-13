# SSO-Components
This is the code required to integrate a php app into Trogy.NZ Single Sign On.

Designed to work with The Trogy.NZ Framework you can probably find a way to crowbar this into your software*

Trogy.NZ SSO is not yet availible please check back at a later date for instructions on how to use the API.

*Requires Valid Software API Key in addition to a developer level account at trogy.nz

--Below is some theory this is NOT the final design in any way--

Login Requests

1. Send the API your App key
2. SSO will send a one time request key
3. Send user to login page with request key
4. SSO will send user back with authenticated login token.

Polling Login Status
*Checking a users login is YOUR responsibility Trogy.NZ will impose NO limits on checking a users login as long as you have the users token and your app key all other requests will be 403

1. Send API Login Token, User Token and App Key
2. API will respond with "VALID" or "INVALID" (SSO will never give the reason your request was rejected unless it was a bug)

Setup
//Both versions on the setup requre the same setup from you but how SSO responds is different depending on what the user chooses you will need to take this into account in your code

Online


