# HOW TO COMPLETE ALL 44 CHARACTERS

I've provided 5 complete character examples in `characters-sample.json`.

Here's a compact template for the remaining 39 characters. Just copy this pattern:

## TEMPLATE (Copy & Modify):

```json
{"id":"characterid","name":"CHARACTER NAME","title":"Title","icon":"🎭","color":"#hexcolor","speed":6,"defense":5,"attack":7,"moves":{
"light":{"name":"Attack Name","dmg":9,"cd":0.25,"type":"melee","hitstun":10,"range":70,"color":"#hex"},
"heavy":{"name":"Power Attack","dmg":24,"cd":1.5,"type":"melee","guardBreak":true,"hitstun":22,"range":95,"color":"#hex"},
"sweep":{"name":"Sweep Attack","dmg":16,"cd":1.0,"type":"melee","trip":true,"hitstun":16,"range":80,"color":"#hex"},
"antiair":{"name":"Launcher","dmg":20,"cd":1.2,"type":"melee","launch":true,"hitstun":24,"range":85,"color":"#hex"},
"lunge":{"name":"Dash Attack","dmg":22,"cd":1.4,"type":"dash_attack","hitstun":19,"range":165,"color":"#hex"},
"special1":{"name":"Special 1","dmg":35,"cd":4,"type":"projectile","color":"#hex"},
"special2":{"name":"Special 2","dmg":45,"cd":6,"type":"projectile","color":"#hex"},
"support":{"name":"Support","cd":10,"type":"buff","shield":true,"duration":3,"color":"#hex"},
"ultimate":{"name":"ULTIMATE","dmg":150,"type":"domain","effect":"stun","color":"#hex"}
}}
```

## QUICK CHARACTER LIST TO ADD:

1. **yuta** - Yuta Okkotsu (👑, #ffffff)
2. **maki** - Maki Zenin (👓, #2e8b57)
3. **inumaki** - Toge Inumaki (📢, #9370db)
4. **panda** - Panda (🐼, #333)
5. **todo** - Aoi Todo (👏, #4169e1)
6. **nanami** - Kento Nanami (👔, #f4a460)
7. **mahito** - Mahito (🧵, #708090)
8. **jogo** - Jogo (🌋, #8b0000)
9. **toji** - Toji Fushiguro (⛓️, #111)
10. **geto** - Suguru Geto (🌀, #4b0082)
11. **hakari** - Kinji Hakari (🎰, #ffd700)
12. **kashimo** - Hajime Kashimo (⚡, #00ffff)
13. **higuruma** - Hiromi Higuruma (⚖️, #8b4513)
14. **takaba** - Fumihiko Takaba (🎭, #ff1493)
15. **uro** - Takako Uro (☁️, #87ceeb)
16. **ryu** - Ryu Ishigori (💥, #ff4500)
17. **uraume** - Uraume (❄️, #b0e0e6)
18. **choso** - Choso (🩸, #8b0000)
19. **hanami** - Hanami (🌳, #228b22)
20. **dagon** - Dagon (🌊, #1e90ff)
21. **naoya** - Naoya Zenin (💨, #fff44f)
22. **mei** - Mei Mei (🐦, #708090)
23. **kusakabe** - Atsuya Kusakabe (⚔️, #4a4a4a)
24. **miguel** - Miguel (🪢, #8b4513)
25. **larue** - Larue (💔, #ff0066)
26. **rika** - Rika Orimoto (👻, #800080)
27. **kenjaku** - Kenjaku (🧠, #4a0e4e)
28. **yorozu** - Yorozu (🔧, #ff6347)
29. **angel** - Angel/Hana (👼, #ffffff)
30. **reggie** - Reggie Star (📜, #daa520)
31. **dhruv** - Dhruv Lakdawalla (🦅, #8fbc8f)
32. **kurourushi** - Kurourushi (🪳, #2f4f2f)
33. **hajime** - Hajime (🔪, #c0c0c0)
34. **ichiji** - Kiyotaka Ichiji (🚗, #4169e1)
35. **mimiko** - Mimiko & Nanako (👭, #ff00ff)
36. **mechamaru** - Mechamaru (🤖, #708090)
37. **junpei** - Junpei Yoshino (🌙, #9370db)
38. **noritoshi** - Noritoshi Kamo (🏹, #dc143c)
39. **mai** - Mai Zenin (🔫, #4682b4)

## STEP-BY-STEP:

1. Open `characters-sample.json`
2. Copy one of the 5 complete character entries
3. Modify the values (name, icon, colors, move names)
4. Paste before the final `]`
5. Add a comma after each character (except the last one)
6. Repeat for all 39 remaining characters

## PRO TIP:

**Speed Balance:**
- Fast (7-9): Low damage (7-10), Low defense (4-5)
- Balanced (6-7): Medium (8-10 dmg, 5-6 def)  
- Tank (4-5): High damage (9-12), High defense (7-9)

**Attack Damage Scaling:**
- Light: speed * 1.2
- Heavy: speed * 4
- Sweep: speed * 2.5
- Antiair: speed * 3
- Lunge: speed * 3.5

This makes balancing super easy!

## FINAL FILE STRUCTURE:

```json
[
  {first character},
  {second character},
  ...
  {44th character}
]
```

NO comma after the last character!

Save as `characters.json` when done.
