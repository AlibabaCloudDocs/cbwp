# Make API requests

EIP Bandwidth Plan and Virtual Private Cloud \(VPC\) share the same endpoint. To call the EIP Bandwidth Plan API, you must send HTTP GET requests to the endpoint of the EIP Bandwidth Plan API. You must add the request parameters that correspond to the API operation being called. After you call the API operation, the system returns a response. The request and response are both encoded in UTF-8.

## Request syntax

EIP Bandwidth Plan API operations use the RPC protocol. You can call EIP Bandwidth Plan API operations by sending HTTP GET requests.

Request syntax:

```
http://Endpoint/?Action=xx&Parameters
```

Where:

-   Endpoint: the endpoint of the EIP Bandwidth Plan API. The endpoint is `vpc.aliyuncs.com`.
-   Action: the operation that you want to perform. For example, to create an EIP bandwidth plan, set the action to CreateCommonBandwidthPackage.
-   Version: the version of the API to be called. The version of EIP Bandwidth Plan API is 2016-04-28.
-   Parameters: the request parameters for the operation. Separate multiple parameters with ampersands \(&\).

    Request parameters include common parameters and operation-specific parameters. Common parameters include information such as the API version number and authentication information. For more information, see [Common parameters](/intl.en-US/API reference/HTTP Requests/Common parameters.md).


The following example demonstrates how to call the CreateCommonBandwidthPackage operation to create an EIP bandwidth plan:

**Note:** The following code has been edited to improve readability.

```
https://vpc.aliyuncs.com/?Action=CreateCommonBandwidthPackage
&Format=xml
&Version=2016-04-28
&Signature=xxxx%xxxx%3D
&SignatureMethod=HMAC-SHA1
&SignatureNonce=15215528852396
&SignatureVersion=1.0
&AccessKeyId=key-test
&Timestamp=2012-06-01T12:00:00Z
…
```

## Authorization

To ensure the security of your account, we recommend that you call API operations as a Resource Access Management \(RAM\) user. Before you can call the EIP Bandwidth Plan API as a RAM user, you must create and attach the required permission policy to the RAM user.

For more information about the resources and API operations that can be authorized to a RAM user, see [RAM user authorization](/intl.en-US/API reference/RAM user authorization.md).

## Request signature

You must sign all API requests to ensure security. Request signatures are used to verify the identities of the API callers. When you call an API operation by sending an HTTP or HTTPS request, the request must include the signature information.

EIP Bandwidth Plan implements symmetric encryption with an AccessKey pair \(AccessKey ID and AccessKey secret\) to verify the identity of the request sender. An AccessKey pair is an identity credential issued to Alibaba Cloud accounts and RAM users. An AccessKey pair is similar to a pair of username and password. The AccessKey ID is used to verify the identities of the API callers. The AccessKey secret is a secret key that is used to encrypt the signature string on a client and verify the signature string on a server. It is used to authenticate users and must be kept confidential.

To call an RPC API operation, you must add the signature to the API request in the following format:

`https://endpoint/?SignatureVersion=1.0&SignatureMethod=HMAC-SHA1&Signature=XXXX%3D&SignatureNonce=3ee8c1b8-83d3-44af-a94f-4e0axxxxxxxx`

Take the CreateCommonBandwidthPackage operation as an example. If your AccessKey ID is `testid`, and your AccessKey secret is `testsecret`, the URL before the request is signed is:

```
http://vpc.aliyuncs.com/?Action=CreateCommonBandwidthPackage
&Timestamp=2016-05-23T12:46:24Z
&Format=XML
&AccessKeyId=testid
&SignatureMethod=HMAC-SHA1
&SignatureNonce=3ee8c1b8-83d3-44af-a94f-4e0axxxxxxxx
&Version=2014-05-26
&SignatureVersion=1.0
```

To calculate the signature, take the following steps:

1.  Create a string-to-sign by using the request parameters.

    ```
    GET&%2F&AccessKeyId%3Dtestid&Action%3DCreateCommonBandwidthPackage&Format%3DXML&SignatureMethod%3DHMAC-SHA1&SignatureNonce%3D3ee8c1b8-83d3-44af-a94f-4e0axxxxxxxx&SignatureVersion%3D1.0&TimeStamp%3D2016-02-23T12%253A46%253A24Z&Version%3D2014-05-15
    ```

2.  Calculate the HMAC value of the string-to-sign.

    Append an ampersand \(&\) to the AccessKey secret as the key to calculate the HMAC value. In this example, the key is `testsecret&`.

    ```
    CT9X0VtwR86fNWS********juE=
    ```

3.  Add the signature to the request URL.

    ```
    http://vpc.aliyuncs.com/?Action=CreateCommonBandwidthPackage
    &Timestamp=2016-05-23T12:46:24Z
    &Format=XML
    &AccessKeyId=testid
    &SignatureMethod=HMAC-SHA1
    &SignatureNonce=3ee8c1b8-83d3-44af-a94f-4e0axxxxxxxx
    &Version=2014-05-26
    &SignatureVersion=1.0
    &Signature=XXXX%3D
    ```


