# Ephemerous Phone Self Install

![Phone Software](./media/phone-demo.jpg)
![Phone Software](./media/phone-in-demo.jpg)

Make and receive calls using Cloudflare Workers and Twilio.


## Requirements
* Cloudflare account
* Twilio account

(Cloudflare's free tier or better - Twilio offers a free trial.)

## Steps
1. Setup Cloudflare
	1. Account
	1. Activate workers
	1. Worker key
1. Setup Twilio
	1. Account
	1. Phone number
	1. API key
1. Install and Configure
	1. Install phone software
	1. Connect Twilio


### Cloudflare
Create a [Cloudflare](https://dash.cloudflare.com/sign-up) account (free tier works, you don't need to add a domain.)

#### Activate workers

From the Cloudflare dashboard

![](./media/cloudflare-workers-step.jpg)

Select a subdomain (you can change this later)

![](./media/cloudflare-account-id-step.jpg)

Note your Account ID (we'll need this in the install step)



#### Create a worker token

![](./media/cloudflare-api-profile-step.jpg)
![](./media/cloudflare-api-token-step.jpg)

**Create Token**

![](./media/cloudflare-api-template-step.jpg)

**Permissions**
Use provided defaults.

**Account Resources**
All Accounts

**Zone Resources**
All Zones

**Client IP Address Filtering**
Leave as is

**TTL**
Click `Start Date`, select today.

Click today again to set `End Date`.

Click away from calendar

**Continue to Summary**
Review settings

**Create Token**

![](./media/cloudflare-api-key-step.jpg)

Save this key, we'll use it in the install step.

Next setup Twilio...


### Twilio
Create a [Twilio](https://www.twilio.com/try-twilio) account.

**Note your ACCOUNT SID**

We'll need this in the configuration step.


**Get a phone number**

![](./media/twilio-explore-step.jpg)
![](./media/twilio-phone-number-product-step.jpg)

**Buy a number**
Search for and buy a number.



**Create API key**

![](./media/twilio-api-key-step.jpg)

**Create API key**
Provide a `Friendly Name`

**Keytype:** Standard 

**Create API Key**

Record...
* SID
* Secret

We'll need these for the configure step.

Next, install the phone software to your Cloudflare worker...

### Install
Browse to the [Ephemerous installer](https://get.ephemerous.com/)

![](./media/ephemerous-install-step.jpg)

Select the **Cloudflare** hosting option.


Provide your Cloudflare worker credentials.
* Account ID
* Worker Token


**Next**

Wait as Ephemerous is automatically installed to your Cloudflare account (this can take a minute or two.)

### Configure
You'll be forwarded to your new phone url, make note of the `url` and `activation code`.

Provide your Twilio key information.
* Account SID
* API SID
* API Secret

Select the phone number you'll use for your web phone.

You're all set!

## Bonus Steps

### Activate your phone on another device.

1. From the new device visit your phone url.
1. Enter your activation key.


![](./media/ephemerous-activate-step.jpg)

