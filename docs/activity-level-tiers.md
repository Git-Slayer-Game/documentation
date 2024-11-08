# Git Slayer - Activity Level Tiers

This document provides a structured approach to level progression, item scaling, and calculations for the **Git Slayer Game**. It outlines how XP rewards from activities contribute to level-ups, explains item effect formulas, and provides examples of class-specific item effects across multiple tiers.

## 1. Level Progression and Tiers

Contributors progress through levels by earning XP from various activities. The levels are grouped into tiers to introduce progressively powerful items and abilities as players advance.

### Level Tiers
- **Tier 1**: Levels 1-100
- **Tier 2**: Levels 101-200
- **Tier 3**: Levels 201-300
- **Further Tiers**: Continue in increments of 100 levels

As contributors reach a new tier, they gain access to stronger versions of class-specific items and unique effects tailored to higher-level achievements.

## 2. XP Rewards by Activity

Contributors earn XP through GitLab/GitHub activities. Here’s a summary of the XP awarded for each activity:

- **Commits**: +10 XP
- **Pull Requests Merged**: +25 XP
- **Issue Resolution**: +15 XP
- **Code Review (Approval or Comments)**: +20 XP
- **Documentation Updates**: +15 XP

These XP rewards apply across all tiers, and each level-up is achieved by accumulating enough XP, with milestones every 10 levels.

## 3. Class-Specific Item Scaling

Each class has unique items with effects that grow stronger as the player levels up. Item effects are designed to scale by tier to keep them relevant as contributors progress.

### 3.1 Item Scaling Formulas

#### Attack Power Formula (for Weapons)

Weapons increase attack power, which translates into XP bonuses for contributions specific to each class.

**Formula**:
\[
A_T = A_0 \times G^{(T-1)}
\]

- \( A_0 \): Base attack power increase (e.g., 10% at Tier 1).
- \( G \): Growth factor per tier (e.g., 1.15 for a 15% increase).
- \( T \): Current tier (1 for levels 1-100, 2 for levels 101-200, etc.).

**Example Calculation for Knight’s Sword of Fortitude**:
- **Tier 1 (Levels 1-100)**: \( A_1 = 10\% \)
- **Tier 2 (Levels 101-200)**: \( A_2 = 10\% \times 1.15 = 11.5\% \)
- **Tier 3 (Levels 201-300)**: \( A_3 = 10\% \times 1.15^2 \approx 13.2\% \)

#### HP Bonus Formula (for Armor)

Armor increases HP, making contributors more resilient in complex or long-term tasks.

**Formula**:
\[
H_T = H_0 + (I \times (T - 1))
\]

- \( H_0 \): Base HP increase (e.g., 5% at Tier 1).
- \( I \): Increment per tier (e.g., 2%).
- \( T \): Current tier.

**Example Calculation for Knight’s Shield of Resilience**:
- **Tier 1 (Levels 1-100)**: \( H_1 = 5\% \)
- **Tier 2 (Levels 101-200)**: \( H_2 = 5\% + 2\% = 7\% \)
- **Tier 3 (Levels 201-300)**: \( H_3 = 5\% + 4\% = 9\% \)

#### Mana and Hybrid Bonuses (Accessories)

Accessories provide both HP and mana bonuses that scale with levels, suited for hybrid roles.

**HP Formula**:
\[
H_T = 4\% + (1.5\% \times (T - 1))
\]

**Mana Formula**:
\[
M_T = 6\% + (2\% \times (T - 1))
\]

**Example Calculation for Druid’s Amulet of Adaptability**:
- **HP**: 
  - **Tier 1**: \( H_1 = 4\% \)
  - **Tier 2**: \( H_2 = 4\% + 1.5\% = 5.5\% \)
  - **Tier 3**: \( H_3 = 4\% + 3\% = 7\% \)
- **Mana**:
  - **Tier 1**: \( M_1 = 6\% \)
  - **Tier 2**: \( M_2 = 6\% + 2\% = 8\% \)
  - **Tier 3**: \( M_3 = 6\% + 4\% = 10\% \)

## 4. Example Class-Specific Item Effects Across Tiers

Each class has unique items that scale with levels, offering targeted benefits that enhance their preferred activities.

### Knight (Stability & Robustness)
- **Weapon: Sword of Fortitude**
  - Tier 1: +10% XP for bug fixes and performance improvements.
  - Tier 2: +11.5% XP boost.
  - Tier 3: +13.2% XP boost.
- **Armor: Shield of Resilience**
  - Tier 1: +5% HP.
  - Tier 2: +7% HP.
  - Tier 3: +9% HP.

### Sorcerer (Innovation & Creativity)
- **Weapon: Staff of Ingenuity**
  - Tier 1: +12% XP for introducing new features.
  - Tier 2: +13.8% XP.
  - Tier 3: +15.9% XP.
- **Accessory: Spellbook of Insight**
  - Tier 1: +5% chance of bonus XP for complex pull requests.
  - Tier 2: +7% chance.
  - Tier 3: +9% chance.

### Paladin (Collaboration & Documentation)
- **Weapon: Banner of Teamwork**
  - Tier 1: +10 XP to all code reviews.
  - Tier 2: +11 XP.
  - Tier 3: +12 XP.
- **Armor: Tome of Unity**
  - Tier 1: +5 XP per documentation update.
  - Tier 2: +6 XP.
  - Tier 3: +7 XP.

### Druid (Adaptability & Versatility)
- **Accessory: Amulet of Adaptability**
  - Tier 1: +10% XP for versatile contributions.
  - Tier 2: +12% XP.
  - Tier 3: +14% XP.
- **Armor: Mantle of Versatility**
  - Tier 1: +5% HP, +6% mana.
  - Tier 2: +5.5% HP, +8% mana.
  - Tier 3: +7% HP, +10% mana.

## 5. Progressive Item Rarity and Random Drops

To keep contributors engaged, items have rarity levels that provide additional or unique effects:

- **Common**: Basic stats, frequently awarded.
- **Rare**: Enhanced stats, awarded for milestone achievements.
- **Epic/Legendary**: Powerful and unique abilities, awarded through special events or random drops.

### Random Item Drops
Occasional random drops are awarded for significant contributions (e.g., merging complex pull requests), offering a small chance of obtaining rare or legendary items.

## 6. Item Acquisition Criteria and Milestones

Items are awarded based on significant achievements or milestones:

- **Milestone-Based Rewards**: Award items every 10 levels, with stronger versions available at higher tiers.
- **Event-Based Drops**: Specific activities trigger item rewards:
  - **Bug Fixing**: Rewards Knights with defensive items.
  - **Feature Development**: Rewards Sorcerers with creative items.
  - **Documentation**: Rewards Paladins with collaborative items.
  - **Versatile Contributions**: Rewards Druids with adaptable items.

## 7. Implementation and Balancing

### Balancing Item Acquisition
Item acquisition rates are balanced to maintain engagement:
- **Levels 1-10**: Frequent common items to introduce players to the system.
- **Levels 10-100**: Slower acquisition, with more impactful items.
- **Post Level 100**: Increased rarity, occasional epic drops.
