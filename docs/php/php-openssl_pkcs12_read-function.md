# PHP openssl_pkcs12_read()函数

> Original: [https://www.geeksforgeeks.org/php-openssl_pkcs12_read-function/](https://www.geeksforgeeks.org/php-openssl_pkcs12_read-function/)

**openssl_pkcs12_read()**函数是 PHP 中的内置函数，PKCS#12 证书存储库使用该函数将其转换为 pkcs12 提供的数组。 PKCS#12 文件可以被加密和签名。

**语法：**

```
*bool* openssl_pkcs12_read( *string* $pkcs12, *array* &$certs, *string* $pass )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$pkcs12：**PKCS#12 是 RSA 实验室发布的名为公钥密码标准(PKCS)的标准家族之一。
*   **$certs：**如果成功，这将包含证书存储信息。
*   **$pass：**此参数用于解锁 PKCS#12 文件的加密密码。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

**示例：**

## PHP

```
<?php

$dn = array(
    "countryName" => 'xx',
    "stateOrProvinceName" => 'uttar prradesh',
    "localityName" => 'varanasi',
    "organizationName" => 'geeksforgeeks',
    "organizationalUnitName" => 'geeks team',
    "commonName" => 'people',
    "emailAddress" => 'user@geeks.com'
);

$privateKeyPass = 'dummyPassword';
$numberOfDays   = 108;

$privateKey = openssl_pkey_new();
$csr = openssl_csr_new($dn, $privateKey);

// Create a csr file, change null to
// a filename to save 
$sscert = openssl_csr_sign($csr, 
    null, $privateKey, $numberOfDays);

// On success $publicKey will hold
// the PEM content 
openssl_x509_export($sscert, $publicKey);

// Export the privateKey as a PEM content
openssl_pkey_export($privateKey, 
        $privateKey, $privateKeyPass);

// Parses the $privateKey and used by
// openssl_pkcs12_export_to_file.
$key = openssl_pkey_get_private(
        $privateKey, $privateKeyPass);

$certificateOutput = null;

// Save the pfx file to $certificateOutput
openssl_pkcs12_export($sscert, 
    $certificateOutput, $key, $privateKeyPass);

// openssl_pkcs12_read reads the pkcs12
// certificate and store into array
openssl_pkcs12_read ($certificateOutput, 
        $readableOutput, $privateKeyPass );

var_dump($readableOutput);

?>
```

发帖主题：Re：Колибри0.7.0

```
array(2) {
 ["cert"]=>
  string(1444) "-----BEGIN CERTIFICATE-----
MIID/DCCAuSgAwIBAgIBADANBgkqhkiG9w0BAQUFADCBljELMAkGA1UEBhMCeHgx
FzAVBgNVBAgMDnV0dGFyIHBycmFkZXNoMREwDwYDVQQHDAh2YXJhbmFzaTEWMBQG
A1UECgwNZ2Vla3Nmb3JnZWVrczETMBEGA1UECwwKZ2Vla3MgdGVhbTEPMA0GA1UE
AwwGcGVvcGxlMR0wGwYJKoZIhvcNAQkBFg51c2VyQGdlZWtzLmNvbTAeFw0yMDA5
MDExNjI3MDBaFw0yMDEyMTgxNjI3MDBaMIGWMQswCQYDVQQGEwJ4eDEXMBUGA1UE
CAwOdXR0YXIgcHJyYWRlc2gxETAPBgNVBAcMCHZhcmFuYXNpMRYwFAYDVQQKDA1n
ZWVrc2ZvcmdlZWtzMRMwEQYDVQQLDApnZWVrcyB0ZWFtMQ8wDQYDVQQDDAZwZW9w
bGUxHTAbBgkqhkiG9w0BCQEWDnVzZXJAZ2Vla3MuY29tMIIBIjANBgkqhkiG9w0B
AQEFAAOCAQ8AMIIBCgKCAQEAxDzM5/lUYUir/5Q42Dh1XJk+V9jZm+CQ2QTD9LHY
+AntTX7jxPMdndXm/igd0IEgV0jVEOh+Y/ErlJEJJjMBFCMzbkL+goP15yqwxDEb
OoMEdCJ9StJywc4x/SbgIZLK6cHjqsUgzNIcUdjYjZ/BqN+C/9sXO0v3ArBsmOB3
AgycPxda0PoPcFy2oNMyM7FnJXnPvglJfozdBricggi0hUkMYih2fPWEpNS2dEgf
DmwpiXYu3S4gV0p0l08Q9VFdls8M2X9Nxp4dWV0lfWC8HkmmPOZofMipTsQ0Qvix
/TuA/xxg9ozRdOLv5JOwD8GJctFGKXkXstGPC4Z5+kwBMwIDAQABo1MwUTAdBgNV
HQ4EFgQUVEplgv0Z9eK8NE1YkVBJ0WuNFZwwHwYDVR0jBBgwFoAUVEplgv0Z9eK8
NE1YkVBJ0WuNFZwwDwYDVR0TAQH/BAUwAwEB/zANBgkqhkiG9w0BAQUFAAOCAQEA
EcAu+9VKra4U32LLwHcX+80+LFwwwpzdehFEscfiBxr9zwCbszj1R75gL8AsGhjo
8OKE26+uTABjkElV7NJu9hgeDHxy9/an3xlz+MsEcoaFv9N9qCgqjX/Ihbwv7AHw
N8VxtVrhjyY6ScwyvOaR9Zo8tHNY04tGxqAfRLX5X2TN2EvzpijoLZMOIgsHqQFB
MocshV2BEJ/teom+CactKvrSHcQPwhRpE2dnEqsWK9vai4k1byHpTIAQdb3B+Ytz
MIOMd2wWuWr5EXwoUIaf8pzKAIEQjxNF+yUIMNkXNhaN3NxGIDrWh9057zjYHR2I
yxFL/nK5hEIEWiCyUtd1nQ==
-----END CERTIFICATE-----
"
  ["pkey"]=>
  string(1704) "-----BEGIN PRIVATE KEY-----
MIIEvQIBADANBgkqhkiG9w0BAQEFAASCBKcwggSjAgEAAoIBAQDEPMzn+VRhSKv/
lDjYOHVcmT5X2Nmb4JDZBMP0sdj4Ce1NfuPE8x2d1eb+KB3QgSBXSNUQ6H5j8SuU
kQkmMwEUIzNuQv6Cg/XnKrDEMRs6gwR0In1K0nLBzjH9JuAhksrpweOqxSDM0hxR
2NiNn8Go34L/2xc7S/cCsGyY4HcCDJw/F1rQ+g9wXLag0zIzsWclec++CUl+jN0G
uJyCCLSFSQxiKHZ89YSk1LZ0SB8ObCmJdi7dLiBXSnSXTxD1UV2WzwzZf03Gnh1Z
XSV9YLweSaY85mh8yKlOxDRC+LH9O4D/HGD2jNF04u/kk7APwYly0UYpeRey0Y8L
hnn6TAEzAgMBAAECggEAFLJU6iJhw+DmQw5e8G8D8cA30wwL52TH4huejzAysfZa
ENJRM3RwqzTkJ+oTOupjftEvp5jdu6yz6/df/6dhdb5ArmBid2Fzje3ytr53ILSw
w47fqASKFeapXwm6mc/hlsXcPSaNTwzZ78fvDwDKbAUmy9VPnfFlG+N/kKAb7Rs3
8BUVmeAAhQ0ggRFDjzyK/sNIzK1iJO9xqpWemiWMqiYIvOzPxGymx0O4M9y8k5wo
lAgezRcoYUB4zQsWqkj5X/5NEZsEjy4/jYy/KpCz7LaIPIoZpTqIA0HOetspafuI
P+l4N1vU14wMXeQ0oZCKiysAIExmtMfHmyF7uzbIAQKBgQDzHtOkD8aDcSNOg4Qp
Q/SupcSSQZ93k4xVc3OjRPbBc8OIG+T7gwOS+Y6PpUAbYV7QKtVRNZ0W75qiafRk
akA1Y2CuG24lCE3u7qyUSx/zE9ehUg0MDXcNkauSYfD+1BbIlyQSRaZhGYiKJ5f3
jJuTqS3W4zkPvxLKc2cSGJb1RQKBgQDOoicPFut1SpIW/wVhzoxXfM8IvyW3KlnE
PaqPLFLh5PomiQVhcvd0fKm6FV3sjVI7I++TYzKcpix8V+B2axSTuHrsYCNNGz8L
BE7pOMbEZVE+SPwYT8G15QdiAKxITbNz1YkxB9yBarpAoRw4THAtpnhZhclAzBj5
0dwwTN+YFwKBgQCWXDZgfTE1Eb/YSxZtvw2RBgywt808UxCzuJeIHprNwh7oCvhv
ZPPM7nLw/C7NwEa3UAZmF1Z0XPOyBv2TLPNREYk1pNlWJfCtGQe7H0s/NsJhjzFq
htlelv0Zp2E4+Uqt/GvesRzZaMU9TId8HoYJqNQk1prv1ih09TKFypdyUQKBgHbT
CnED9hz55+6vcjHfbBb3X7sg6JhfE0XlTEqO646ZdTxpuR1j1mc3NQccOGnKjsoR
jTiNZ9JrQNO0WRDf3PJhuNZrJoG1tFgqfxJgovTXapPNtqJoYvWtocQ6rNfbTuHC
nuUCJ0yIylhWDXtWgX/O5hBc/fF0LLykcOGZo067AoGACL/iSs8wNse15sEJ1OdT
SNgL4AnwzyP/wnyIEN57GVhJV9XJCuhlUDhQhn1dRVKmsi3pWMlPldZYgdiZGH6y
9p12cXSJywVIdwszld3OpXhFS+TwMTbAm49qHtvP2TovsPJpEHLXDBEZBo7k1oHU
Uu3UyCB/z8dWkOINHWoi5/0=
-----END PRIVATE KEY-----
"
}

```