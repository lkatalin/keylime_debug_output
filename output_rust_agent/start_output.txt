## REGISTAR STDOUT

[root@localhost ~]# keylime_registrar
Using config file /etc/keylime.conf
2021-09-22 11:23:57.868 - keylime.keylime_db - INFO - database_url is not set, using multi-parameter database configuration options
2021-09-22 11:23:57.945 - keylime.keylime_db - INFO - database_url is not set, using multi-parameter database configuration options
2021-09-22 11:23:57.947 - alembic.env - INFO - Migrating database registrar
2021-09-22 11:23:57.947 - alembic.runtime.migration - INFO - Context impl SQLiteImpl.
2021-09-22 11:23:57.947 - alembic.runtime.migration - INFO - Will assume non-transactional DDL.
2021-09-22 11:23:57.966 - alembic.runtime.migration - INFO - Running upgrade  -> 8a44a4364f5a, Initial database migration
2021-09-22 11:23:57.988 - alembic.runtime.migration - INFO - Running upgrade 8a44a4364f5a -> eeb702f77d7d, allowlist rename
2021-09-22 11:23:57.989 - alembic.runtime.migration - INFO - Running upgrade eeb702f77d7d -> 8da20383f6e1, extend_ip_field
2021-09-22 11:23:57.989 - alembic.runtime.migration - INFO - Running upgrade 8da20383f6e1 -> a7a64155ab3a, Add ima_sign_verification_keys column
2021-09-22 11:23:57.989 - alembic.runtime.migration - INFO - Running upgrade a7a64155ab3a -> cc2630851a1f, receive the aik_tpm from the agent
2021-09-22 11:23:57.995 - alembic.runtime.migration - INFO - Running upgrade cc2630851a1f -> ae898986c6e9, add_mb_refstate_column
2021-09-22 11:23:57.995 - alembic.runtime.migration - INFO - Running upgrade ae898986c6e9 -> eb869a77abd1, create_allowlist_table
2021-09-22 11:23:57.996 - alembic.runtime.migration - INFO - Running upgrade eb869a77abd1 -> b4d024197413, add_verfier_id_to_verifiermain_table
2021-09-22 11:23:57.996 - alembic.runtime.migration - INFO - Running upgrade b4d024197413 -> f82c4252bc4f, Add ip and port to registrar
2021-09-22 11:23:57.997 - alembic.runtime.migration - INFO - Running upgrade f82c4252bc4f -> 7d5db1a6ffb0, Add agentstates columns
2021-09-22 11:23:57.997 - alembic.runtime.migration - INFO - Running upgrade 7d5db1a6ffb0 -> f35cdd35eb83, Move (v)tpm_policy to JSONPickleType
2021-09-22 11:23:57.997 - alembic.runtime.migration - INFO - Running upgrade f35cdd35eb83 -> 257fe0f0c039, Add fields for revocation context to verifier
2021-09-22 11:23:58.031 - keylime.cloudverifier_common - INFO - Setting up TLS...
2021-09-22 11:23:58.033 - keylime.registrar - INFO - Starting Cloud Registrar Server on ports 8890 and 8891 (TLS) use <Ctrl-C> to stop
2021-09-22 11:23:58.033 - keylime.registrar - INFO - Current API version 1.0
2021-09-22 16:29:14.395 - keylime.tpm - INFO - TPM2-TOOLS Version: 4.3.2
2021-09-22 16:29:14.396 - keylime.registrar - WARNING - Overriding ek_tpm for agent d432fbb3-d2f1-4a97-9ef7-75bd81c00000 from ekcert
2021-09-22 16:29:14.512 - keylime.tpm - INFO - Encrypting AIK for UUID d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:29:14.548 - keylime.registrar - INFO - POST returning key blob for agent_id: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:29:14.701 - keylime.registrar - INFO - PUT activated: d432fbb3-d2f1-4a97-9ef7-75bd81c00000
2021-09-22 16:29:28.884 - keylime.registrar - INFO - GET returning 200 response for agent_id: d432fbb3-d2f1-4a97-9ef7-75bd81c00000


## VERIFIER STDOUT

