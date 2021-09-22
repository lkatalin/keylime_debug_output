### Info

This is the output after one delete has failed (see `delete_output.md`), the registrar, verifier, and agent processes have been killed and restarted, and the \*.sqlite databases have NOT been deleted.

### REGISTRAR STDOUT

```
[root@localhost ~]# keylime_registrar
Using config file /etc/keylime.conf
2021-09-22 18:27:15.218 - keylime.keylime_db - INFO - database_url is not set, using multi-parameter database configuration options
2021-09-22 18:27:15.302 - keylime.keylime_db - INFO - database_url is not set, using multi-parameter database configuration options
2021-09-22 18:27:15.304 - alembic.env - INFO - Migrating database registrar
2021-09-22 18:27:15.305 - alembic.runtime.migration - INFO - Context impl SQLiteImpl.
2021-09-22 18:27:15.305 - alembic.runtime.migration - INFO - Will assume non-transactional DDL.
2021-09-22 18:27:15.311 - keylime.registrar - INFO - Loaded 1 public keys from database
2021-09-22 18:27:15.312 - keylime.cloudverifier_common - INFO - Setting up TLS...
2021-09-22 18:27:15.313 - keylime.registrar - INFO - Starting Cloud Registrar Server on ports 8890 and 8891 (TLS) use <Ctrl-C> to stop
2021-09-22 18:27:15.314 - keylime.registrar - INFO - Current API version 1.0
2021-09-22 18:28:26.938 - keylime.tpm - INFO - TPM2-TOOLS Version: 4.3.2
2021-09-22 18:28:26.938 - keylime.registrar - WARNING - Overriding ek_tpm for agent d432fbb3-d2f1-4a97-9ef7-75bd81c00000 from ekcert
2021-09-22 18:28:27.001 - keylime.tpm - INFO - Encrypting AIK for UUID d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 18:28:27.006 - keylime.registrar - INFO - Overwriting previous registration for this UUID.
2021-09-22 18:28:27.042 - keylime.registrar - INFO - POST returning key blob for agent_id: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 18:28:27.198 - keylime.registrar - INFO - PUT activated: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 18:28:36.346 - keylime.registrar - INFO - GET returning 200 response for agent_id: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 18:32:47.258 - keylime.registrar - INFO - GET returning 200 response for agent_id: d432fbb3-d2f1-4a97-9ef7-75bd81c00000

```

### VERIFIER STDOUT

```
[root@localhost ~]# keylime_verifier
Using config file /etc/keylime.conf
2021-09-22 18:27:18.191 - keylime.keylime_db - INFO - database_url is not set, using multi-parameter database configuration options
2021-09-22 18:27:18.281 - keylime.keylime_db - INFO - database_url is not set, using multi-parameter database configuration options
2021-09-22 18:27:18.285 - alembic.env - INFO - Migrating database cloud_verifier
2021-09-22 18:27:18.285 - alembic.runtime.migration - INFO - Context impl SQLiteImpl.
2021-09-22 18:27:18.286 - alembic.runtime.migration - INFO - Will assume non-transactional DDL.
2021-09-22 18:27:18.645 - keylime.cloudverifier - INFO - Agent ids in db loaded from file: [('d432fbb3-d2f1-4a97-9ef7-75bd81c00000',)]
2021-09-22 18:27:18.645 - keylime.cloudverifier - INFO - Starting Cloud Verifier (tornado) on port 8881, use <Ctrl-C> to stop
2021-09-22 18:27:18.645 - keylime.cloudverifier - INFO - Current API version 1.0
2021-09-22 18:27:18.646 - keylime.cloudverifier_common - INFO - Setting up TLS...
2021-09-22 18:27:18.646 - keylime.cloudverifier_common - INFO - Existing CA certificate found in /var/lib/keylime/cv_ca, not generating a new one
2021-09-22 18:27:18.647 - keylime.cloudverifier - INFO - Starting service for revocation notifications on port 8992
2021-09-22 18:28:39.944 - keylime.cloudverifier - WARNING - Agent of uuid d432fbb3-d2f1-4a97-9ef7-75bd81c00000 already exists
2021-09-22 18:28:48.954 - keylime.cloudverifier_common - WARNING - Non-fatal problem ocurred while attempting to evaluate agent attribute "mb_refstate" (('malformed node or string: <ast.Name object at 0x7f4bf090f190>',)). Will just consider the value of this attribute to be "None"
2021-09-22 18:28:49.166 - keylime.cloudverifier - INFO - agent state valid for deletion: 8
2021-09-22 18:28:49.461 - keylime.cloudverifier - INFO - DELETE returning 200 response for agent id: d432fbb3-d2f1-4a97-9ef7-75bd81c00000

```

