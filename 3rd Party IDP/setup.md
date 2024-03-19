Use your choice of a third-party identity provider solution for agents to log in to Voice from the Omni-Channel widget. 
For example, if your Salesforce org uses Microsoft Azure as an identity provider, you can configure your contact center to require agents to log in and out of the Azure single sign-on page from Omni-Channel.

Where: This change applies to Lightning Experience in Enterprise and Unlimited editions. Available in Salesforce orgs with these telephony Models
  Service Cloud Voice with Amazon Connect
  Service Cloud Voice with Partner Telephony from Amazon Connect
  
How: In the contact center details page, configure your third-party identity provider.

When you click Telephony Settings on the contact center details page, the third-party identity provider logs you in to Amazon Connect.
When an agent sets themselves as available in the Omni-Channel widget, the identity provider logs them in to Amazon Connect behind the scenes.

You Can configure Relay State URL and Identity URL in callCenter xml file as show below 
![1709412131252](https://github.com/sujaicus/aws-connect-scv/assets/82329822/6709b32f-5445-40e9-a338-2ee100230da0)


[Uplo<items>
  <label>Relay State</label>
  <name>reqRelayState</name>
  <value>https://us-east-1.console.aws.amazon.com/connect/federate/XXXX</value>
</items>
<items>
  <label>Identity URL</label>
  <name>reqIdentityUrl</name>
  <value>https://launcher.myapps.microsoft.com/api/signin/XXXX</value>
</items>ading callcenter.xml…]()


<items>
  <label>Relay State</label>
  <name>reqRelayState</name>
  <value>https://us-east-1.console.aws.amazon.com/connect/federate/XXXX</value>
</items>
<items>
  <label>Identity URL</label>
  <name>reqIdentityUrl</name>
  <value>https://launcher.myapps.microsoft.com/api/signin/XXXX</value>
</items>

Ensure to Enable , Third Party IDP and SSO Login Pop Up Window to true in callCenter xml file as show below
<items>
  <label>Third Party IDP</label>
  <name>reqThirdPartyIDP</name>
  <value>true</value>
</items>
<items>
  <label>SSO Login Popup Window</label>
  <name>reqSSOLoginPopupWindow</name>
  <value>true</value>
</items>
