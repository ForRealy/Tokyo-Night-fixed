# Customization Guide

This guide will help you customize the Tokyo Night V2 theme to your preferences.

## Color Customization

### Changing the Accent Color

The main accent color can be changed by modifying the `--accent-color` variable:

```css
.theme-dark {
  --accent-color: #7aa2f7; /* Default blue */
  /* Try these alternatives: */
  /* --accent-color: #bb9af7; Purple */
  /* --accent-color: #f7768e; Pink */
  /* --accent-color: #9ece6a; Green */
  /* --accent-color: #e0af68; Yellow */
}
```

### Background Colors

You can adjust the background colors for different areas:

```css
.theme-dark {
  /* Main chat area */
  --background-primary: #1a1b26;
  
  /* Sidebars and secondary areas */
  --background-secondary: #171722;
  
  /* Tertiary elements */
  --background-tertiary: #16161e;
  
  /* Floating elements (modals, popouts) */
  --background-floating: #161620;
}
```

### Text Colors

Modify text colors for better readability:

```css
.theme-dark {
  /* Primary text */
  --text-normal: #b1bae6;
  
  /* Secondary text */
  --text-muted: #565f89;
  
  /* Interactive elements */
  --interactive-normal: #5f647e;
  --interactive-hover: #a2a6c2;
  --interactive-active: #b5bad1;
}
```

## Font Customization

### Using Custom Fonts

To use a custom font throughout Discord:

```css
:root {
  --font-primary: 'Your Font Name', 'Fallback Font', sans-serif;
  --font-display: var(--font-primary);
}
```

### Monospace Font

Enable the monospace addon or customize it:

```css
/* Enable JetBrains Mono */
@import url("https://raw.githubusercontent.com/ForRealy/TokyoNightV2/main/src/addons/monospace-fonts.css");

/* Or use your own monospace font */
:root {
  --font-code: 'Fira Code', 'Consolas', monospace;
}
```

## Layout Customization

### Server List Width

Adjust the width of the server list:

```css
.guilds_a7e7a8 {
  width: 80px; /* Default is 72px */
}

/* Adjust content accordingly */
.base_f3f9c4 {
  left: 80px;
}
```

### Channel List Width

Modify the channel sidebar width:

```css
.sidebar_a4d4d9 {
  width: 260px; /* Default is 240px */
}

.chat_f3f9c4 {
  margin-left: 260px;
}
```

### Member List Width

Change the member list width:

```css
.members_f3f9c4 {
  width: 260px; /* Default is 240px */
}
```

## Addon Customization

### Mac Titlebar Colors

Customize the titlebar button colors:

```css
:root {
  --close-button-color: #ff5f57; /* Red */
  --minimize-button-color: #ffbd2e; /* Yellow */
  --maximize-button-color: #28ca42; /* Green */
}
```

### Square Avatar Radius

Adjust the border radius for square avatars:

```css
:root {
  --avatar-radius: 8px; /* Default is 5px */
}
```

### Compact Mode Breakpoints

Modify when compact mode activates:

```css
/* Change the breakpoint for compact mode */
@media screen and (min-width: 601px) and (max-width: 1000px) {
  /* Compact mode styles */
}

/* Change the breakpoint for very compact mode */
@media screen and (min-width: 0px) and (max-width: 700px) {
  /* Very compact mode styles */
}
```

## Advanced Customization

### Custom Scrollbars

Create custom scrollbar styles:

```css
.scrollerBase_dc00c5::-webkit-scrollbar {
  width: 8px;
}

.scrollerBase_dc00c5::-webkit-scrollbar-thumb {
  background-color: var(--accent-color);
  border-radius: 4px;
}

.scrollerBase_dc00c5::-webkit-scrollbar-track {
  background-color: var(--background-tertiary);
}
```

### Custom Animations

Add custom animations to elements:

```css
/* Smooth transitions for buttons */
.button_dd4f85 {
  transition: all 0.3s ease;
}

.button_dd4f85:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

/* Fade in animation for messages */
.message_d5deea {
  animation: fadeIn 0.3s ease-in;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}
```

### Custom Message Styling

Customize message appearance:

```css
/* Message background */
.message_d5deea {
  background-color: var(--background-secondary);
  border-radius: 8px;
  margin: 4px 0;
  padding: 8px 12px;
}

/* Username styling */
.username_d5deea {
  font-weight: 600;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.3);
}

/* Timestamp styling */
.timestamp_d5deea {
  opacity: 0.6;
  font-size: 0.75rem;
}
```

## Creating Your Own Addon

To create a custom addon:

1. Create a new CSS file in the `src/addons/` directory
2. Add your custom styles
3. Import it in the main theme file:

```css
/* Custom addon */
@import url("path/to/your/custom-addon.css");
```

Example custom addon structure:

```css
/* custom-addon.css */

/* Addon description and purpose */
/* Custom styling for [specific feature] */

/* Your custom CSS rules */
.someElement {
  /* Your styles */
}

/* Media queries for responsive design */
@media screen and (max-width: 768px) {
  /* Mobile styles */
}
```

## Tips for Customization

1. **Use CSS Variables**: Leverage the existing CSS variables for consistency
2. **Test Thoroughly**: Test your changes across different Discord features
3. **Keep Backups**: Save your customizations before making major changes
4. **Use Browser DevTools**: Inspect elements to find the correct selectors
5. **Check for Updates**: Ensure your customizations work with theme updates

## Sharing Your Customizations

If you create useful customizations:

1. Fork the repository
2. Add your customization as a new addon
3. Submit a pull request
4. Share with the community!

## Getting Help

For customization help:

1. Check the existing addons for examples
2. Use browser developer tools to inspect elements
3. Ask for help in the [Issues section](https://github.com/ForRealy/TokyoNightV2/issues)
4. Join the Discord community for real-time help