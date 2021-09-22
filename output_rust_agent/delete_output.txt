## REGISTRAR STDOUT

[root@localhost ~]# keylime_registrar
Using config file /etc/keylime.conf
2021-09-22 16:51:13.993 - keylime.keylime_db - INFO - database_url is not set, using multi-parameter database configuration options
2021-09-22 16:51:14.184 - keylime.keylime_db - INFO - database_url is not set, using multi-parameter database configuration options
2021-09-22 16:51:14.186 - alembic.env - INFO - Migrating database registrar
2021-09-22 16:51:14.187 - alembic.runtime.migration - INFO - Context impl SQLiteImpl.
2021-09-22 16:51:14.187 - alembic.runtime.migration - INFO - Will assume non-transactional DDL.
2021-09-22 16:51:14.193 - keylime.registrar - INFO - Loaded 1 public keys from database
2021-09-22 16:51:14.194 - keylime.cloudverifier_common - INFO - Setting up TLS...
2021-09-22 16:51:14.195 - keylime.registrar - INFO - Starting Cloud Registrar Server on ports 8890 and 8891 (TLS) use <Ctrl-C> to stop
2021-09-22 16:51:14.195 - keylime.registrar - INFO - Current API version 1.0
2021-09-22 16:51:50.811 - keylime.tpm - INFO - TPM2-TOOLS Version: 4.3.2
2021-09-22 16:51:50.812 - keylime.registrar - WARNING - Overriding ek_tpm for agent d432fbb3-d2f1-4a97-9ef7-75bd81c00000 from ekcert
2021-09-22 16:51:50.867 - keylime.tpm - INFO - Encrypting AIK for UUID d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:51:50.871 - keylime.registrar - INFO - Overwriting previous registration for this UUID.
2021-09-22 16:51:50.911 - keylime.registrar - INFO - POST returning key blob for agent_id: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:51:51.086 - keylime.registrar - INFO - PUT activated: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:51:55.575 - keylime.registrar - INFO - GET returning 200 response for agent_id: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:52:07.799 - keylime.registrar - INFO - GET returning 200 response for agent_id: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:52:11.471 - keylime.registrar - INFO - GET returning 200 response for agent_id: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:52:11.673 - keylime.registrar - INFO - GET returning 200 response for agent_id: d432fbb3-d2f1-4a97-9ef7-75bd81c00000


## VERIFIER STDOUT

