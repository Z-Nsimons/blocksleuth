# BlockSleuth 

BlockSleuth is a Python-based Linux tool that monitors system authentication logs to detect failed SSH login attempts. It scans `/var/log/auth.log`, identifies potential brute-force attacks based on repeated login failures from the same IP, and logs alerts with timestamps for further investigation. It is scheduled to run daily using `cron`, providing lightweight, automated log analysis to help harden your server’s security posture.

---

## Features

- Parses `/var/log/auth.log` to find failed SSH login attempts
- Extracts IP addresses and tracks how many times each one fails
- Flags brute-force behavior (5+ failed attempts)
- Logs alerts with timestamps to `alerts.log`
- Automatically runs every day using `cron`

