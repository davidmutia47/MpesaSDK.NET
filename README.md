# MpesaSDK.NET
Mpesa Daraja SDK implementation for .net.

[![Build Status](https://img.shields.io/endpoint.svg?url=https%3A%2F%2Factions-badge.atrox.dev%2Fmutiadavid%2FMpesaSDK.NET%2Fbadge%3Fref%3Dmaster&style=for-the-badge)](https://actions-badge.atrox.dev/mutiadavid/MpesaSDK.NET/goto?ref=master) ![Nuget](https://img.shields.io/nuget/v/MpesaSDK.NET?style=for-the-badge) ![Nuget](https://img.shields.io/nuget/dt/MpesaSDK.NET?style=for-the-badge) 


For More Info check [Safaricom Mpesa Documentation](https://developer.safaricom.co.ke/docs#authentication)

# Download and Install
nugget [install](https://www.nuget.org/packages/MpesaSDK.NET/)

# Usage

### Sending Requests
***

##### STK Push request
```cs

using MpesaSDK.NET;
using MpesaSDK.NET.Dtos.Requests;
...

MpesaClient mpesaclient = new MpesaClient("consumerkey","secret");

var result = await mpesaclient.STKPush(...);

```

##### Stk Push Query request
```cs

var result = await mpesaclient.StkPushQuery(...);

```

##### B2C request
```cs

var result = await mpesaclient.B2C(...);

```

##### B2B request
```cs

var result = await mpesaclient.B2B(...);

```
>To get MPesa Security credetials for both B2B and B2C use method below. 

```cs 
string credential = "pass".MpesaSecurityCredential(); 
```

##### C2B Register Url request
```cs

var result = await mpesaclient.C2BRegisterUrl(...);

```

##### C2B Simulate Transaction request
```cs

var result = await mpesaclient.C2BSimulateTransaction(...);

```

##### Account Balance request
```cs

var result = await mpesaclient.AccountBalance(...);

```

##### Transaction Status request
```cs

var result = await mpesaclient.TransactionStatus(...);

```

##### Reversal request
```cs

var result = await mpesaclient.Reversal(...);

```

### Callback server

***
Check sample callback api [here](https://github.com/davidmutia47/MpesaSDK.NET/blob/master/CallbackServer/Controllers/CallbackController.cs)



Docs to be updated soon.


## LICENSE

Apache LICENSE-2.0 [read more](https://www.apache.org/licenses/LICENSE-2.0)


