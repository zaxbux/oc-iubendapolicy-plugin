# Iubenda Policy Cacher
This October CMS plugin allows you to display your Iubenda privacy/cookie policy on your website. The policy is downloaded and cached every day, ensuring the latest version is served to your users, and caching minimizes wait times.

## Requirements
You must have a PRO subscription attached to your privacy policy in order to access the API.

## Plugin Settings
There are only two options to configure. Each time you save the settings, the policy is removed from the cache and downloaded.

### Policy ID
Your Iubenda policy ID, which can be obtained from your embedding code on the Iubenda dashboard.

### Policy Style
How you want your policy to be displayed.
* **Default**: Styled privacy policy
* **Only legal**: Removes icons and most of the CSS
* **No markup**: Similar to 'Only legal', no extra markup or CSS

## Components
### Privacy Policy Component
The `iubendaPrivacyPolicy` component allows your privacy policy to be displayed on any page.
```
title = "Privacy Policy"
url = "/privacy"

[iubendaPolicy]
==
{% component 'iubendaPrivacyPolicy' %}
```

### Cookie Policy Component
The `iubendaCookiePolicy` component allows your cookie policy to be displayed on any page.
```
title = "Cookie Policy"
url = "/cookies"

[iubendaCookiePolicy]
==
{% component 'iubendaCookiePolicy' %}
```

## Errors
If there is an error when retrieving the policy, generic error messages will displayed in place of a policy. Extra information is logged in the backend.

## Change Log
* 1.1.0 - Renamed plugin & cleaned up code
* 1.0.4 - Added support for cookie policy
* 1.0.3 - Localization improvements
* 1.0.2 - Refactored code
* 1.0.1 - First version

## TODO
* Add support for additional Iubenda services.