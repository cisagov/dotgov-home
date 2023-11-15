---
redirect_to: /
title: 2-step Verification
layout: docs
permalink: /2018/10/1/doing-the-2-step/
redirect_from:
  - /2step/
subnav:
  - text: 2-step verification
    href: '#what-is-2-step-verification'
  - text: 2-step FAQ
    href: '#faq'
---
###### October 1, 2018

We’ve added a new feature to improve the security of your .gov registrar account: **2-step verification**.

* [What is 2-step verification?](#what-is-2-step-verification)
* [Why is this change happening?](#why-is-this-change-happening)
* [What does this change mean for me?](#what-does-this-change-mean-for-me)
* [How do I set up 2-step verification?](#how-do-i-set-up-2-step-verification)
* [FAQ](#faq)

## What is 2-step verification?
A password is all that protects your account right now, and passwords can be easier to obtain than you might think.

2-step verification adds another step to the login process. After you enter your password, you’ll be asked for a passcode from your mobile device. This raises the stakes for someone who wants to get into your account because now they have to get your password and your phone.

## Why is this change happening?
Though you might only change your .gov domain or account information infrequently, someone with your password could sign in at any time and make changes. This extra layer of security makes it harder for someone to log in as you, which protects the services you make available to the public via a .gov domain.

## How do I set up 2-step verification?

In order to set up 2-step verification, you will need to use an [authentication app](#what-is-an-authentication-app) to generate security codes. *DotGov will only provide customer support for Google Authenticator*, but any application that implements the time-based one-time password (TOTP) standard will also work.

Here's how to set up 2-step verification with Google Authenticator:

1. **Download** the Google Authenticator app ([Android](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2), [iOS](https://itunes.apple.com/us/app/google-authenticator/id388497605)) on your mobile device. (Note that your organization might have rules about whether this app should be installed on your personal or your work device.)
2. On your computer, **[log in](https://domains.dotgov.gov)** to the .gov registrar at https://domains.dotgov.gov.
3. Once logged in, **click on** *Account* in the left navigation, then **select** *Setup 2-step Verification*.
4. Open the Authenticator app on your device and **select** *Begin Setup* (or '+' if you’ve used the app before), **then tap** *Scan Barcode*, and **point your device’s camera** at the the QR code on the screen. You should see an entry for the *.gov Registrar* added in Authenticator.
6. **Type** the six-digit code displayed on your device in the *One time password* field.

Your account now has 2-step verification enabled! From now on, after you log in with your password, you will need to enter the six-digit code from your authentication app.

## FAQ

* [Who does this change affect?](#who-does-this-change-affect)
* [What is an authentication app?](#what-is-an-authentication-app)
* [Is there a cost for an authentication app?](#is-there-a-cost-for-an-authentication-app)
* [I do not have a smartphone. What other options do I have?](#i-do-not-have-a-smartphone-what-other-options-do-i-have)
* [Do authentication apps need an internet connection to function?](#do-authentication-apps-need-an-internet-connection-to-function)
* [I have a new phone. How do I switch devices?](#i-have-a-new-phone-how-do-i-switch-devices)
* [I’ve lost my phone! How do get back into my account?](#ive-lost-my-phone-how-do-get-back-into-my-account)
* [I have a question that isn’t listed. Who should I contact?](#i-have-a-question-that-isnt-listed-who-should-i-contact)

### Who does this change affect?

All user accounts will be required to use 2-step verification. If any of your domain points of contact (POC) are unable to use an [authentication app](#what-is-an-authentication-app), you will need to assign a new point of contact.

### What is an authentication app?

Authentication apps generate security codes for signing in to sites that require a high level of security. You can use these apps to get security codes even if you don’t have an internet connection or mobile service. A mobile phone app is the typical example of an authentication app, but other forms exist, including applications for desktops, browser extensions, and physical hardware.

Any application that *implements the time-based one-time password (TOTP) standard and can use a QR code or accept a manually entered key* will also work. **DotGov will only provide customer support for Google Authenticator mobile applications**.

After installing and configuring the application to work with the registrar, you will be able to receive security codes for your account. Some options for authentication apps include:

* Android options: [Google Authenticator](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&hl=en), [1Password](https://1password.com/), [Authy](https://authy.com/), [LastPass](https://lastpass.com/)
* iOS options: [Google Authenticator](https://itunes.apple.com/us/app/google-authenticator/id388497605), [1Password](https://1password.com/), [Authy](https://authy.com/), [LastPass](https://lastpass.com/)
* macOS apps: [1Password](https://1password.com/), [OTP Manager](https://itunes.apple.com/us/app/otp-manager/id928941247)
* Windows apps: [1Password](https://1password.com/), [OTP Manager](https://www.microsoft.com/en-us/p/otp-manager/9nblggh6hngn?SilentAuth=1)
* Chrome extensions: [Authenticator](https://chrome.google.com/webstore/detail/authenticator/bhghoamapcdpbohphigoooaddinpkbai?hl=en)
* TOTP hardware: [Protectimus Slim mini](https://www.protectimus.com/protectimus-slim-mini), [Token2 miniOTP-1](https://www.token2.com/shop/?c=2)

### Is there a cost for an authentication app?

Google Authenticator is free to download, and is the only application that DotGov will field customer support for. Other apps may have a cost.

### I do not have a smartphone. What other options do I have?

All users are required to use 2-step verification. If you are unable to use a smartphone, you should explore other [authentication app](#what-is-an-authentication-app) options available, but note that we will only field customer support for Google Authenticator.

### Do authentication apps need an internet connection to function?

No. An internet connection is required to *download* an app (like Google Authenticator), but *using* it does not require an active connection.

### I have a new phone. How do I switch devices?

If you have the old phone, log in to your account, click on 'Account', then select 'Update 2-step verification.'

If you're updating 2-step verification to a new device and you have access to the old one, consider deleting the old device's ".gov Registrar" entry so you aren't confused in the future.

### I’ve lost my phone! How do get back into my account?

If you are unable to access your device, you should [contact the .gov Help Desk]({{ site.baseurl }}/help/).

### I have a question that isn’t listed. Who should I contact?

[Contact the .gov Help Desk]({{ site.baseurl }}/help/) for additional support.
