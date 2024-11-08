# Git Slayer - Interface Guide

This document provides an overview of the **Git Slayer Game** interface as it integrates with GitHub/GitLab through a Chrome/Firefox addon. The addon enhances the GitHub/GitLab experience by overlaying game elements, providing visual and interactive feedback, and responding to in-game events like leveling up, defeating dragons, or facing defeat.

## 1. Interface Overview

The **Git Slayer** interface is designed to interact directly with contributors’ activities on GitHub/GitLab. By integrating with a browser addon, we can enhance the interface with custom animations, notifications, and overlays without altering the core GitHub/GitLab interface. This approach ensures a seamless, immersive experience that maintains the familiarity of the GitHub/GitLab environment while introducing game elements.

### Key Features of the Interface

- **XP and Level Display**: Visual tracker for XP, levels, and progress towards the next level.
- **Class and Equipment Panel**: Displays class information, equipped items, and active bonuses.
- **Game Notifications**: Real-time notifications for achievements, milestones, and significant actions.
- **Dynamic Responses**: The interface reacts to game events with animations and sounds (e.g., celebrating level-ups, notifying item drops, or showing visual effects during battles).
- **Break/Fail Visuals**: When the player "dies" or loses a conflict, the interface can display “broken” effects, blurring or distorting the screen temporarily.
- **Victory Celebrations**: When defeating a dragon or achieving major milestones, celebratory effects (e.g., fireworks, confetti) overlay the screen, making accomplishments feel impactful.

## 2. Interface Components

### 2.1 XP and Level Tracker

The XP and level tracker sits prominently in the addon overlay, showing current XP, level, and progress to the next level. This bar updates dynamically with every activity on GitHub/GitLab that earns XP.

- **Location**: Top-right corner or a sidebar overlay.
- **Details**: Displays current level, XP, and a progress bar to the next level.
- **Animation**: Pulses or flashes on leveling up, making progress visually rewarding.

### 2.2 Class and Equipment Panel

The Class and Equipment panel provides an overview of the player's chosen class, current items, and bonuses. Players can view their class abilities and items, seeing how these impact their contributions.

- **Location**: Accessible from a floating icon or a sidebar.
- **Details**: Displays current class, active abilities, and equipped items. Allows quick access to view bonuses and effects.
- **Animation**: Items glow or emit subtle animations, especially when new items are earned or equipped.

### 2.3 Game Notifications and Achievements

Notifications appear in real-time for activities like leveling up, earning new items, completing milestones, or contributing to significant events. Notifications can be color-coded or themed to match the nature of the achievement (e.g., green for leveling up, purple for rare item drops).

- **Location**: Bottom-right corner, with notifications stacking if multiple events occur.
- **Details**: Displays short descriptions, such as “Level Up! Reached Level 10!” or “You’ve earned the Knight’s Shield of Resilience.”
- **Animation**: Notifications slide in with sound effects, then fade out after a few seconds.

### 2.4 Interface Reactions to Game Events

The interface will respond dynamically based on the player’s game status, such as successes and defeats. These responses make the experience more immersive and reinforce the stakes in key game events.

#### Death or Defeat

When a player "dies" or fails to meet specific requirements (e.g., losing a dragon battle or missing a milestone), the interface will display “broken” or “shattered” visual effects:

- **Screen Crack Effect**: A cracked glass overlay appears on the screen, indicating the player’s defeat.
- **Screen Blur/Distortion**: The interface distorts or blurs slightly, simulating disorientation.
- **Fading Effect**: The display dims momentarily, with “Retry” or “Revive” options if applicable.

This “break” effect remains for a few seconds, then fades out, allowing players to resume normal activities.

#### Victory Celebration

When players win significant conflicts, such as a dragon battle, or reach key milestones, the interface celebrates their achievement in a memorable way:

- **Confetti and Fireworks**: Confetti or fireworks overlay the screen, lasting a few seconds.
- **Sound Effects**: A celebratory sound or music clip plays briefly.
- **Victory Banner**: A banner with the text “Victory!” or “Dragon Defeated!” flashes across the screen.

Celebrations should be short and impactful, giving players a sense of accomplishment without distracting them for too long.

### 2.5 Real-Time Stat Updates

As players earn XP, level up, or equip new items, their stats update in real-time:

- **XP Bar Animation**: The XP bar animates smoothly to reflect new XP gains.
- **Level Up Effects**: When a level-up occurs, the interface briefly highlights the level tracker with special effects.
- **Equipment Update**: Newly equipped items or changes in gear appear immediately in the Class and Equipment panel, showing new effects and bonuses.

## 3. Integration with GitHub/GitLab Activities

The **Git Slayer** interface relies on GitHub/GitLab activities to update stats and trigger events. Webhooks in GitHub/GitLab notify the addon of actions like commits, pull requests, and issues, allowing it to update XP, trigger item drops, and display notifications.

### Activity Mappings and Triggers

- **Commits**: +10 XP, visual notification of XP gain.
- **Pull Requests Merged**: +25 XP, potential for rare item drops with visual and sound notifications.
- **Issue Resolution**: +15 XP, increases progress in XP bar with minor animation.
- **Code Reviews**: +20 XP, collaboration bonuses trigger depending on class abilities.
- **Documentation Updates**: +15 XP, special bonuses for Paladin class with animation on bonus activation.

These activities are tracked in real-time, with the interface responding immediately to changes. Each activity type is mapped to specific animations, ensuring that contributors are rewarded for all efforts, big and small.

## 4. Chrome/Firefox Addon Installation

To access the **Git Slayer Game** features, users need to install the Git Slayer addon for Chrome or Firefox.

1. **Install Addon**: Users can install the addon from the Chrome Web Store or Firefox Add-ons.
2. **Authorize with GitHub/GitLab**: Upon installation, users will authorize the addon with their GitHub or GitLab account, enabling it to receive activity updates via webhooks.
3. **Configure Preferences**: After installation, players can configure sound and animation preferences in the settings menu.

## 5. Customization and Preferences

To accommodate different user preferences, the addon allows customization of animations, sound effects, and notifications:

- **Enable/Disable Sound**: Users can toggle sound effects for a quieter experience.
- **Adjust Animation Intensity**: Users can choose between minimal, moderate, and full animation settings.
- **Notification Preferences**: Users can opt to receive notifications for only major achievements or all events.
