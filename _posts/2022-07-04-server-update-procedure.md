---
layout: post
title: "Server Update Procedure"
author: "Scout"
---
## Making a New World
Open the Vanilla instance and stop it. Rename the latest save (likely `scenario.zip`) to the current day, formatted as YYYY-MM-DD (ie 2022-07-04). At this time, any updates to the scenario should be applied by someone with shell access if applicable.

Click the Load Scenario button, and paste in the Map Exchange String. The name of the scenario is "scenario". The server should start. Look for the phrase "pingpong" in console - if it does *not* state `86.82.202.96:34197` (paying special attention to the number after the colon), stop the server, start it again, and recheck. Finally, log into the server yourself from the public server listing (do not use the green last-played button on the title screen), and after confirming the map has loaded correctly, ping `@Server Reset Ping` in the proper channel.

If the Map Exchange String does not work and needs patching, and the console produces an error indicating unset or missing values, load Factorio, and follow the dialogs to create a new Freeplay map. In the Map Settings, import the string. Adjust a slider, such as increasing Iron Ore richness, and then drag the slider back to the initial position. Then, export the fixed exchange string.

## Common Map-Exchange Strings
Joloman2's Regular Rich Uranium
```
>>>eNpjZGBksGUAgwZ7BoYDDhwsyfmJOUCuAwivXrXKnis5v6Agt
Ug3vygVKOIAkTpgz5lcVJqSqpufmQPiwRWn5qXmVuomJRangrgQq
QZ7jsyi/DyICQxwE1iLS/LzUpF1s5YUpaYWQ5wCwdylRYl5maW5U
NtBKiFyjLLFk+YWiDMwgPD/egaF//9BGMh6AFQDwgyMDUCVDgyMQ
DEYYE3OyUxLY2BQcARiJ7AiRsZqkXXuD6um2DNC1Og5QBkPoCIHk
mAinjCGnwNOKaCREMrEgXHWTBB4ac9oDAafkRgQS0uAVkCVczggG
BDJFpAkI2OmbKivQOl7O8Y/Kz9e8k1KsGfsfbt1wfdjG+yAkuwg+
5jgBMTCnTCvMCB5BSJ1057x7BkQeGPPyArSIQIiHCyAxAFvZgZGA
T4ga0EPkFCQgfvEDmaMiANjGhh8g/nkMYxx2R7dHyoOjDYgw+VAx
AkQwYoIHKDLGCFMh34HRgd5mKwkQglQvxEDshtSED48CbP2MJL9a
A5RcUBEBKY/0ERUHLBEAxfIwhQ48YIZ7hpgeF5gh/Ec5jswMoMYI
FVfgGIQHjSpg42C0AIO4OBmBic7iJCCA4Nq2GMfAAWwo3Q=<<<
```

Elefetor's Islands (Needs Patched)
```
>>>eNptUjFLw1AQvrMWawVxKIggmqGTUgd11L7TRdz8B9KmKQTap
KTtoA52cBScddFNaMG9W8WlgoLg5FZxcXBTdKzv5eW9pKEHd+/Ld
/fdu3cEAWEbfOuR8NSk6RYqAC2mPG26tZrl5VzPitLTptcsWTnXH
i22HKt6lCsW6rwYeEciQadsz3XiHZL1huuMMg3PsupS2MoLZqbpF
Ry7WZVaok67zXligP2D1dvaPIDw4SkYw6FwjgZcLxyw1Wmv5AE5p
yxpVuxyGcDY4b4rOZTHGikEIQhQr0gBta+rNjna8O2bheAkc7f3f
txgqMpSFAKZPGOqPU7ocHUprKtTSjVgQeqN4fOTsC/mS+dmebg55
8FY1APnlSxDWPbtV832ocAri0+WJdwSLZdE6IuQjOyAECWkC0JaV
tmFsITr1yE6Qyl80aO69iFyf2yQLOmVjnlHjMnSmMWmxYUlHT4Te
hq+v5cp9UXXhAkBRNUP5+SX/N9kK3nOEWb4IbLB48EgOLzv/v0D9
CiINA==<<<
```

Scout Has No Clue How To Make A String
```
>>>eNpjZGBksGUAgtWrVtkzMBxw4GBJzk/MAQo4gDBIlCs5v6Agt
Ug3vygVJgxUaM+ZXFSakqqbn5kD4sEVp+al5lbqJiUWAxU32MMwR
2ZRfh66CazFJfl5qci6WUuKUlOLkTVylxYl5mWW5kL0HgCq0rIDY
QZGX/3dQQXiDAwg/L+eQeH/fxAGsh4ATQNhBsYGkA4GRqAYDLAm5
2SmpTEwKDgCsRNYESNjtcg694dVU+wZIWr0HKCMB1CRA0kwEU8Yw
88BpxTQSAhl4sA4ayYIvLRnNAaDz0gMiKUlQCugyjkcEAyIZAtIk
pExUzbUV6D0vR3jn5UfL/kmJdgz9r7duuD7sQ12QEl2kH1McAJi4
U6YVxiQvAKRumnPePYMCLyxZ2QF6RABEQ4WQOKANzMDowAfkLWgB
0goyMB9YgczRsSBMQ0MvsF88hjGuGyP7g8VB0YbkOFyIOIEiGBFB
A7QZYwQpkO/A6ODPExWEqEEqN+IAdkNKQgfnoRZexjJfjSHqDggI
gLTH2giKg5YooELZGEKnHjBDHcNMDwvsMN4DvMdGJlBDJCqL0AxC
A+a1MFGQWgBB3BwM4OTHURIwYEhq/D3HwBvr6cj<<<
```

