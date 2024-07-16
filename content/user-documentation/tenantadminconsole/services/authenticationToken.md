+++
title = 'Generate authentication token'
weight = 4
+++

As you have learnt in the [Device registration](/deviceRegistration) documentation, a tenant admin can register the aider devices on which the KatApp-app is running. There is no association between the device user and device itself. However, the tenant must use the tenant admin console to generate valid authentication keys that are unique for each device. The authentication key is used to obtain an access token from the backend which the KatApp-app usees to make valid requests to the backend.

In order to generate the authentication token, the button Generate Device Token must pressed.
![Generate-device-token-button](/generate-device-token-button.png)

A dialog window will then open (see below), informing you that this device token will not be saved permanently. As soon as you switch to another page in the tenant management console, the generated authentication token will be lost and you will have to generate a new one. 

![generate-device-token-button](/generate-device-token-dialog.png)

Once you finally confirm that you want to generate the token by clicking the Generate device token button again, the authentication token will be generated (see below). Now is the time to memorise the token, enter it directly into the KatApp app (see KatApp app documentation) or copy and save it. CAUTION: If you temporarily save the authentication token elsewhere, please delete it after entering it into the KatApp app.

![device-token](/device-token.png)

By clicking on the Clipboard Icon the device token can be copied to the clipboard for easier usage.

![clipboard-icon](/clipboard-icon.png)
