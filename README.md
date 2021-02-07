**Repository Moved**

This repository has moved to [tseward/SchannelConfiguration](https://github.com/tseward/SchannelConfiguration).

# SchannelConfiguration
Configure SChannel Security Settings via Group Policy

# What is this?

A Group Policy file (ADMX) that provides configuration of various SChannel options, for example, disabling SSL 3.0 for IIS.

# How do I use it?

Drop the ADMX and en-Us folder your SYSVOL share, e.g.:

\\\example.com\SYSVOL\example.com\Policies\PolicyDefinitions

You can then edit any Group Policy to add these settings. The SChannel settings are located at Computer Configuration\Poicies\Administrative Templates\Network\SChannel Configuration Settings\.

# Is this best practice?

Well, yes and no. This solution "tatoos" the registry, that is, if you configure a setting and then set it back to "undefined", or remove the policy altogether, the settings will remain on the server(s) to which the policy has been applied. If this is undesirable, then use Group Policy Preferences instead. You will need to manually create the registry entries in the policy definition.

However, if you have a large number of servers, or want to set it and forget it without much work, this is the route to go!
