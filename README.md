# About azerothcore systemd units
**azerothcore systemd units** is a pair of systemd units that allows you to manage [azerothcore](https://www.azerothcore.org/) binary files (`authserver` and `worldserver`) from systemd commands (systemctl)

Once installed, you can run most of systemctl commands for services

# Instructions
1. Download both files `acore-auth-server.service` and `acore-world-server.service`

2. Change the path to binaries in both files (at `ExecStart` directive)

3. Move both files to `/etc/systemd/system`

4. Reload systemd by running `sudo systemctl daemon-reload`

# How to use these units

Once installed, they can be managed as any other systemd service

- Start both services
    - `sudo systemctl start acore-auth-server.service`
    - `sudo systemctl start acore-world-server.service`

- Stop both services
    - `sudo systemctl stop acore-auth-server.service`
    - `sudo systemctl stop acore-world-server.service`

- Restart both services
    - `sudo systemctl restart acore-auth-server.service`
    - `sudo systemctl restart acore-world-server.service`

- Set both services to automatically start on boot
    - `sudo systemctl enable acore-auth-server.service`
    - `sudo systemctl enable acore-world-server.service`

- Prevent both services from automatically starting on boot
    - `sudo systemctl disable acore-auth-server.service`
    - `sudo systemctl disable acore-world-server.service`