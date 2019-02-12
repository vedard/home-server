# Services

| Service     | domain                        | Ip            |
| ----------- | ----------------------------- | ------------- |
| Pihole      | pihole.triceratops.local      | 192.168.1.99  |
| Steamcache  | steamcache.triceratops.local  | 192.168.1.98  |
| Web         | triceratops.local             | 192.168.1.100 |
| Plex        | plex.triceratops.local        | 192.168.1.101 |
| Portainer   | portainer.triceratops.local   | 192.168.1.102 |
| Netdata     | netdata.triceratops.local     | 192.168.1.103 |
| RiotCache   | riotcache.triceratops.local   | 192.168.1.104 |
| OriginCache | origincache.triceratops.local | 192.168.1.105 |

## DNS topology

```
+------------+      +--------------------+     +------------+     +----------------+
|            |      |                    |     |            |     |                |
|   Router   +------>   Steamcache-dns   +----->   Pihole   +----->   Google DNS   |
|            |      |                    |     |            |     |                |
+------------+      +---------+----------+     +------------+     +----------------+
                              |
                              |
                      +-------v--------+
                      |                |
                      |   Steamcache   |
                      |                |
                      +----------------+

```