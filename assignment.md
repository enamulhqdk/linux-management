# Assignment: User and Group Management

## Task 1: Create Users
1. Created `tupu` using:
    ```bash
    sudo adduser tupu
    ```

2. Created `lupu` with home directory and group using:
    ```bash
    sudo useradd -m -d /home/lupu -s /bin/bash -g lupu lupu
    ```

3. Created system user `hupu` with no login access:
    ```bash
    sudo useradd --system --shell /bin/false hupu
    ```

## Task 2: Add Users to the `sudo` Group
1. Added `tupu` to the `sudo` group:
    ```bash
    sudo usermod -aG sudo tupu
    ```

2. Added `lupu` to the `sudo` group:
    ```bash
    sudo usermod -aG sudo lupu
    ```

## Task 3: Create Directory `/opt/projekti`
1. Created directory with restricted access:
    ```bash
    sudo mkdir -p /opt/projekti
    sudo chgrp projekti /opt/projekti
    sudo chmod 2770 /opt/projekti
    ```

## Task 4: Verified Permissions
1. Verified permissions using:
    ```bash
    ls -ld /opt/projekti
    ```

    Output:
    ```
    drwxrws--- 2 root projekti 4096 <date> /opt/projekti
    ```

## Notes:
- Only `tupu` and `lupu` have access to `/opt/projekti`.