[root@localhost ~]# keylime_verifier
Using config file /etc/keylime.conf
2021-09-22 16:51:25.555 - keylime.keylime_db - INFO - database_url is not set, using multi-parameter database configuration options
2021-09-22 16:51:25.605 - keylime.keylime_db - INFO - database_url is not set, using multi-parameter database configuration options
2021-09-22 16:51:25.607 - alembic.env - INFO - Migrating database cloud_verifier
2021-09-22 16:51:25.607 - alembic.runtime.migration - INFO - Context impl SQLiteImpl.
2021-09-22 16:51:25.607 - alembic.runtime.migration - INFO - Will assume non-transactional DDL.
2021-09-22 16:51:25.620 - keylime.cloudverifier - INFO - Starting Cloud Verifier (tornado) on port 8881, use <Ctrl-C> to stop
2021-09-22 16:51:25.620 - keylime.cloudverifier - INFO - Current API version 1.0
2021-09-22 16:51:25.621 - keylime.cloudverifier_common - INFO - Setting up TLS...
2021-09-22 16:51:25.621 - keylime.cloudverifier_common - INFO - Existing CA certificate found in /var/lib/keylime/cv_ca, not generating a new one
2021-09-22 16:51:25.622 - keylime.cloudverifier - INFO - Starting service for revocation notifications on port 8992
2021-09-22 16:52:11.364 - keylime.cloudverifier - INFO - POST returning 200 response for adding agent id: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:52:11.639 - keylime.registrar_client - WARNING - TLS is enabled.
2021-09-22 16:52:11.639 - keylime.registrar_client - INFO - Setting up client TLS...
/usr/lib/python3.9/site-packages/urllib3/connectionpool.py:997: InsecureRequestWarning: Unverified HTTPS request is being made to host '127.0.0.1'. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/latest/advanced-usage.html#ssl-warnings
  warnings.warn(
2021-09-22 16:52:11.743 - keylime.tpm - INFO - TPM2-TOOLS Version: 4.3.2
2021-09-22 16:52:11.753 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:52:16.630 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:52:20.361 - keylime.cloudverifier_common - WARNING - Non-fatal problem ocurred while attempting to evaluate agent attribute "mb_refstate" (('malformed node or string: <ast.Name object at 0x7ff48c9f8ee0>',)). Will just consider the value of this attribute to be "None"
2021-09-22 16:52:20.665 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:52:24.633 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:52:28.606 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:52:32.602 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:52:37.618 - keylime.cloudverifier_common - WARNING - Non-fatal problem ocurred while attempting to evaluate agent attribute "mb_refstate" (('malformed node or string: <ast.Name object at 0x7ff48ed9eaf0>',)). Will just consider the value of this attribute to be "None"
2021-09-22 16:52:37.690 - keylime.cloudverifier - INFO - agent state not valid for deletion: 3
2021-09-22 16:52:37.753 - keylime.cloudverifier - INFO - DELETE returning 202 response for agent id: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:52:39.292 - keylime.cloudverifier_common - WARNING - Non-fatal problem ocurred while attempting to evaluate agent attribute "mb_refstate" (('malformed node or string: <ast.Name object at 0x7ff478021940>',)). Will just consider the value of this attribute to be "None"
2021-09-22 16:52:39.323 - keylime.tpm - INFO - Checking IMA measurement list on agent: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:52:41.672 - keylime.cloudverifier_common - WARNING - Non-fatal problem ocurred while attempting to evaluate agent attribute "mb_refstate" (('malformed node or string: <ast.Name object at 0x7ff48c9f0fd0>',)). Will just consider the value of this attribute to be "None"


## RUST AGENT STDOUT
...
 INFO  keylime_agent::quotes_handler  > Calling Integrity Quote with nonce: NCYlGKL9AaFNpnZ9Czg3, mask: 0x408400
 TRACE keylime_agent::tpm             > Attested to PCR digest: [191, 140, 150, 120, 178, 156, 71, 85, 48, 100, 210, 171, 225, 237, 34, 6, 72, 85, 246, 212, 94, 196, 230, 19, 216, 106, 199, 71, 219, 202, 32, 157], read PCR digest: [194, 162, 159, 168, 181, 170, 96, 242, 51, 225, 65, 75, 81, 125, 162, 144, 81, 11, 168, 38, 36, 224, 31, 185, 242, 19, 28, 126, 135, 253, 141, 2]
 INFO  keylime_agent::tpm             > PCR data and attestation data mismatched on attempt 0
 TRACE keylime_agent::tpm             > Attested to PCR digest: [191, 140, 150, 120, 178, 156, 71, 85, 48, 100, 210, 171, 225, 237, 34, 6, 72, 85, 246, 212, 94, 196, 230, 19, 216, 106, 199, 71, 219, 202, 32, 157], read PCR digest: [191, 140, 150, 120, 178, 156, 71, 85, 48, 100, 210, 171, 225, 237, 34, 6, 72, 85, 246, 212, 94, 196, 230, 19, 216, 106, 199, 71, 219, 202, 32, 157]
 INFO  keylime_agent::quotes_handler  > GET integrity quote returning 200 response
...


## TENANT STDOUT

### Delete

[root@localhost ~]# keylime_tenant -v 127.0.0.1 -t 127.0.0.1 --uuid d432fbb3-d2f1-4a97-9ef7-75bd81c00000 --allowlist /root/allowlist.txt --include /root/senddir --cert /root/ca --exclude /root/excludes.txt -c delete
Using config file /etc/keylime.conf
2021-09-22 16:52:35.956 - keylime.tpm - INFO - TPM2-TOOLS Version: 4.3.2
2021-09-22 16:52:35.958 - keylime.tenant - INFO - Setting up client TLS in /var/lib/keylime/cv_ca
/usr/lib/python3.9/site-packages/urllib3/connectionpool.py:997: InsecureRequestWarning: Unverified HTTPS request is being made to host '127.0.0.1'. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/latest/advanced-usage.html#ssl-warnings
  warnings.warn(
/usr/lib/python3.9/site-packages/urllib3/connectionpool.py:997: InsecureRequestWarning: Unverified HTTPS request is being made to host '127.0.0.1'. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/latest/advanced-usage.html#ssl-warnings
  warnings.warn(
/usr/lib/python3.9/site-packages/urllib3/connectionpool.py:997: InsecureRequestWarning: Unverified HTTPS request is being made to host '127.0.0.1'. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/latest/advanced-usage.html#ssl-warnings
  warnings.warn(
/usr/lib/python3.9/site-packages/urllib3/connectionpool.py:997: InsecureRequestWarning: Unverified HTTPS request is being made to host '127.0.0.1'. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/latest/advanced-usage.html#ssl-warnings
  warnings.warn(
/usr/lib/python3.9/site-packages/urllib3/connectionpool.py:997: InsecureRequestWarning: Unverified HTTPS request is being made to host '127.0.0.1'. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/latest/advanced-usage.html#ssl-warnings
  warnings.warn(
Traceback (most recent call last):
  File "/usr/lib/python3.9/site-packages/urllib3/connectionpool.py", line 665, in urlopen
    httplib_response = self._make_request(
  File "/usr/lib/python3.9/site-packages/urllib3/connectionpool.py", line 421, in _make_request
    six.raise_from(e, None)
  File "<string>", line 3, in raise_from
  File "/usr/lib/python3.9/site-packages/urllib3/connectionpool.py", line 416, in _make_request
    httplib_response = conn.getresponse()
  File "/usr/lib64/python3.9/http/client.py", line 1349, in getresponse
    response.begin()
  File "/usr/lib64/python3.9/http/client.py", line 316, in begin
    version, status, reason = self._read_status()
  File "/usr/lib64/python3.9/http/client.py", line 285, in _read_status
    raise RemoteDisconnected("Remote end closed connection without"
http.client.RemoteDisconnected: Remote end closed connection without response

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/usr/lib/python3.9/site-packages/requests/adapters.py", line 439, in send
    resp = conn.urlopen(
  File "/usr/lib/python3.9/site-packages/urllib3/connectionpool.py", line 719, in urlopen
    retries = retries.increment(
  File "/usr/lib/python3.9/site-packages/urllib3/util/retry.py", line 400, in increment
    raise six.reraise(type(error), error, _stacktrace)
  File "/usr/lib/python3.9/site-packages/urllib3/packages/six.py", line 702, in reraise
    raise value.with_traceback(tb)
  File "/usr/lib/python3.9/site-packages/urllib3/connectionpool.py", line 665, in urlopen
    httplib_response = self._make_request(
  File "/usr/lib/python3.9/site-packages/urllib3/connectionpool.py", line 421, in _make_request
    six.raise_from(e, None)
  File "<string>", line 3, in raise_from
  File "/usr/lib/python3.9/site-packages/urllib3/connectionpool.py", line 416, in _make_request
    httplib_response = conn.getresponse()
  File "/usr/lib64/python3.9/http/client.py", line 1349, in getresponse
    response.begin()
  File "/usr/lib64/python3.9/http/client.py", line 316, in begin
    version, status, reason = self._read_status()
  File "/usr/lib64/python3.9/http/client.py", line 285, in _read_status
    raise RemoteDisconnected("Remote end closed connection without"
urllib3.exceptions.ProtocolError: ('Connection aborted.', RemoteDisconnected('Remote end closed connection without response'))

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/usr/local/bin/keylime_tenant", line 33, in <module>
    sys.exit(load_entry_point('keylime==0.0.0', 'console_scripts', 'keylime_tenant')())
  File "/usr/local/lib/python3.9/site-packages/keylime/cmd/tenant.py", line 15, in main
    tenant.main()
  File "/usr/local/lib/python3.9/site-packages/keylime/tenant.py", line 1255, in main
    mytenant.do_cvdelete(args.verifier_check)
  File "/usr/local/lib/python3.9/site-packages/keylime/tenant.py", line 727, in do_cvdelete
    response = get_cvdelete.get(
  File "/usr/local/lib/python3.9/site-packages/keylime/requests_client.py", line 29, in get
    return self.session.get(self.base_url + url, **kwargs)
File "/usr/lib/python3.9/site-packages/requests/sessions.py", line 543, in get
    return self.request('GET', url, **kwargs)
  File "/usr/lib/python3.9/site-packages/requests/sessions.py", line 530, in request
    resp = self.send(prep, **send_kwargs)
  File "/usr/lib/python3.9/site-packages/requests/sessions.py", line 643, in send
    r = adapter.send(request, **kwargs)
  File "/usr/lib/python3.9/site-packages/requests/adapters.py", line 498, in send
    raise ConnectionError(err, request=request)
requests.exceptions.ConnectionError: ('Connection aborted.', RemoteDisconnected('Remote end closed connection without response'))


### Status

[root@localhost ~]# keylime_tenant -v 127.0.0.1 -t 127.0.0.1 --uuid d432fbb3-d2f1-4a97-9ef7-75bd81c00000 -c status
Using config file /etc/keylime.conf
2021-09-22 16:56:24.908 - keylime.tpm - INFO - TPM2-TOOLS Version: 4.3.2
2021-09-22 16:56:24.910 - keylime.tenant - INFO - Setting up client TLS in /var/lib/keylime/cv_ca
/usr/lib/python3.9/site-packages/urllib3/connectionpool.py:997: InsecureRequestWarning: Unverified HTTPS request is being made to host '127.0.0.1'. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/latest/advanced-usage.html#ssl-warnings
  warnings.warn(
Traceback (most recent call last):
  File "/usr/lib/python3.9/site-packages/urllib3/connectionpool.py", line 665, in urlopen
    httplib_response = self._make_request(
  File "/usr/lib/python3.9/site-packages/urllib3/connectionpool.py", line 421, in _make_request
    six.raise_from(e, None)
  File "<string>", line 3, in raise_from
  File "/usr/lib/python3.9/site-packages/urllib3/connectionpool.py", line 416, in _make_request
    httplib_response = conn.getresponse()
  File "/usr/lib64/python3.9/http/client.py", line 1349, in getresponse
    response.begin()
  File "/usr/lib64/python3.9/http/client.py", line 316, in begin
    version, status, reason = self._read_status()
  File "/usr/lib64/python3.9/http/client.py", line 285, in _read_status
    raise RemoteDisconnected("Remote end closed connection without"
http.client.RemoteDisconnected: Remote end closed connection without response

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/usr/lib/python3.9/site-packages/requests/adapters.py", line 439, in send
    resp = conn.urlopen(
  File "/usr/lib/python3.9/site-packages/urllib3/connectionpool.py", line 719, in urlopen
    retries = retries.increment(
  File "/usr/lib/python3.9/site-packages/urllib3/util/retry.py", line 400, in increment
    raise six.reraise(type(error), error, _stacktrace)
  File "/usr/lib/python3.9/site-packages/urllib3/packages/six.py", line 702, in reraise
    raise value.with_traceback(tb)
  File "/usr/lib/python3.9/site-packages/urllib3/connectionpool.py", line 665, in urlopen
    httplib_response = self._make_request(
  File "/usr/lib/python3.9/site-packages/urllib3/connectionpool.py", line 421, in _make_request
    six.raise_from(e, None)
  File "<string>", line 3, in raise_from
  File "/usr/lib/python3.9/site-packages/urllib3/connectionpool.py", line 416, in _make_request
    httplib_response = conn.getresponse()
  File "/usr/lib64/python3.9/http/client.py", line 1349, in getresponse
    response.begin()
  File "/usr/lib64/python3.9/http/client.py", line 316, in begin
    version, status, reason = self._read_status()
  File "/usr/lib64/python3.9/http/client.py", line 285, in _read_status
    raise RemoteDisconnected("Remote end closed connection without"
urllib3.exceptions.ProtocolError: ('Connection aborted.', RemoteDisconnected('Remote end closed connection without response'))

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/usr/local/bin/keylime_tenant", line 33, in <module>
    sys.exit(load_entry_point('keylime==0.0.0', 'console_scripts', 'keylime_tenant')())
  File "/usr/local/lib/python3.9/site-packages/keylime/cmd/tenant.py", line 15, in main
    tenant.main()
  File "/usr/local/lib/python3.9/site-packages/keylime/tenant.py", line 1257, in main
    mytenant.do_status()
  File "/usr/local/lib/python3.9/site-packages/keylime/tenant.py", line 646, in do_status
    response = do_cvstatus.get(
  File "/usr/local/lib/python3.9/site-packages/keylime/requests_client.py", line 29, in get
    return self.session.get(self.base_url + url, **kwargs)
  File "/usr/lib/python3.9/site-packages/requests/sessions.py", line 543, in get
    return self.request('GET', url, **kwargs)
  File "/usr/lib/python3.9/site-packages/requests/sessions.py", line 530, in request
    resp = self.send(prep, **send_kwargs)
  File "/usr/lib/python3.9/site-packages/requests/sessions.py", line 643, in send
    r = adapter.send(request, **kwargs)
  File "/usr/lib/python3.9/site-packages/requests/adapters.py", line 498, in send
    raise ConnectionError(err, request=request)
requests.exceptions.ConnectionError: ('Connection aborted.', RemoteDisconnected('Remote end closed connection without response'))