[root@localhost ~]# keylime_verifier
Using config file /etc/keylime.conf
2021-09-22 11:24:05.176 - keylime.keylime_db - INFO - database_url is not set, using multi-parameter database configuration options
2021-09-22 11:24:05.233 - keylime.keylime_db - INFO - database_url is not set, using multi-parameter database configuration options
2021-09-22 11:24:05.234 - alembic.env - INFO - Migrating database cloud_verifier
2021-09-22 11:24:05.235 - alembic.runtime.migration - INFO - Context impl SQLiteImpl.
2021-09-22 11:24:05.235 - alembic.runtime.migration - INFO - Will assume non-transactional DDL.
2021-09-22 11:24:05.254 - alembic.runtime.migration - INFO - Running upgrade  -> 8a44a4364f5a, Initial database migration
2021-09-22 11:24:05.271 - alembic.runtime.migration - INFO - Running upgrade 8a44a4364f5a -> eeb702f77d7d, allowlist rename
2021-09-22 11:24:05.285 - alembic.runtime.migration - INFO - Running upgrade eeb702f77d7d -> 8da20383f6e1, extend_ip_field
2021-09-22 11:24:05.290 - alembic.runtime.migration - INFO - Running upgrade 8da20383f6e1 -> a7a64155ab3a, Add ima_sign_verification_keys column
2021-09-22 11:24:05.292 - alembic.runtime.migration - INFO - Running upgrade a7a64155ab3a -> cc2630851a1f, receive the aik_tpm from the agent
2021-09-22 11:24:05.293 - alembic.runtime.migration - INFO - Running upgrade cc2630851a1f -> ae898986c6e9, add_mb_refstate_column
2021-09-22 11:24:05.294 - alembic.runtime.migration - INFO - Running upgrade ae898986c6e9 -> eb869a77abd1, create_allowlist_table
2021-09-22 11:24:05.314 - alembic.runtime.migration - INFO - Running upgrade eb869a77abd1 -> b4d024197413, add_verfier_id_to_verifiermain_table
2021-09-22 11:24:05.315 - alembic.runtime.migration - INFO - Running upgrade b4d024197413 -> f82c4252bc4f, Add ip and port to registrar
2021-09-22 11:24:05.315 - alembic.runtime.migration - INFO - Running upgrade f82c4252bc4f -> 7d5db1a6ffb0, Add agentstates columns
2021-09-22 11:24:05.317 - alembic.runtime.migration - INFO - Running upgrade 7d5db1a6ffb0 -> f35cdd35eb83, Move (v)tpm_policy to JSONPickleType
2021-09-22 11:24:05.325 - alembic.runtime.migration - INFO - Running upgrade f35cdd35eb83 -> 257fe0f0c039, Add fields for revocation context to verifier
2021-09-22 11:24:05.354 - keylime.cloudverifier - INFO - Starting Cloud Verifier (tornado) on port 8881, use <Ctrl-C> to stop
2021-09-22 11:24:05.354 - keylime.cloudverifier - INFO - Current API version 1.0
2021-09-22 11:24:05.355 - keylime.cloudverifier_common - INFO - Setting up TLS...
2021-09-22 11:24:05.355 - keylime.cloudverifier_common - INFO - Existing CA certificate found in /var/lib/keylime/cv_ca, not generating a new one
2021-09-22 11:24:05.355 - keylime.cloudverifier - INFO - Starting service for revocation notifications on port 8992


## TENANT STDOUT

[root@localhost ~]# keylime_tenant -v 127.0.0.1 -t 127.0.0.1 --uuid d432fbb3-d2f1-4a97-9ef7-75bd81c00000 -c status
Using config file /etc/keylime.conf
2021-09-22 16:29:28.838 - keylime.tpm - INFO - TPM2-TOOLS Version: 4.3.2
2021-09-22 16:29:28.840 - keylime.tenant - INFO - Setting up client TLS in /var/lib/keylime/cv_ca
/usr/lib/python3.9/site-packages/urllib3/connectionpool.py:997: InsecureRequestWarning: Unverified HTTPS request is being made to host '127.0.0.1'. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/latest/advanced-usage.html#ssl-warnings
  warnings.warn(
2021-09-22 16:29:28.869 - keylime.registrar_client - WARNING - TLS is enabled.
2021-09-22 16:29:28.869 - keylime.registrar_client - INFO - Setting up client TLS...
/usr/lib/python3.9/site-packages/urllib3/connectionpool.py:997: InsecureRequestWarning: Unverified HTTPS request is being made to host '127.0.0.1'. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/latest/advanced-usage.html#ssl-warnings
  warnings.warn(
2021-09-22 16:29:28.885 - keylime.tenant - INFO - Agent Status: "Registered"



## RUST AGENT STDOUT

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


