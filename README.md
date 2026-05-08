# PROJECT VAELEN
### Turn-Based RPG Mobile Game using Ionic Angular

---

# 1. GAME OVERVIEW

## Genre
- Turn-Based RPG
- Dark Fantasy
- Dungeon Progression
- Weapon Gacha

---

## Platform
- Android
- Web

---

## Engine / Framework
- Ionic Angular
- Tailwind CSS

---

## Visual Style
- Dark Medieval Fantasy
- Anime UI
- 2D Turn-Based Battle

---

# 2. CORE GAMEPLAY LOOP

```txt
Enter Level
↓
Fight Enemy
↓
Win Battle
↓
Get Coin + EXP
↓
Weapon Gacha
↓
Equip Weapon
↓
Increase Power
↓
Fight Stronger Enemy
```

---

# 3. PLAYER ROLE SYSTEM

## Available Roles

---

## Warrior

### Identity
Balanced frontline fighter.

### Main Stats
- Physical Attack
- HP
- Sustain

### Strength
- Easy to use
- Balanced
- Good survivability

### Weakness
- No extreme specialization

---

## Archer

### Identity
High critical ranged DPS.

### Main Stats
- Physical Attack
- Critical Rate
- Speed

### Strength
- High burst damage
- Fast turn cycle

### Weakness
- Low durability

---

## Mage

### Identity
Magic burst caster.

### Main Stats
- Magic Attack
- Magic Penetration
- Mana

### Strength
- Strong AOE
- Massive skill damage

### Weakness
- Very fragile

---

## Assassin

### Identity
Fast single-target executioner.

### Main Stats
- Physical Penetration
- Critical Rate
- Speed

### Strength
- Burst damage
- Anti tank

### Weakness
- Very low defense

---

## Tank

### Identity
Frontline protector.

### Main Stats
- HP
- Physical Defense
- Magic Defense

### Strength
- Extremely durable
- Protects team

### Weakness
- Low damage

---

## Support

### Identity
Utility and healing specialist.

### Main Stats
- Heal Power
- Hybrid Attack
- Mana

### Strength
- Sustain team
- Buff capability

### Weakness
- Weak solo performance

---

# 4. STAT SYSTEM

## Main Stats

```txt
HP
Mana

Physical Attack
Magic Attack

Physical Defense
Magic Defense

Critical Rate
Critical Damage

Physical Penetration
Magic Penetration

Speed
```

---

# 5. BATTLE SYSTEM

## Battle Flow

```txt
Battle Start
↓
Determine Turn Order
↓
Player Turn
↓
Choose Action
    ├── Attack
    ├── Skill
    ├── Defend
    └── Item
↓
Execute Action
↓
Enemy Turn
↓
Status Effect Check
↓
Repeat
↓
Battle End
```

---

## Damage Formula

### Physical Damage

```math
PhysicalDamage = (PhysicalAttack - PhysicalDefense) × SkillMultiplier
```

---

### Magic Damage

```math
MagicDamage = (MagicAttack - MagicDefense) × SkillMultiplier
```

---

### Critical Damage

```math
CriticalDamage = Damage × (1 + CriticalMultiplier)
```

---

### Penetration Formula

```math
EffectiveDefense = Defense - Penetration
```

---

### Turn Priority Formula

```math
TurnPriority = Speed + Random(1,10)
```

---

# 6. WEAPON GACHA SYSTEM

## Gacha Type
Weapon-only gacha system.

Player obtains:
- Weapon
- Weapon passive
- Weapon rarity

Player does NOT obtain:
- Character
- Role

---

# 7. WEAPON SYSTEM

## Weapon Categories

### Warrior
- Sword
- Greatsword
- Axe

### Archer
- Bow
- Crossbow

### Mage
- Staff
- Tome

### Assassin
- Dagger
- Dual Blade

### Tank
- Shield Hammer
- Lance

### Support
- Wand
- Holy Book

---

# 8. WEAPON RARITY