Scout Made a Tiny Map
```
>>>eNpjZGBksGUAgtWrVtkzMBxw4GBJzk/MAQo4gDBIlCs5v6Agt
Ug3vygVJgxUaM+ZXFSakqqbn5kD4sEVp+al5lbqJiUWAxU32EMUN
9hzZBbl56GbwFpckp+XiqybtaQoNbUYohGCuUuLEvMyS3Mheg+AD
LNbvUrLjoFxulqo2Q5uBgYQ/l/PoPD/PwgDWQ+ApoEwA2MDULUDA
yNQDAZYk3My09IYGBQcgdgJrIiRsVpknfvDqin2jBA1eg5QxgOoy
IEkmIgnjOHngFMKaCSEMnFgnDUTBF7aMxqDwWckBsTSEqAVUOUcD
ggGRLIFJMnImCkb6itQ+t6O8c/Kj5d8kxLsGXvfbl3w/dgGO6AkO
8g+JjgBsXAnzCsMSF6BSN20Zzx7BgTe2DOygnSIgAgHCyBxwJuZg
VGAD8ha0AMkFGTgPrGDGSPiwJgGBt9gPnkMY1y2R/eHigOjDchwO
RBxAkSwIgIH6DJGCNOh34HRQR4mK4lQAtRvxIDshhSED0/CrD2MZ
D+aQ1QcEBGB6Q80ERUHLNHABbIwBU68YIa7BhieF9hhPIf5DozMI
AZI1RegGIQHTepgoyC0gAM4uJnByQ4i9MGeYf7dTT8AAVWmvw==<
<<
```

Scout Tweaks Some Ore Settings
```
>>>eNpjZGBkcGEAgtWrVtkzMBxw4GBJzk/MAQoAeQwOQOTAlZxfU
JBapJtflApUZAdSBMKcyUWlKam6+ZlQxRBRrtS81NxK3aTE4lSQX
qAQUKrBniOzKD8P3QTW4pL8vFRk3awlRampxSANMMxdWpSYl1maC
9ILMnD1Ki07EGZg7DWe4LKAn4EBhP/XMyj8/w/CQNYDoIkgzMDYA
DTBgYERKAYDrMk5mWlpDAwKjkDsBFbEyFgtss79YdUUe0aIGj0HK
OMBVORAEkzEE8bwc8ApBTQSQpk4MM6aCQIv7RmNweAzEgNiaQnQC
qhyDgcEAyLZApJkZMyUDfUVKH1vx/hn5cdLvkkJ9oy9b7cu+H7sg
B1Qkh1kHxOcgFi4E+YVBiSvQKRu2jOePQMCb+wZWUE6RECEgwWQe
LAUaJ0AH5C1oAdIKMjAfWIHM0bEgTENDL7BfPIYxrhsj+4PFQdGG
5DhciDiBIhgRQQO0GWMEKZDvwOjgzxMVhKhBKjfiAHZDSkIH56EW
XsYyX40h6g4ICIC0x9oIioOWKKBC2RhCpx4wQx3DTA8L7DDeA7zH
RiZQQyQqi9AMQgPkn8gRkFoAQdwcDODkx1ESMGBIdzv6VsAKeyoN
A==<<<
```

Scout Hates You
```
>>>eNp1U78vA3EUf081qhI6dJEIHTpJSoLBIHePSMRi8g9U7xpNq
se1HTAwGAwSi4VF50psBos0sSAkEgsbIUJiESK2eu++/faa4uXe+
37u8973/fh+7xAQJoHloNxvAlQo1JpyktmDctlgkvihcMpZXLTdh
OPaAOumUOJqT7lFy044mSyzhmbDds5eWE7MJfMcXPEyyqZQxnVyz
RmC+YKTYwZ8puDadl7FKO0ouslcprig9npR0qoBaC1ln0tdAKLVN
YhVq6KM7jlEFHDdK4/MaQmmspl0GiA2zjrhBSGuRg+nHlZ2TFQxA
1QD9zWmMqeZaQ1m6F8Xp1TLCOHersiricOefDQAVbTAJWrhIfKBc
m6IE/F9/nHz6PvTqLGWibNPkaV8/53Bzjap11I3quCxHgUaRlGuO
xOvLkXeTAzKjqgYGmVT2mIT6dQo1lOfxNBpooRpT770JI8a3JjNc
8QJxyR5r5gzMUH/cLgzVJC2CalPe7v9EN4/BI09WP6E57rsaUP9p
kbi5F/E7zmamDj9cQ1hKWjVzUug3g2f53WbfqN9woAAifpkTr2p/
0elUmuEvOMOeJ+domIEt4MnFz8e4KEB<<<
```
## Updating the Server Software
To update the Clusterio Control panel, first, stop all instances of the game from the Clusterio panel. Then, stop the panel via systemd:
```bash
$ sudo systemctl stop factorio
```

If the above command fails, use the backup `docker-compose down`.

The `/opt/Control` folder is a local git repository containing docker and other configuration files. Pull the GitHub repository to update the control panel. In addition, the `/opt/Control/factorio` directory is a headless server install of Factorio, owned by the user `nobody:factorio`. Updating said install will update **all** instances.

In addition, the scenario files are installed in local git repositories in each instance's `scenarios/scenario` folder, and can be pulled from via there. This does not require the main panel to be offline - only the respective instance being updated.

Start the panel again via systemd:
```bash
$ sudo systemctl start factorio
``
