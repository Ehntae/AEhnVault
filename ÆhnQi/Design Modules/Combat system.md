---
alias: Combat System Design
tags: [gamedesign, combat, cultivation]
created: 2025-01-15
---

# 🗡️ Wuxia Combat System

> [!info] Core Concept
> A cultivation game combat system emphasizing body part specific damage and two distinct cultivation paths: Body and Soul cultivators.

## 🎯 Core Mechanics

### Body Part System
Each character's body is divided into distinct parts:
- Head
- Arms
- Hands
- Feet
- Legs
- Torso
- Hips

> [!note] Body Part Attributes
> - Base Health: 100% (representing condition/integrity)
> - Qi Storage Capacity (upgradeable)
> - Current Qi Amount

### Health System
Unlike traditional HP systems:
- Each body part maintains its own health percentage
- Overall character condition = average of all body part health percentages
- Damage targets specific body parts
- Performance is tied to body part condition

## ⚔️ Cultivation Paths

### 💪 Body Cultivators
![[body_cultivator.png]]

> [!example] Body Cultivator Example
> **Right Hand Stats:**
> - Health: 500/500 (500% maximum)
> - Qi Storage: 650/800
> 
> **Attack (100 Qi cost):**
> 1. Qi consumed: 650 → 550
> 2. Base damage: 100
> 3. Final damage: 100 * 500% = 500

#### Key Features
- Enhance physical body parts beyond 100% health
- Can achieve extremely high health thresholds (e.g., 500%)
- Maintain full combat efficiency until final 100% health
- Store and utilize Qi directly in body parts
- Use keyword "Perform" for actions

### 🌟 Soul Cultivators
![[soul_cultivator.png]]

#### Key Features
- Can enhance body parts to 130-150% health as defensive measure
- Focus on spiritual energy rather than physical enhancement
- Different resource system (to be detailed)
- Use keyword "Cast" for actions
- Miss out on body part multipliers

## 🎲 Combat Mechanics

### Damage & Efficiency System

> [!important] Body Part Health States
> #### Above 100% Health
> - Acts as buffer zone
> - Provides damage multipliers (Body Cultivators only)
> - Maintains 100% efficiency
> 
> #### Below 100% Health
> - Begins efficiency penalties
> - Affects skills using that body part
> - Reduces combat effectiveness

### Combat Calculations
```js
// Base damage formula for Body Cultivators
Damage = Base_Damage * Body_Part_Health_Percentage

// Overall condition calculation
Condition = Average(All_Body_Part_Health_Percentages)
```

## 🔮 Qi System

> [!tip] Qi Management
> - Stored individually in body parts
> - Upgradeable storage capacity
> - Powers skills and techniques
> - Separate pools per body part
> - Primary resource for Body Cultivators

### Skill Usage
When using a skill:
1. Qi is drawn from the relevant body part
2. Damage/effect is modified by body part's health percentage
3. Additional effects may vary based on cultivation path

## 🎮 Implementation Notes

### Performance vs Casting
- Body Cultivators "Perform" skills through enhanced body parts
- Soul Cultivators "Cast" skills through spiritual means
- Different keywords indicate different scaling mechanics

### Balance Considerations
- Body Cultivators excel at sustained combat through enhanced durability
- Soul Cultivators focus on different mechanics (to be detailed)
- System provides natural progression paths for both styles

> [!warning] TODO
> - Detail Soul Cultivator resource system
> - Define spiritual energy mechanics
> - Create skill progression trees
> - Balance body part enhancement rates

---
## Related Notes
- [[Combat Skills]]
- [[Cultivation Paths]]
- [[Game Balance]]
```

Note: Image links are placeholders for your Obsidian vault organization
```