```txt
Common
Rare
Epic
Legendary
Mythic
```

---

# 9. WEAPON PASSIVE SYSTEM

## Example Passive Effects

- Burn
- Poison
- Lifesteal
- Freeze
- Combo Attack
- Execute
- Shield Break

---

# 10. GACHA RATE

```txt
Common      60%
Rare        25%
Epic        10%
Legendary    4%
Mythic       1%
```

---

# 11. PITY SYSTEM

```txt
30 Pulls  = Guaranteed Epic
100 Pulls = Guaranteed Legendary
```

---

# 12. PLAYER PROGRESSION

## Progression Sources

- Battle
- EXP
- Weapon upgrade
- Better rarity weapon

---

## Level Reward

Player gains:
- HP increase
- Attack increase
- Mana increase
- New skill unlock

---

# 13. LEVEL SYSTEM

## Structure

```txt
World 1
├── Level 1
├── Level 2
├── Level 3
└── Boss
```

```txt
World 2
├── Harder enemies
├── Better rewards
└── New weapon pool
```

---

# 14. REWARD SYSTEM

## Coin Formula

```math
CoinReward = EnemyLevel × 15 + Random(5,20)
```

---

## EXP Formula

```math
EXP = EnemyLevel × 25
```

---

# 15. INVENTORY SYSTEM

## Inventory Categories

```txt
Weapons
Consumables
Relics
Quest Items
```

---

# 16. RELIC SYSTEM

## Relic Function
Passive item that modifies gameplay.

## Example Effects

- Lifesteal
- Bonus crit damage
- Burn extension
- Counter attack
- Mana regeneration

---

# 17. TECH STACK

## Frontend
- Ionic Angular
- Tailwind CSS

---

## State Management
- Angular Services
- RxJS

---

## Storage
- Ionic Storage
- Local JSON
- SQLite (future)

---

## Animation
- Anime.js

---

## Audio
- Howler.js

---

# 18. PROJECT STRUCTURE

```txt
/src/app
├── core
├── models
├── services
├── systems
├── pages
├── components
└── shared
```

---

# 19. SYSTEM STRUCTURE

```txt
systems/
├── battle-system
├── gacha-system
├── inventory-system
├── skill-system
├── enemy-ai-system
├── save-system
└── reward-system
```

---

# 20. DATA STRUCTURE

## assets/data

```txt
/assets/data
├── enemies.json
├── weapons.json
├── skills.json
├── relics.json
├── gacha.json
└── levels.json
```

---

# 21. SAMPLE WEAPON DATA

```ts
export interface Weapon {
  id: string;

  name: string;
  role: string;

  rarity: string;
  type: string;

  attack: number;
  magicAttack: number;

  critRate: number;

  physicalPen: number;
  magicPen: number;

  passive?: string;
}
```

---

# 22. MVP TARGET

## Initial Scope

### Features
- 6 Roles
- 1 World
- 5 Enemy Types
- 1 Boss
- Weapon Gacha
- Battle System
- Inventory
- EXP System
- Save System

---

## Weapon Count
- 10–15 Weapons

---

## Passive Count
- 5 Passive Effects

---

# 23. FUTURE FEATURES

## Planned Features

- Class Advancement
- Element System
- Multiplayer Raid
- Guild System
- Daily Dungeon
- Weapon Upgrade
- Skin System
- Story Mode
- Boss Raid

---

# 24. PROJECT GOAL

Create a scalable mobile turn-based RPG using Ionic Angular with:
- Class-based combat
- Weapon gacha progression
- Strategic turn-based gameplay
- Long-term scalable architecture

---

# 25. DEVELOPMENT PHASE

## Phase 1
Core Battle Prototype

## Phase 2
Role + Weapon System

## Phase 3
Gacha + Inventory

## Phase 4
Level Progression

## Phase 5
UI Polish + Animation

## Phase 6
Content Expansion

---

# END OF BLUEPRINT
