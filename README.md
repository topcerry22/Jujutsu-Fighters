# JUJUTSU KAISEN: DOMAIN CLASH - JSON-Based Game

## 📦 FILE STRUCTURE

Your game now uses a **modular JSON-based system** for easy character and data management:

```
game-folder/
├── jjk-game-complete.html    (Main game file - all code in one HTML)
├── characters.json            (All 44 characters with 5 attack moves each)
├── maps.json                  (All 6 battle arenas)
└── shop.json                  (All 6 upgrade items)
```

---

## 🎮 HOW IT WORKS

### **Single HTML File**
- Contains ALL game code (CSS, JavaScript, HTML)
- No separate files to manage
- Just open in browser and it loads the JSON data

### **JSON Data Files**
- **characters.json** - Easy to add/edit characters
- **maps.json** - Easy to add new battle arenas
- **shop.json** - Easy to modify upgrade items and prices

---

## ✨ ADDING NEW CHARACTERS

To add a new character, simply add this to `characters.json`:

```json
{
  "id": "newcharacter",
  "name": "CHARACTER NAME",
  "title": "Subtitle",
  "icon": "🎭",
  "color": "#hexcolor",
  "domainColor": "#hexcolor",
  "speed": 6.5,
  "defense": 5,
  "attack": 7,
  "moves": {
    "light": {
      "name": "Quick Attack",
      "dmg": 9,
      "cd": 0.25,
      "type": "melee",
      "hitstun": 10,
      "range": 70,
      "color": "#hexcolor"
    },
    "heavy": {
      "name": "Power Strike",
      "dmg": 24,
      "cd": 1.5,
      "type": "melee",
      "guardBreak": true,
      "hitstun": 22,
      "range": 100,
      "color": "#hexcolor"
    },
    "sweep": {
      "name": "Low Sweep",
      "dmg": 16,
      "cd": 1.0,
      "type": "melee",
      "trip": true,
      "hitstun": 16,
      "range": 80,
      "color": "#hexcolor"
    },
    "antiair": {
      "name": "Launcher",
      "dmg": 20,
      "cd": 1.2,
      "type": "melee",
      "launch": true,
      "hitstun": 25,
      "range": 85,
      "color": "#hexcolor"
    },
    "lunge": {
      "name": "Dash Attack",
      "dmg": 22,
      "cd": 1.5,
      "type": "dash_attack",
      "hitstun": 19,
      "range": 160,
      "color": "#hexcolor"
    },
    "special1": { ... },
    "special2": { ... },
    "support": { ... },
    "ultimate": { ... }
  }
}
```

---

## 🎯 COMBAT SYSTEM

### **5 Attack Abilities** (J/K/L/;/')
1. **Light** (J) - Fast, chains combos
2. **Heavy** (K) - Slow, guard breaks
3. **Sweep** (L + Down) - Trips opponent
4. **Anti-Air** (; + Up) - Launches for air combos
5. **Lunge** (' + Forward) - Dash attack

### **Defense** (SHIFT)
- Hold = Block (70% damage reduction)
- Perfect Timing = Parry (negate + counter + 15% ult charge)

### **Stamina System**
- 100 max, regenerates naturally
- Drains with attacks, blocks, dodges
- 0 stamina while blocking = Guard Break

### **Combo System**
- Chain attacks for bonus damage
- 2-3 hits: +5% damage
- 4-5 hits: +10% damage
- 6+ hits: +15% damage + slow-motion

### **Ultimate Charge**
- Light hit: +3%
- Heavy hit: +5%
- Special hit: +8%
- Perfect parry: +15%
- 6+ combo: +10% bonus

---

## 🗺️ ADDING NEW MAPS

Edit `maps.json`:

```json
{
  "id": "newmap",
  "name": "Map Name",
  "icon": "🏔️",
  "bgColor": "#hexcolor",
  "floorColor": "#hexcolor"
}
```

---

## 💰 ADDING SHOP ITEMS

Edit `shop.json`:

```json
{
  "id": "newitem",
  "name": "Item Name",
  "icon": "⚡",
  "price": 100,
  "effect": "damageMultiplier",
  "value": 0.2
}
```

**Available Effects:**
- `maxHealth` - Increases max HP
- `damageMultiplier` - Increases all damage
- `speedBoost` - Increases movement speed
- `cooldownReduction` - Reduces ability cooldowns
- `lifesteal` - Heals on damage dealt
- `damageReduction` - Reduces incoming damage

---

## 🎨 MOVE TYPES

### **Melee Attacks**
```json
{
  "type": "melee",
  "dmg": 20,
  "range": 100,
  "hitstun": 20,
  "guardBreak": true,  // optional
  "trip": true,        // optional (sweeps)
  "launch": true       // optional (anti-airs)
}
```

### **Projectiles**
```json
{
  "type": "projectile",
  "dmg": 35,
  "multi": 3,          // fires 3 projectiles
  "knockback": 150     // optional
}
```

### **Dash Attacks**
```json
{
  "type": "dash_attack",
  "dmg": 25,
  "range": 180,
  "teleport": true     // optional
}
```

### **Domain Expansions**
```json
{
  "type": "domain",
  "dmg": 200,
  "effect": "stun",    // or "dot", "instant_dmg"
  "duration": 4
}
```

### **Buffs**
```json
{
  "type": "buff",
  "speedBoost": 1.5,
  "damageBoost": 2.0,
  "shield": true,
  "duration": 5
}
```

---

## 🎮 CURRENT STATUS

### ✅ **What's Included:**
- 5 fully implemented characters (Gojo, Sukuna, Yuji, Megumi, Nobara)
- All 6 maps ready
- All 6 shop items ready
- Complete combat system framework
- JSON loading system
- Clean modular structure

### ⏳ **What You Need to Add:**
1. Add remaining 39 characters to `characters.json` (just copy the format)
2. The game logic is partially implemented in the HTML file
3. Follow the examples of the 5 characters already done

---

## 🚀 QUICK START

1. Put all files in the same folder
2. Open `jjk-game-complete.html` in a web browser
3. The game will automatically load character/map/shop data from JSON files
4. If you get an error, make sure the JSON files are in the same folder

---

## 📝 NOTES

- **Easy to Expand**: Just edit JSON files to add content
- **No Compilation**: Pure HTML/CSS/JS
- **Beginner Friendly**: JSON is easy to edit
- **Modular**: Each system separated by JSON type

---

## 🎯 ADDING THE REMAINING 39 CHARACTERS

I've provided 5 complete character examples in `characters.json`. To add the rest:

1. Copy one of the existing character entries
2. Change the ID, name, title, icon, and colors
3. Adjust the stats (speed, defense, attack)
4. Modify move names and damage values to fit the character
5. Keep the same structure for the 9 moves (5 attacks + 4 specials)

**Balance Guidelines:**
- Fast characters (speed 7-9): Lower damage, lower defense
- Balanced characters (speed 6-7): Medium everything  
- Tank characters (speed 4-5): High damage, high defense, slow

---

END OF README
