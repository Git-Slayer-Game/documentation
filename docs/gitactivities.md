# Git Slayer Game - GitLab/GitHub Activities and XP Rewards

The Git Slayer Game tracks contributors' activities using GitHub and GitLab webhook events, automating XP rewards, item drops, and class effects based on contributions. This updated system emphasizes frequent activities like merge requests over less common actions like releases.

---

## GitHub and GitLab Webhook Events Overview

The game uses the following webhook events to recognize user activities, reward XP, and trigger in-game effects. Rewards have been adjusted to reflect the frequency and impact of each activity.

---

### 1. Push Events

- **Event**: `push`
- **Description**: Triggered when commits are pushed to a repository.
- **XP Reward**: 
  - **Base Reward**: +10 XP per commit.
  - **Bonus XP**: +5 XP for commits tagged as bug fixes, refactors, or performance improvements.
- **Item Drop Chance**: Small chance for significant commits, such as adding new features or substantial changes.
- **Class Abilities**:
  - **Knight**: Gains bonus XP for bug fixes or performance-related commits.
  - **Sorcerer**: Gains an XP boost for introducing new libraries or technologies.

---

### 2. Pull Request / Merge Request Events

- **Event**: `pull_request` (GitHub) / `merge_request` (GitLab)
- **Description**: Triggered when a pull/merge request is created, updated, merged, or closed.
- **XP Reward**: 
  - **Merge**: +20 XP for successfully merging a request.
  - **Create/Update**: +5 XP for creating or updating a merge request.
- **Item Drop Chance**: Moderate for innovative or complex merges.
- **Class Abilities**:
  - **Knight**: Reduced cooldown on class abilities for stability/security merges.
  - **Sorcerer**: Bonus XP for innovative or challenging merges.
  - **Paladin**: Gains additional XP for merges involving multiple collaborators.

---

### 3. Issue Events

- **Event**: `issues`
- **Description**: Triggered when an issue is created, updated, or closed.
- **XP Reward**: 
  - **Closing**: +10 XP per issue.
  - **High-Priority Issues**: +5 bonus XP for closing high-priority issues.
- **Item Drop Chance**: Small chance for high-priority issue closures.
- **Class Abilities**:
  - **Knight**: Gains bonus XP for resolving security or performance-related issues.
  - **Paladin**: Gains an XP boost for resolving issues that enhance collaboration or documentation.
  - **Druid**: Gains extra XP for resolving issues that span multiple project areas.

---

### 4. Comment Events (Issues and Merge Requests)

- **Event**: `issue_comment` (GitHub) / `note` (GitLab)
- **Description**: Triggered when a comment is added to an issue or merge request.
- **XP Reward**: +5 XP for each constructive or insightful comment.
- **Item Drop Chance**: Rare chance for high-quality feedback or impactful comments.
- **Class Abilities**:
  - **Paladin**: Gains bonus XP for collaborative comments that facilitate teamwork.
  - **Druid**: Gains extra XP for comments that address cross-domain impacts (e.g., frontend and backend).

---

### 5. Release Events

- **Event**: `release`
- **Description**: Triggered when a release is published.
- **XP Reward**: **+5 XP per release**, reduced to reflect its less frequent use.
- **Item Drop Chance**: High for major releases, rare for patch-level releases.
- **Class Abilities**:
  - **Knight**: Gains small bonus XP for stability-focused releases.
  - **Sorcerer**: Gains random bonus XP for releases introducing innovative features.
  - **Druid**: Gains minor extra XP for releases that impact multiple areas.

---

## Summary of XP Rewards

| **GitLab/GitHub Activity**   | **XP Reward** | **Item Drop Chance** | **Notes**                                     |
|------------------------------|---------------|-----------------------|-----------------------------------------------|
| Push (Commit)                | +10 XP        | Low                  | Bonus XP for bug fixes and improvements.      |
| Pull/Merge Request Merged    | +20 XP        | Moderate             | Rewards emphasize merges over releases.       |
| Pull/Merge Request Created   | +5 XP         | Low                  | Reward for initiating requests.               |
| Issue Closed                 | +10 XP        | Moderate             | Extra XP for high-priority issues.            |
| Comment (Issue/PR)           | +5 XP         | Rare                 | Encourages collaborative discussions.         |
| Release Published            | +5 XP         | Low                  | Reduced due to infrequent usage.              |

---

## Integration Setup

To enable the Git Slayer Game:

1. **GitHub Setup**:
   - Go to your repository settings and navigate to **Webhooks**.
   - Add a new webhook with the target URL of the Git Slayer Game API.
   - Enable specific events: `push`, `pull_request`, `issues`, `issue_comment`, and `release`.

2. **GitLab Setup**:
   - Go to your project settings and navigate to **Webhooks**.
   - Add a new webhook pointing to the Git Slayer Game API.
   - Enable events: `Push Events`, `Merge Request Events`, `Issue Events`, `Note Events`, and `Release Events`.

3. **Game API Integration**:
   - Webhook events will send real-time activity data to the Git Slayer Game API.
   - The API processes these events to calculate XP, handle item drops, and activate class abilities.
