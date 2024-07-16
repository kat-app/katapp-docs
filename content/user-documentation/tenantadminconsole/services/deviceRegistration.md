+++
title = 'Register devices'
weight = 2
+++

The Device registration is used in order to register aider devices that run the KatApp app to the Tenant. The registration of those devices is needed for allowing them to make valid request to the backend services by using authentication tokens. For more information about the authentication tokens, see [Generate authentication token](/authenticationToken).

For the device registration following values are needed:
| Value      | Description |
| ----------- | ----------- |
| **Identification number of the device (IMEI)** | The International Mobile Equipment Identity (IMEI) is used to uniquely identify the device, both for the Tenant Admin Console user and for storage purpose. The IMEI is a 15-digit serial number. The serial number can be requested by entering *#06# in the telephone number input field. On many mobile phones, the IMEI can also be found on the type plate, the packaging or on the SIM tray (holder for the SIM that slides in at the side). For iPhones and iPads, you can also find their IMEI under Settings > General > About. |
| **Name of the device**   | The name of the device is an individual name for device that can be freely filled in. There is no naming convention. Nevertheless, a suitable name should be selected so that the device can be found in the device list. |
| **Operating system** | The KatApp app is available on Android or iOS |
| **Role of the device** | The assigned role gives the device certain access rights to resources. You can find more information about roles and the associated rights [here](/assignRoles). |
| **First and Last name (optional)** | The user of the device can be stored so that the name of the device user is displayed in the dashboard when a triage is created. | 