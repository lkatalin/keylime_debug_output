This is in a Fedora33 VM while running swtpm and the keylime IAM emulator.

It is running the Python components from commit `ff24fe53c9f63c56f68e752d59d7374b36550d12` from Sept. 10,
with two lines added for debug output when delection occurs in `cloud_verifier_tornado.py`.

All components are starting up fresh and the \*.sqlite databases from `var/lib/keylime` have been deleted.
