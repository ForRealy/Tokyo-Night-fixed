# Installation Guide

This guide will help you install the Tokyo Night V2 Discord theme using different methods.

## Prerequisites

Before installing the theme, you'll need one of the following:

- **BetterDiscord** (recommended for desktop)
- **Stylus browser extension** (for web Discord)

## Method 1: BetterDiscord (Recommended)

### Step 1: Install BetterDiscord

1. Download BetterDiscord from [betterdiscord.app](https://betterdiscord.app/)
2. Run the installer and follow the setup instructions
3. Restart Discord

### Step 2: Download the Theme

1. Go to the [releases page](https://github.com/ForRealy/TokyoNightV2/releases)
2. Download the latest `tokyo-night.theme.css` file
3. Or right-click [this link](https://raw.githubusercontent.com/ForRealy/TokyoNightV2/main/themes/tokyo-night.theme.css) and save as

### Step 3: Install the Theme

1. Open Discord
2. Go to Settings (gear icon)
3. Scroll down to "BetterDiscord" section
4. Click on "Themes"
5. Click "Open Themes Folder"
6. Copy the downloaded `tokyo-night.theme.css` file into this folder
7. Go back to Discord and toggle the theme on

## Method 2: Stylus Browser Extension

### Step 1: Install Stylus

1. Install Stylus for your browser:
   - [Chrome/Edge](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne)
   - [Firefox](https://addons.mozilla.org/en-US/firefox/addon/styl-us/)

### Step 2: Install the Theme

1. Download the `tokyo-night.user.css` file from [here](https://raw.githubusercontent.com/ForRealy/TokyoNightV2/main/themes/tokyo-night.user.css)
2. Open Stylus extension
3. Click "Write new style"
4. Copy and paste the contents of the `.user.css` file
5. Save the style
6. Make sure it's enabled for `discord.com`

## Method 3: Direct CSS Import (Advanced)

If you want to use the theme without downloading files:

1. In BetterDiscord, create a new theme file
2. Add this import line at the top:
   ```css
   @import url("https://raw.githubusercontent.com/ForRealy/TokyoNightV2/main/themes/tokyo-night.theme.css");
   ```

## Customization

### Enabling/Disabling Addons

The theme comes with several optional addons. To enable or disable them:

1. Open the theme file in a text editor
2. Find the addon section (around line 20)
3. To enable an addon, remove the `/*` and `*/` around the `@import` line
4. To disable an addon, add `/*` before and `*/` after the `@import` line

Example:
```css
/* Disabled addon */
/* @import url("https://raw.githubusercontent.com/ForRealy/TokyoNightV2/main/src/addons/compact-mode.css"); */

/* Enabled addon */
@import url("https://raw.githubusercontent.com/ForRealy/TokyoNightV2/main/src/addons/compact-mode.css");
```

### Available Addons

- **Revert Rebrand**: Restores classic Discord branding (enabled by default)
- **VSCode User Area**: Visual Studio Code-like interface (enabled by default)
- **Syntax Highlighting**: Enhanced code block styling (enabled by default)
- **Mac Titlebar**: macOS-style window controls (enabled by default)
- **Compact Mode**: Space-saving layout for smaller screens
- **Monospace Fonts**: JetBrains Mono font integration
- **Square Avatars**: Square-shaped user avatars
- **Username Backgrounds**: Colorful username highlighting

## Troubleshooting

### Theme Not Loading

1. Make sure BetterDiscord is properly installed and running
2. Check that the theme file is in the correct themes folder
3. Verify the theme is enabled in Discord settings
4. Try restarting Discord

### Broken Styling

1. Make sure you're using the latest version of the theme
2. Check if Discord has updated (theme may need updates)
3. Try disabling other themes or plugins that might conflict
4. Clear Discord's cache and restart

### Performance Issues

1. Disable unused addons to improve performance
2. Make sure you're using the latest version of BetterDiscord
3. Check if other themes or plugins are causing conflicts

## Getting Help

If you encounter issues:

1. Check the [Issues page](https://github.com/ForRealy/TokyoNightV2/issues) for known problems
2. Create a new issue with details about your problem
3. Include your Discord version, BetterDiscord version, and operating system

## Updates

The theme will automatically update if you're using the direct import method. For manual installations:

1. Check the [releases page](https://github.com/ForRealy/TokyoNightV2/releases) periodically
2. Download and replace the theme file when new versions are available
3. Follow the project on GitHub to get notified of updates