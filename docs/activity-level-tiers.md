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

To create a more engaging experience:
- **Levels 1-50** should be fast and rewarding.
- **Levels 51-100** should take about one month for active contributors.
- **Levels 101+** should slow down considerably for long-term engagement.
- **Milestone Dragon Battles** at **Levels 10, 25, 50, 75, and 100** provide team-based challenges.
- **Post-Level 100 Dragon Battles** introduce greater challenges with dynamic XP scaling.

## 2. XP Rewards by Activity

Contributors earn XP through GitLab/GitHub activities. Here’s a summary of the XP awarded for each activity:

| **Activity**              | **XP (Levels 1-50)** | **XP (Levels 51-100)** | **XP (Levels 101+)** |
|---------------------------|----------------------|----------------------|------------------|
| **Commits**                | 15 XP               | 10 XP               | 8 XP            |
| **Pull Requests Merged**   | 35 XP               | 30 XP               | 25 XP           |
| **Issue Resolution**       | 20 XP               | 15 XP               | 12 XP           |
| **Code Review**            | 30 XP               | 25 XP               | 20 XP           |
| **Documentation Updates**  | 25 XP               | 20 XP               | 15 XP           |

XP rewards apply dynamically, with boosts for significant contributions and milestone events.

## 3. Post-Level 100 Dragon Battles Formula

After Level 100, **Dragon Battles** introduce an additional layer of challenge, requiring collective XP contributions to defeat progressively stronger dragons.

**Dragon XP Requirement Formula**:
\[
D_T = D_0 \times (1.25^{(T - 1)})
\]

- \( D_0 \): Base XP requirement for the first post-100 battle (e.g., 10,000 XP).
- \( 1.25 \): Scaling factor, increasing difficulty with each battle.
- \( T \): Battle tier (1 for Level 110, 2 for Level 120, etc.).

**Example Calculation**:
- **Level 110 Dragon**: 10,000 XP required.
- **Level 120 Dragon**: 10,000 × 1.25 = 12,500 XP.
- **Level 130 Dragon**: 12,500 × 1.25 = 15,625 XP.

These battles require teamwork and increased contribution, ensuring sustained engagement beyond Level 100.

## 4. Class-Specific Item Scaling

Each class has unique items with effects that grow stronger as the player levels up. Item effects are designed to scale by tier to keep them relevant as contributors progress.

### 4.1 Item Scaling Formulas

#### Attack Power Formula (for Weapons)

**Formula**:
\[
A_T = A_0 \times G^{(T-1)}
\]

- \( A_0 \): Base attack power increase (e.g., 10% at Tier 1).
- \( G \): Growth factor per tier (e.g., 1.15 for a 15% increase).
- \( T \): Current tier (1 for levels 1-100, 2 for levels 101-200, etc.).

#### HP Bonus Formula (for Armor)

**Formula**:
\[
H_T = H_0 + (I \times (T - 1))
\]

- \( H_0 \): Base HP increase (e.g., 5% at Tier 1).
- \( I \): Increment per tier (e.g., 2%).
- \( T \): Current tier.

## 5. Example Class-Specific Item Effects Across Tiers

### Knight (Stability & Robustness)
- **Weapon: Sword of Fortitude**
  - Tier 1: +10% XP for bug fixes and performance improvements.
  - Tier 2: +11.5% XP boost.
  - Tier 3: +13.2% XP boost.

### Sorcerer (Innovation & Creativity)
- **Weapon: Staff of Ingenuity**
  - Tier 1: +12% XP for introducing new features.
  - Tier 2: +13.8% XP.
  - Tier 3: +15.9% XP.

### Paladin (Collaboration & Documentation)
- **Weapon: Banner of Teamwork**
  - Tier 1: +10 XP to all code reviews.
  - Tier 2: +11 XP.
  - Tier 3: +12 XP.

### Druid (Adaptability & Versatility)
- **Accessory: Amulet of Adaptability**
  - Tier 1: +10% XP for versatile contributions.
  - Tier 2: +12% XP.
  - Tier 3: +14% XP.

## 6. Progressive Item Rarity and Random Drops

To keep contributors engaged, items have rarity levels that provide additional or unique effects:

- **Common**: Basic stats, frequently awarded.
- **Rare**: Enhanced stats, awarded for milestone achievements.
- **Epic/Legendary**: Powerful and unique abilities, awarded through special events or random drops.

## 7. Item Acquisition Criteria and Milestones

- **Milestone-Based Rewards**: Award items every 10 levels, with stronger versions available at higher tiers.
- **Dragon Battles**: Special events at **Levels 10, 25, 50, 75, 100, and beyond**.
- **Prestige System**: After Level 100, players can reset XP to earn exclusive leaderboard positions.

## 8. Implementation and Balancing

### Balancing Item Acquisition
Item acquisition rates are balanced to maintain engagement:
- **Levels 1-10**: Frequent common items to introduce players to the system.
- **Levels 10-100**: Slower acquisition, with more impactful items.
- **Post Level 100**: Increased rarity, occasional epic drops.
