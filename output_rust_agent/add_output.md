## REGISTRAR STDOUT

```
[root@localhost ~]# keylime_registrar
...
2021-09-22 16:32:35.075 - keylime.registrar - INFO - GET returning 200 response for agent_id: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:32:40.082 - keylime.registrar - INFO - GET returning 200 response for agent_id: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:32:40.235 - keylime.registrar - INFO - GET returning 200 response for agent_id: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
...
```

## VERIFIER STDOUT

```
...
2021-09-22 16:34:00.926 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:34:04.902 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:34:08.899 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:34:13.163 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:34:17.105 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:34:21.108 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:34:25.235 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:34:29.340 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:34:33.308 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:34:37.163 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:34:41.228 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:34:45.019 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
...
```

## TENANT STDOUT

### Add

```
[root@localhost ~]# keylime_tenant -v 127.0.0.1 -t 127.0.0.1 --uuid d432fbb3-d2f1-4a97-9ef7-75bd81c00000 --allowlist /root/allowlist.txt --include /root/senddir --cert /root/ca --exclude /root/excludes.txt -c add
Using config file /etc/keylime.conf
2021-09-22 16:32:35.059 - keylime.tpm - INFO - TPM2-TOOLS Version: 4.3.2
2021-09-22 16:32:35.060 - keylime.tenant - INFO - Setting up client TLS in /var/lib/keylime/cv_ca
2021-09-22 16:32:35.061 - keylime.registrar_client - WARNING - TLS is enabled.
2021-09-22 16:32:35.061 - keylime.registrar_client - INFO - Setting up client TLS...
/usr/lib/python3.9/site-packages/urllib3/connectionpool.py:997: InsecureRequestWarning: Unverified HTTPS request is being made to host '127.0.0.1'. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/latest/advanced-usage.html#ssl-warnings
  warnings.warn(
2021-09-22 16:32:35.076 - keylime.tenant - INFO - TPM PCR Mask from policy is 0x408000
2021-09-22 16:32:35.076 - keylime.tenant - INFO - TPM PCR Mask from policy is 0x808000
Please enter the password to decrypt your keystore: 
2021-09-22 16:32:39.097 - keylime.ca-util - INFO - Creating cert package for d432fbb3-d2f1-4a97-9ef7-75bd81c00000 in d432fbb3-d2f1-4a97-9ef7-75bd81c00000-pkg.zip
2021-09-22 16:32:39.142 - keylime.ca-util - INFO - Creating cert package for RevocationNotifier in RevocationNotifier-pkg.zip
/usr/lib/python3.9/site-packages/urllib3/connectionpool.py:997: InsecureRequestWarning: Unverified HTTPS request is being made to host '127.0.0.1'. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/latest/advanced-usage.html#ssl-warnings
  warnings.warn(
/usr/lib/python3.9/site-packages/urllib3/connectionpool.py:997: InsecureRequestWarning: Unverified HTTPS request is being made to host '127.0.0.1'. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/latest/advanced-usage.html#ssl-warnings
  warnings.warn(
2021-09-22 16:32:40.094 - keylime.tenant - WARNING - DANGER: EK cert checking is disabled and no additional checks on EKs have been specified with ek_check_script option. Keylime is not secure!!
2021-09-22 16:32:40.095 - keylime.tenant - INFO - Quote from 127.0.0.1 validated
```

###Status

```
[root@localhost ~]# keylime_tenant -v 127.0.0.1 -t 127.0.0.1 --uuid d432fbb3-d2f1-4a97-9ef7-75bd81c00000 -c status
Using config file /etc/keylime.conf
2021-09-22 16:37:49.274 - keylime.tpm - INFO - TPM2-TOOLS Version: 4.3.2
2021-09-22 16:37:49.276 - keylime.tenant - INFO - Setting up client TLS in /var/lib/keylime/cv_ca
/usr/lib/python3.9/site-packages/urllib3/connectionpool.py:997: InsecureRequestWarning: Unverified HTTPS request is being made to host '127.0.0.1'. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/latest/advanced-usage.html#ssl-warnings
  warnings.warn(
2021-09-22 16:37:50.887 - keylime.tenant - INFO - Agent Status: "Get Quote"
2021-09-22 16:37:50.887 - keylime.tenant - INFO - Agent severity level: "None"
2021-09-22 16:37:50.887 - keylime.tenant - INFO - Agent last event id: "None"
```


## RUST AGENT STDOUT

