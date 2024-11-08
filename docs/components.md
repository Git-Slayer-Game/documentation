# Git Slayer - Game Components

Welcome to the core documentation for the **Git Slayer Game** components. This file provides an in-depth look at the game’s structure, including levels, character classes, items, milestones, and integration with GitLab/GitHub activities.

## 1. Levels and Experience Points (XP)

Contributors earn **XP** through GitLab/GitHub activities. XP allows players to level up, unlocking new abilities, items, and milestones. Here’s a breakdown of how XP is awarded based on common activities:

- **Commits**: +10 XP
- **Pull Requests Merged**: +25 XP
- **Issue Resolution**: +15 XP
- **Code Review (Approval or Comments)**: +20 XP
- **Documentation Updates**: +15 XP

Each activity contributes towards leveling up, which in turn enhances a player’s abilities, items, and class-specific bonuses.

## 2. Character Classes

Each player selects a **Character Class** based on their coding style and preferred contributions. Each class has unique abilities, items, and XP bonuses for certain activities:

### 2.1 Knight (Stability & Robustness)

**Abilities**:
- **Armor of Resilience**: Increases XP gain by 20% for bug fixes and performance improvements.
- **Shield of Fortification**: Reduces cooldown (review or merge wait time) on approved code reviews by 10%.

### 2.2 Sorcerer (Innovation & Creativity)

**Abilities**:
- **Staff of Ingenuity**: Increases XP gain by 15% for introducing new features or libraries.
- **Spell of Insight**: Provides random bonus XP for complex or innovative pull requests.

### 2.3 Paladin (Collaboration & Documentation)

**Abilities**:
- **Banner of Teamwork**: Adds +10 XP to code reviews, encouraging collaboration.
- **Book of Knowledge**: Provides a chance for rare items on significant documentation contributions.

### 2.4 Druid (Adaptability & Versatility)

**Abilities**:
- **Mantle of Versatility**: Grants XP bonuses for contributions across different areas of the project.
- **Amulet of Adaptation**: Increases XP for non-code tasks like CI/CD configurations.

## 3. Items and Gear

Items are rewards for significant contributions, milestones, or random drops. They enhance player abilities and provide strategic advantages based on the character class. Here’s a breakdown of item types and example effects.

### 3.1 Item Types and Effects

- **Weapons**: Boost "attack power" against specific tasks.
- **Armor**: Provides additional HP, increasing resilience for complex tasks.
- **Accessories**: Provide passive bonuses (e.g., HP regeneration or XP boost for collaboration).

### 3.2 Example Item Effects

Each class has unique items with scaling effects based on the player’s level tier. For each level range (1-100, 101-200, etc.), items become progressively stronger.

#### Example Items

- **Knight’s Sword of Fortitude**: Grants +10% XP for bug fixes and performance improvements.
- **Sorcerer’s Staff of Innovation**: Provides a 10% chance of bonus XP for innovative contributions.
- **Paladin’s Tome of Unity**: Adds +5 XP per code review.
- **Druid’s Amulet of Adaptability**: Increases XP by 10% for versatile contributions across different project areas.

## 4. Item and Ability Scaling Formulas

To create a scalable progression, we use formulas for item effects, ensuring that items grow in power across levels and tiers.

### 4.1 Attack Power (Weapons)

**Formula**: 
\[
A_T = A_0 \times G^{(T-1)}
\]
Where:
- \( A_0 \) = Base attack power (e.g., 10% at Tier 1).
- \( G \) = Growth factor per tier (e.g., 1.15 for a 15% increase per tier).
- \( T \) = Current item tier (e.g., 1 for levels 1-100, 2 for levels 101-200).

#### Example Calculation for **Knight's Sword of Fortitude**

1. **Tier 1 (Levels 1-100)**: \( A_1 = 10\% \)
2. **Tier 2 (Levels 101-200)**: \( A_2 = 10\% \times 1.15 = 11.5\% \)
3. **Tier 3 (Levels 201-300)**: \( A_3 = 10\% \times 1.15^2 \approx 13.2\% \)

### 4.2 HP Bonus (Armor)

**Formula**:
\[
H_T = H_0 + (I \times (T - 1))
\]
Where:
- \( H_0 \) = Base HP bonus (e.g., 5% at Tier 1).
- \( I \) = Increment per tier (e.g., 2% per tier).
- \( T \) = Current item tier.

#### Example Calculation for **Knight's Shield of Resilience**

1. **Tier 1 (Levels 1-100)**: \( H_1 = 5\% \)
2. **Tier 2 (Levels 101-200)**: \( H_2 = 5\% + 2\% = 7\% \)
3. **Tier 3 (Levels 201-300)**: \( H_3 = 5\% + 4\% = 9\% \)

### 4.3 Mana and Hybrid Bonuses (Accessories)

Items like **Druid's Amulet of Adaptability** can boost both HP and mana over levels.

#### Example

- **HP Base Increase**: 4%
- **HP Growth Increment**: 1.5% per tier
- **Mana Base Increase**: 6%
- **Mana Growth Increment**: 2% per tier

**HP Formula**:
\[
H_T = 4\% + (1.5\% \times (T - 1))
\]

**Mana Formula**:
\[
M_T = 6\% + (2\% \times (T - 1))
\]

## 5. Milestones and Achievements

Encourage ongoing engagement through achievements and milestone-based rewards:

- **Level Milestones**: Every 10 levels, players receive items tailored to their class.
- **Random Drops**: Small chance of item drops for significant contributions like high-priority issue closures.
- **Special Events**: Host monthly or seasonal challenges for exclusive items (e.g., "Winter Event Shield").

## 6. Interface Design and GitLab/GitHub Integration

An engaging user interface is crucial for tracking progress and interacting with the game:

- **Dashboard**: Displays current XP, level, class, items, and abilities.
- **Inventory**: Shows earned items, allowing players to equip or upgrade items.
- **Leaderboard**: Highlights top contributors by class, level, and XP.

**Integration**:

- **Webhooks**: Trigger XP rewards and item drops based on contributions.
- **APIs**: Fetch data like commit history, PR status, and calculate XP/item drops.
- **Notifications**: Notify players of new items or milestones via GitHub/GitLab or external channels (e.g., Slack or email).
