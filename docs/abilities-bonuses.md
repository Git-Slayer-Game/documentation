# Git Slayer - Abilities and Bonuses

This document provides details on the unique abilities and bonuses associated with each class in the **Git Slayer Game**. Each class has its own set of abilities that enhance specific GitLab/GitHub activities. Abilities are designed to scale with each tier, making them progressively more powerful as players level up.

## 1. Abilities Overview by Class

Each class has two unique abilities that provide bonuses in specific areas. Abilities scale based on tiers, ensuring that bonuses stay impactful as contributors level up.

### Knight (Stability & Robustness)

1. **Armor of Resilience**: Increases XP gain for bug fixes and performance improvements.
   - **Formula**:
     \[
     XP_{bonus} = XP_{base} \times (1 + R \times (T - 1))
     \]
   - Where:
     - \( XP_{base} \): Base XP gain (e.g., 10%).
     - \( R \): Scaling rate per tier (e.g., 0.2 for a 20% increase).
     - \( T \): Current tier.

   - **Example Calculation**:
     - **Tier 1**: \( XP_{bonus} = 10\% \)
     - **Tier 2**: \( XP_{bonus} = 10\% + (10\% \times 0.2) = 12\% \)
     - **Tier 3**: \( XP_{bonus} = 12\% + (12\% \times 0.2) = 14.4\% \)

2. **Shield of Fortification**: Reduces the cooldown (review/merge wait time) on approved code reviews.
   - **Formula**:
     \[
     Cooldown_{reduction} = C_{base} \times (1 - (R \times (T - 1)))
     \]
   - Where:
     - \( C_{base} \): Base cooldown reduction (e.g., 10%).
     - \( R \): Reduction factor per tier (e.g., 0.1).
     - \( T \): Current tier.

   - **Example Calculation**:
     - **Tier 1**: 10% reduction.
     - **Tier 2**: 11%.
     - **Tier 3**: 12.1%.

---

### Sorcerer (Innovation & Creativity)

1. **Staff of Ingenuity**: Increases XP gain for introducing new features or libraries.
   - **Formula**:
     \[
     XP_{bonus} = XP_{base} \times (1 + I \times (T - 1))
     \]
   - Where:
     - \( XP_{base} \): Base XP gain (e.g., 15%).
     - \( I \): Increase factor per tier (e.g., 0.15 for 15%).
     - \( T \): Current tier.

   - **Example Calculation**:
     - **Tier 1**: 15%.
     - **Tier 2**: 17.25%.
     - **Tier 3**: 19.8%.

2. **Spell of Insight**: Random bonus XP for complex or innovative pull requests.
   - **Formula**:
     \[
     Bonus\_XP = Base\_XP \times Random\_Factor
     \]
   - The random factor varies per tier, increasing the chance and size of the bonus.

---

### Paladin (Collaboration & Documentation)

1. **Banner of Teamwork**: Adds bonus XP for code reviews.
   - **Formula**:
     \[
     XP_{bonus} = XP_{base} + (B \times (T - 1))
     \]
   - Where:
     - \( XP_{base} \): Base XP for code reviews (e.g., +10 XP).
     - \( B \): Bonus increment per tier (e.g., +2 XP).
     - \( T \): Current tier.

   - **Example Calculation**:
     - **Tier 1**: 10 XP.
     - **Tier 2**: 12 XP.
     - **Tier 3**: 14 XP.

2. **Book of Knowledge**: Increases chance for rare item drops on documentation contributions.
   - **Formula**:
     \[
     Drop\_Chance = Base\_Chance \times (1 + D \times (T - 1))
     \]
   - Where:
     - \( Base\_Chance \): Initial drop chance (e.g., 5%).
     - \( D \): Drop rate increment (e.g., 0.05 for each tier).
     - \( T \): Current tier.

   - **Example Calculation**:
     - **Tier 1**: 5%.
     - **Tier 2**: 5.5%.
     - **Tier 3**: 6%.

---

### Druid (Adaptability & Versatility)

1. **Mantle of Versatility**: Grants XP bonuses for contributions across various project areas.
   - **Formula**:
     \[
     XP_{bonus} = XP_{base} \times (1 + V \times (T - 1))
     \]
   - Where:
     - \( XP_{base} \): Base XP gain (e.g., 10%).
     - \( V \): Versatility increment (e.g., 0.2 for 20%).
     - \( T \): Current tier.

   - **Example Calculation**:
     - **Tier 1**: 10%.
     - **Tier 2**: 12%.
     - **Tier 3**: 14.4%.

2. **Amulet of Adaptation**: Increases XP for non-code tasks like CI/CD configurations.
   - **Formula**:
     \[
     XP_{bonus} = XP_{base} + (A \times (T - 1))
     \]
   - Where:
     - \( XP_{base} \): Initial XP boost (e.g., +8 XP).
     - \( A \): Adaptation bonus per tier (e.g., +2 XP).
     - \( T \): Current tier.

   - **Example Calculation**:
     - **Tier 1**: 8 XP.
     - **Tier 2**: 10 XP.
     - **Tier 3**: 12 XP.

---

## 2. Summary Table of Abilities

| Class      | Ability Name          | Tier 1 Effect                        | Tier 2 Effect                      | Tier 3 Effect                      |
|------------|------------------------|--------------------------------------|------------------------------------|------------------------------------|
| **Knight** | Armor of Resilience    | +10% XP for bug fixes                | +12% XP                            | +14.4% XP                          |
|            | Shield of Fortification| -10% cooldown                        | -11% cooldown                      | -12.1% cooldown                    |
| **Sorcerer**| Staff of Ingenuity    | +15% XP for new features             | +17.25% XP                         | +19.8% XP                          |
|            | Spell of Insight       | Random bonus XP                      | Increased chance                   | Higher chance and bonus            |
| **Paladin**| Banner of Teamwork     | +10 XP for code reviews              | +12 XP                             | +14 XP                             |
|            | Book of Knowledge      | 5% rare item drop on docs            | 5.5% drop chance                   | 6% drop chance                     |
| **Druid**  | Mantle of Versatility  | +10% XP for versatile contributions  | +12% XP                            | +14.4% XP                          |
|            | Amulet of Adaptation   | +8 XP for non-code tasks             | +10 XP                             | +12 XP                             |