### RUST AGENT STDOUT

```
[keylime-ima@localhost rust-keylime]$ sudo RUST_LOG=keylime_agent=trace ./target/debug/keylime_agent
 WARN  keylime_agent > INSECURE: Keylime is using a software TPM emulator rather than a real hardware TPM.
 WARN  keylime_agent > INSECURE: The security of Keylime is NOT linked to a hardware root of trust.
 WARN  keylime_agent > INSECURE: Only use Keylime in this mode for testing or debugging purposes.
 INFO  keylime_agent > Starting server with API version v1.0...
 INFO  keylime_agent > Agent UUID: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
 INFO  keylime_agent::registrar_agent > Requesting agent registration from http://127.0.0.1:8890/v1.0/agents/d432fbb3-d2f1-4a97-9ef7-75bd81c00000 for d432fbb3-d2f1-4a97-9ef7-75bd81c00000
 INFO  keylime_agent                  > SUCCESS: Agent d432fbb3-d2f1-4a97-9ef7-75bd81c00000 registered
 INFO  keylime_agent::registrar_agent > Requesting agent activation from http://127.0.0.1:8890/v1.0/agents/d432fbb3-d2f1-4a97-9ef7-75bd81c00000 for d432fbb3-d2f1-4a97-9ef7-75bd81c00000
 INFO  keylime_agent                  > SUCCESS: Agent d432fbb3-d2f1-4a97-9ef7-75bd81c00000 activated
 INFO  keylime_agent                  > Listening on http://127.0.0.1:9002

```

### TENANT STDOUT

#### Delete
```
2021-09-22 18:28:39.944 - keylime.tenant - ERROR - Agent d432fbb3-d2f1-4a97-9ef7-75bd81c00000 already existed at CV. Please use delete or update.

[root@localhost ~]# keylime_tenant -v 127.0.0.1 -t 127.0.0.1 --uuid d432fbb3-d2f1-4a97-9ef7-75bd81c00000 --allowlist /root/allowlist.txt --include /root/senddir --cert /root/ca --exclude /root/excludes.txt -c delete
Using config file /etc/keylime.conf
2021-09-22 18:28:47.083 - keylime.tpm - INFO - TPM2-TOOLS Version: 4.3.2
2021-09-22 18:28:47.085 - keylime.tenant - INFO - Setting up client TLS in /var/lib/keylime/cv_ca
/usr/lib/python3.9/site-packages/urllib3/connectionpool.py:997: InsecureRequestWarning: Unverified HTTPS request is being made to host '127.0.0.1'. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/latest/advanced-usage.html#ssl-warnings
  warnings.warn(
/usr/lib/python3.9/site-packages/urllib3/connectionpool.py:997: InsecureRequestWarning: Unverified HTTPS request is being made to host '127.0.0.1'. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/latest/advanced-usage.html#ssl-warnings
  warnings.warn(
2021-09-22 18:28:49.462 - keylime.tenant - INFO - Agent d432fbb3-d2f1-4a97-9ef7-75bd81c00000 deleted from the CV
```

#### Status
```
[root@localhost ~]# keylime_tenant -v 127.0.0.1 -t 127.0.0.1 --uuid d432fbb3-d2f1-4a97-9ef7-75bd81c00000 -c status
Using config file /etc/keylime.conf
2021-09-22 18:32:47.208 - keylime.tpm - INFO - TPM2-TOOLS Version: 4.3.2
2021-09-22 18:32:47.210 - keylime.tenant - INFO - Setting up client TLS in /var/lib/keylime/cv_ca
/usr/lib/python3.9/site-packages/urllib3/connectionpool.py:997: InsecureRequestWarning: Unverified HTTPS request is being made to host '127.0.0.1'. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/latest/advanced-usage.html#ssl-warnings
  warnings.warn(
2021-09-22 18:32:47.245 - keylime.registrar_client - WARNING - TLS is enabled.
2021-09-22 18:32:47.245 - keylime.registrar_client - INFO - Setting up client TLS...
/usr/lib/python3.9/site-packages/urllib3/connectionpool.py:997: InsecureRequestWarning: Unverified HTTPS request is being made to host '127.0.0.1'. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/latest/advanced-usage.html#ssl-warnings
  warnings.warn(
2021-09-22 18:32:47.259 - keylime.tenant - INFO - Agent Status: "Registered"

```

Note: At this point, it was possible to re-add the agent.
