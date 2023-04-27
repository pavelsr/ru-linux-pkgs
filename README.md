# What is it ? 

Dump of available and installed packages in three popular Russian Linux distros - [Astra Linux](https://wikipedia.org/wiki/Astra_Linux), [ALT Linux](https://wikipedia.org/wiki/ALT_Linux) and [RedOS](https://ru.wikipedia.org/wiki/РЕД_ОС)


```
*-installed - packages installed by default in distro
*-available - packages available in repo
```

## Tested distros

ALT Linux 10.0 «Autolycus»

Astra Linux orel-2.12.45.5-23.07.2022_07.53.iso

RedOS MUROM-7.3.2

## How did I get this txt output ?

ALT Linux -> `rpm -qa` (installed only)

Astra Linux -> `dpkg-query -f '${binary:Package}\n' -W` && `apt-cache search .` (after `apt-get update`)

RedOS -> `yum list installed` && `yum list available` (after `yum check-update`)

(first command is list of installed, second - available)

## Total stat

| Distro \ spec  | pkgs available | pkgs installed |
|----------------|----------------|----------------|
| RedOS          | 36989          | 1945           |
| Astra Linux    | 14623          | 1854           |
| ALT Linux      |                | 1918           |