```
INFO  keylime_agent                  > Listening on http://127.0.0.1:9002
 INFO  keylime_agent::quotes_handler  > GET invoked from "127.0.0.1:48696" with uri /v1.0/quotes/identity?nonce=gReBfSlRSEeYtpPSJ4Th
 INFO  keylime_agent::quotes_handler  > Calling Identity Quote with nonce: gReBfSlRSEeYtpPSJ4Th
 TRACE keylime_agent::tpm             > Attested to PCR digest: [47, 143, 252, 194, 155, 9, 28, 133, 140, 100, 53, 115, 182, 84, 135, 245, 135, 226, 198, 136, 73, 151, 196, 197, 17, 109, 255, 197, 22, 234, 34, 184], read PCR digest: [47, 143, 252, 194, 155, 9, 28, 133, 140, 100, 53, 115, 182, 84, 135, 245, 135, 226, 198, 136, 73, 151, 196, 197, 17, 109, 255, 197, 22, 234, 34, 184]
 INFO  keylime_agent::quotes_handler  > GET identity quote returning 200 response
 INFO  keylime_agent::quotes_handler  > GET invoked from "127.0.0.1:48698" with uri /v1.0/quotes/integrity?nonce=AWICBD3ff04ZJc976tPd&mask=0x408400&vmask=0x808000&partial=0&ima_ml_entry=0
 INFO  keylime_agent::quotes_handler  > Calling Integrity Quote with nonce: AWICBD3ff04ZJc976tPd, mask: 0x408400
 INFO  keylime_agent::keys_handler    > Received ukey
 DEBUG keylime_agent::keys_handler    > Still waiting on u or v key or auth_tag
 TRACE keylime_agent::tpm             > Attested to PCR digest: [1, 249, 68, 76, 214, 30, 15, 202, 181, 117, 195, 51, 162, 44, 188, 253, 88, 54, 125, 166, 157, 14, 203, 151, 249, 71, 50, 175, 118, 1, 44, 244], read PCR digest: [1, 249, 68, 76, 214, 30, 15, 202, 181, 117, 195, 51, 162, 44, 188, 253, 88, 54, 125, 166, 157, 14, 203, 151, 249, 71, 50, 175, 118, 1, 44, 244]
 INFO  keylime_agent::quotes_handler  > GET integrity quote returning 200 response
 INFO  keylime_agent::keys_handler    > Received vkey
 INFO  keylime_agent::keys_handler    > HMAC check passed
 INFO  keylime_agent::keys_handler    > Successfully derived symmetric payload decryption key
 INFO  keylime_agent                  > Successfully decrypted payload
 INFO  keylime_agent::secure_mount    > Using existing secure storage tmpsfs mount /tmp/secure
 INFO  keylime_agent                  > Wrote payload decryption key to "/tmp/secure/unzipped/derived_tci_key"
 INFO  keylime_agent                  > Wrote decrypted payload to "/tmp/secure/unzipped/decrypted_payload"
 INFO  keylime_agent                  > Unzipping payload decrypted_payload to /tmp/secure/unzipped
 INFO  keylime_agent                  > Payload init script indicated: autorun.sh
 INFO  keylime_agent                  > Running script: "/tmp/secure/unzipped/autorun.sh"
 INFO  keylime_agent                  > "/tmp/secure/unzipped/autorun.sh" ran successfully
 INFO  keylime_agent::secure_mount    > Using existing secure storage tmpsfs mount /tmp/secure
 INFO  keylime_agent::revocation      > Connecting to revocation endpoint at tcp://127.0.0.1:8992...
 INFO  keylime_agent::revocation      > Loading the revocation certificate from /tmp/secure/unzipped/RevocationNotifier-cert.crt
 INFO  keylime_agent::revocation      > Waiting for revocation messages on 0mq tcp://127.0.0.1:8992
 INFO  keylime_agent::quotes_handler  > GET invoked from "127.0.0.1:48704" with uri /v1.0/quotes/integrity?nonce=UKkD0iKRSaaZCd992SKt&mask=0x408400&vmask=0x808000&partial=1&ima_ml_entry=1164
 INFO  keylime_agent::quotes_handler  > Calling Integrity Quote with nonce: UKkD0iKRSaaZCd992SKt, mask: 0x408400
 TRACE keylime_agent::tpm             > Attested to PCR digest: [224, 113, 125, 62, 91, 188, 213, 204, 84, 147, 159, 123, 122, 16, 75, 112, 231, 110, 136, 100, 121, 93, 100, 31, 135, 3, 128, 4, 18, 66, 53, 233], read PCR digest: [224, 113, 125, 62, 91, 188, 213, 204, 84, 147, 159, 123, 122, 16, 75, 112, 231, 110, 136, 100, 121, 93, 100, 31, 135, 3, 128, 4, 18, 66, 53, 233]
 INFO  keylime_agent::quotes_handler  > GET integrity quote returning 200 response
 INFO  keylime_agent::quotes_handler  > GET invoked from "127.0.0.1:48706" with uri /v1.0/quotes/integrity?nonce=3Y1Tnf07MIXZ2DgGG4E6&mask=0x408400&vmask=0x808000&partial=1&ima_ml_entry=1164
 INFO  keylime_agent::quotes_handler  > Calling Integrity Quote with nonce: 3Y1Tnf07MIXZ2DgGG4E6, mask: 0x408400
 TRACE keylime_agent::tpm             > Attested to PCR digest: [1, 249, 68, 76, 214, 30, 15, 202, 181, 117, 195, 51, 162, 44, 188, 253, 88, 54, 125, 166, 157, 14, 203, 151, 249, 71, 50, 175, 118, 1, 44, 244], read PCR digest: [1, 249, 68, 76, 214, 30, 15, 202, 181, 117, 195, 51, 162, 44, 188, 253, 88, 54, 125, 166, 157, 14, 203, 151, 249, 71, 50, 175, 118, 1, 44, 244]
 INFO  keylime_agent::quotes_handler  > GET integrity quote returning 200 response
...
```
