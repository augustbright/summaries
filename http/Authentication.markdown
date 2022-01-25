# Authentication framework
![](i/c2c5b5dd-e1a8-40ca-83d5-d6e4fc187419.jpg)
# Authentication headers
- Authorization <auth-scheme> <authorisation-parameters>
- Proxy-Authorization <auth-scheme> <authorisation-parameters>
- WWW-Authenticate <auth-scheme>[ ...params]
- Proxy-Authenticate <auth-scheme>[ ...params]


# Authentication schemes
- Basic - base64 (ID/PASSWORD) - https/tls must be used
- Bearer
- Digest
- HOBA
- Mutual
- Negotiate/ NTLM
- VAPID
- SCRAM
- AWS4-HMAC-SHA256