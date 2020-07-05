---
title: "Converting Certs from Different Formats"
date: 2020-06-07T00:20:25+08:00
tags: [sslcert, tlscert, cert-conversion]
draft: false
---

* Convert a DER file (.crt .cer .der) to PEM
```
openssl x509 -inform der -in certificate.cer -out certificate.pem
```

* Convert a PEM file to DER
```
openssl x509 -outform der -in certificate.pem -out certificate.der
```

* Convert a PKCS#12 file (.pfx .p12) containing a private key and certificates to PEM
```
openssl pkcs12 -in keyStore.pfx -out keyStore.pem -nodes
```

* You can add -nocerts to only output the private key or add -nokeys to only output the certificates.
```
openssl pkcs12 -export -out certificate.pfx -inkey privateKey.key -in certificate.crt -certfile CACert.crt
```

More details in https://www.sslshopper.com/ssl-converter.html
