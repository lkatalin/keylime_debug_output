#### Tenant

keylime\_tenant -v 127.0.0.1 -t 127.0.0.1 --uuid d432fbb3-d2f1-4a97-9ef7-75bd81c00000 --allowlist /root/allowlist.txt --include /root/senddir --cert /root/ca --exclude /root/excludes.txt -c add

keylime\_tenant -v 127.0.0.1 -t 127.0.0.1 --uuid d432fbb3-d2f1-4a97-9ef7-75bd81c00000 -c delete

keylime\_tenant -v 127.0.0.1 -t 127.0.0.1 --uuid d432fbb3-d2f1-4a97-9ef7-75bd81c00000 -c status

#### Delete database

rm -f /var/lib/keylime/\*.sqlite

### Set up swtpm

### Agent

sudo RUST\_LOG=keylime\_agent=trace ./target/debug/keylime\_agent

