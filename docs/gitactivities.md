# Git Slayer Game - GitLab/GitHub Activities and XP Rewards

The Git Slayer Game uses GitHub and GitLab webhook events to track contributors' activities in real time. These events allow us to automate XP rewards, item drops, and other in-game effects based on specific actions in the repositories. This document outlines the activities recognized by GitHub and GitLab and how each action contributes to the game.

## GitHub and GitLab Webhook Events Overview

The following webhook events are utilized to capture user activities, reward XP, and trigger item drops or class abilities based on contribution type. Each action is matched to its associated XP reward and other potential in-game effects.

### 1. Push Events

- **Event**: `push`
- **Description**: Triggered when commits are pushed to a repository.
- **GitHub Equivalent**: [Push Event](https://docs.github.com/en/developers/webhooks-and-events/webhooks/webhook-events-and-payloads#push)
- **GitLab Equivalent**: [Push Event](https://docs.gitlab.com/ee/user/project/integrations/webhooks.html#push-events)
- **In-Game Impact**:
  - **XP Reward**: +10 XP per commit.
  - **Item Drop Chance**: Small chance of random item drop for significant commits (e.g., refactoring or large feature addition).
  - **Class Ability Activation**:
    - **Knight**: Additional XP for performance improvement or bug fix-related commits.
    - **Sorcerer**: XP boost if the commit introduces a new technology or library.

### 2. Pull Request / Merge Request Events

- **Event**: `pull_request` (GitHub) / `merge_request` (GitLab)
- **Description**: Triggered when a pull/merge request is created, updated, merged, or closed.
- **GitHub Equivalent**: [Pull Request Event](https://docs.github.com/en/developers/webhooks-and-events/webhooks/webhook-events-and-payloads#pull_request)
- **GitLab Equivalent**: [Merge Request Event](https://docs.gitlab.com/ee/user/project/integrations/webhooks.html#merge-requests-events)
- **In-Game Impact**:
  - **XP Reward**: +25 XP for each merged pull/merge request.
  - **Item Drop Chance**: Higher chance of item drop for complex or innovative merges.
  - **Class Ability Activation**:
    - **Knight**: Reduced cooldown on merge approvals due to stability and security checks.
    - **Sorcerer**: Chance of bonus XP for innovative or complex pull requests.
    - **Paladin**: Additional XP for collaborative pull requests involving multiple reviewers.

### 3. Issue Events

- **Event**: `issues`
- **Description**: Triggered when an issue is created, updated, or closed.
- **GitHub Equivalent**: [Issues Event](https://docs.github.com/en/developers/webhooks-and-events/webhooks/webhook-events-and-payloads#issues)
- **GitLab Equivalent**: [Issue Event](https://docs.gitlab.com/ee/user/project/integrations/webhooks.html#issues-events)
- **In-Game Impact**:
  - **XP Reward**: +15 XP for closing an issue.
  - **Item Drop Chance**: Small chance of item drop for high-priority issue closures.
  - **Class Ability Activation**:
    - **Knight**: Bonus XP for security or performance-related issue resolutions.
    - **Paladin**: XP boost for resolving issues that enhance documentation or collaboration.
    - **Druid**: Extra XP for resolving issues across different areas (e.g., frontend and backend).

### 4. Comment Events (Issues and Pull Requests)

- **Event**: `issue_comment` (GitHub) / `note` (GitLab)
- **Description**: Triggered when a comment is added to an issue or pull request.
- **GitHub Equivalent**: [Issue Comment Event](https://docs.github.com/en/developers/webhooks-and-events/webhooks/webhook-events-and-payloads#issue_comment)
- **GitLab Equivalent**: [Note Event](https://docs.gitlab.com/ee/user/project/integrations/webhooks.html#comments)
- **In-Game Impact**:
  - **XP Reward**: +5 XP for each constructive comment or feedback.
  - **Item Drop Chance**: Occasional random item drop for high-quality feedback.
  - **Class Ability Activation**:
    - **Paladin**: XP boost for collaborative comments that facilitate teamwork.
    - **Druid**: Bonus XP for comments that span multiple areas (e.g., discussing both backend and frontend impacts).

### 5. Release Events

- **Event**: `release`
- **Description**: Triggered when a release is published.
- **GitHub Equivalent**: [Release Event](https://docs.github.com/en/developers/webhooks-and-events/webhooks/webhook-events-and-payloads#release)
- **GitLab Equivalent**: [Release Event](https://docs.gitlab.com/ee/user/project/integrations/webhooks.html#releases)
- **In-Game Impact**:
  - **XP Reward**: +30 XP for each release, representing the significant effort in delivering new features or versions.
  - **Item Drop Chance**: Higher chance of rare item drop for major releases.
  - **Class Ability Activation**:
    - **Knight**: Additional XP for stability-focused releases.
    - **Sorcerer**: Random bonus XP for releases with innovative features.
    - **Druid**: Extra XP for versatile releases that impact multiple project areas.

## Summary of XP Rewards

| GitLab/GitHub Activity       | XP Reward | Item Drop Chance       | Notes                                             |
|------------------------------|-----------|-------------------------|---------------------------------------------------|
| Push (Commit)                | +10 XP    | Low                    | Higher XP for bug fixes and performance tweaks.   |
| Pull/Merge Request Merged    | +25 XP    | Moderate               | Higher drop rate for complex/innovative requests. |
| Issue Closed                 | +15 XP    | Low                    | Extra XP for resolving high-priority issues.      |
| Comment (Issue/PR)           | +5 XP     | Occasional             | Rewarding constructive feedback and collaboration.|
| Release Published            | +30 XP    | High for major releases| Significant reward for version releases.          |

## Integration Setup

To use these webhooks for game activities, you will need to configure GitHub and GitLab webhook settings for each repository linked to the Git Slayer Game. Once configured, each webhook will send activity data to the game’s API, where XP, item drops, and class abilities are processed based on contribution types.

### Configuring Webhooks

1. **GitHub**:
   - Go to your repository’s settings and navigate to **Webhooks**.
   - Add a new webhook with the target URL of the Git Slayer Game API.
   - Select individual events (e.g., `push`, `pull_request`, `issues`, `issue_comment`, `release`) to monitor the specific activities listed above.

2. **GitLab**:
   - Go to your repository’s settings and navigate to **Webhooks**.
   - Add a new webhook pointing to the Git Slayer Game API.
   - Enable the desired events (e.g., `Push Events`, `Merge Request Events`, `Issue Events`, `Note Events`, `Release Events`).

With these configurations, your game API will receive real-time data, allowing it to calculate XP, handle item drops, and activate class abilities as players contribute to the project.