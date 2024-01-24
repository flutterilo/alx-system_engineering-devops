# 0x12. Web stack debugging #2

## Requirements

- All Bash scripts are created and compiled on Ubuntu 14.04.4 LTS
- All Bash scripts are linted with Shellcheck

## Tasks

<details>
<summary>View Contents</summary>

### [0. Run software as another user](./0-iamsomeonelese)

- The user root is, on Linux, the “superuser”. It can do anything it wants, that’s a good and bad thing. A good practice is that one should never be logged in the root user, as if you fat finger a command and for example run rm -rf /, there is no comeback. That’s why it is preferable to run as a privileged user, meaning that the user also has the ability to perform tasks that the root user can do, just need to use a specific command that you need to discover.

- For the containers that you are given in this project as well as the checker, everything is run under the root user, which has the ability to run anything as another user.
  - write a Bash script that accepts one argument
  - the script should run the whoami command under the user passed as an argument
  - make sure to try your script by passing different users

```
root@ubuntu:~# whoami
root
root@ubuntu:~# ./0-iamsomeonelese nginx
nginx
root@ubuntu:~# whoami
root
```
