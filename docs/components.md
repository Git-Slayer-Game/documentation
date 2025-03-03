# Git Slayer - Game Components

Welcome to the core documentation for the **Git Slayer Game** components. This file provides an in-depth look at the game’s structure, including levels, character classes, items, milestones, and integration with GitLab/GitHub activities.

## 1. Levels and Experience Points (XP)

Contributors earn **XP** through GitLab/GitHub activities. XP allows players to level up, unlocking new abilities, items, and milestones. The XP system is designed to create fast progression in early levels while slowing down after level 100.

### XP Awarded Per Activity:

| **Activity**              | **XP (Levels 1-50)** | **XP (Levels 51-100)** | **XP (Levels 101+)** |
|---------------------------|----------------------|----------------------|------------------|
| **Commits**                | 15 XP               | 10 XP               | 8 XP            |
| **Pull Requests Merged**   | 35 XP               | 30 XP               | 25 XP           |
| **Issue Resolution**       | 20 XP               | 15 XP               | 12 XP           |
| **Code Review**            | 30 XP               | 25 XP               | 20 XP           |
| **Documentation Updates**  | 25 XP               | 20 XP               | 15 XP           |

### Milestone Rewards:
- **Levels 10, 25, 50, 75, 100** trigger **Dragon Battles**, where bonus XP and exclusive items can be won.
- **Temporary XP Boost Items** are awarded for winning battles, providing **+10% XP for 24 hours**.
- **Legendary items** become available at Level 100+.

## 2. Character Classes

Each player selects a **Character Class** based on their coding style and preferred contributions. Each class has unique abilities, items, and XP bonuses for certain activities.

### 2.1 Knight (Stability & Robustness)

**Abilities**:
- **Armor of Resilience**: +20% XP for bug fixes and performance improvements.
- **Shield of Fortification**: Reduces cooldown (review or merge wait time) by 10%.

### 2.2 Sorcerer (Innovation & Creativity)

**Abilities**:
- **Staff of Ingenuity**: +15% XP for introducing new features or libraries.
- **Spell of Insight**: Random bonus XP for complex pull requests.

### 2.3 Paladin (Collaboration & Documentation)

**Abilities**:
- **Banner of Teamwork**: +10 XP to code reviews.
- **Book of Knowledge**: Chance for rare items on significant documentation contributions.

### 2.4 Druid (Adaptability & Versatility)

**Abilities**:
- **Mantle of Versatility**: +10% XP for diverse contributions.
- **Amulet of Adaptation**: +10 XP for CI/CD and DevOps contributions.

## 3. Items and Gear

Items enhance player abilities and provide strategic advantages. Items are earned through leveling, milestones, or rare drops.

### 3.1 Item Types and Effects
- **Weapons**: Boost "attack power" for specific tasks.
- **Armor**: Provides additional HP, increasing resilience for complex tasks.
- **Accessories**: Provide passive bonuses (e.g., XP boosts, HP regeneration).

### 3.2 Scaling XP Bonuses Per Tier
**Formula:**
\[
A_T = A_0 \times G^{(T-1)}
\]

- \( A_0 \) = Base XP bonus (e.g., 10% at Tier 1).
- \( G \) = Growth factor per tier (e.g., 1.15 for a 15% increase per tier).
- \( T \) = Item tier (1 = Level 1-100, 2 = Level 101-200).

**Example – Knight’s Sword of Fortitude**:
- **Tier 1 (Levels 1-100)**: +10% XP for bug fixes.
- **Tier 2 (Levels 101-200)**: +11.5% XP.
- **Tier 3 (Levels 201-300)**: +13.2% XP.

### 3.3 Temporary XP Boost Items
- **Victory Elixir**: +10% XP for 24 hours after winning a **Dragon Battle**.
- **Scroll of Knowledge**: 2x XP for the next **5 documentation contributions**.

## 4. Item and Ability Scaling Formulas

### 4.1 HP and Mana Bonuses (Armor & Accessories)
**HP Formula:**
\[
H_T = H_0 + (I \times (T - 1))
\]
- \( H_0 \) = Base HP bonus (5% at Tier 1).
- \( I \) = Increment per tier (2% per tier).

**Mana Formula:**
\[
M_T = 6\% + (2\% \times (T - 1))
\]

## 5. Milestones and Achievements
- **Every 10 levels**: Milestone reward item tailored to class.
- **Level 100+**: Unlock **Prestige Mode**, resetting XP while keeping **items and bonuses**.

## 6. Interface and GitLab/GitHub Integration
- **Live XP updates** via GitHub/GitLab webhooks.
- **Dashboard**: Displays level, XP, class, and equipped items.
- **Leaderboard**: Tracks top contributors by XP and class.
