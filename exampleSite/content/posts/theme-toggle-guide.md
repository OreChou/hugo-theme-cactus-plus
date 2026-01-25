---
title: "Theme Toggle User Guide"
date: 2026-01-25T12:00:00+08:00
draft: false
tags:
  - tutorial
  - theme
categories:
  - user guide
---

Bat theme has a powerful built-in theme toggle feature, allowing you to easily switch between dark and light modes.

## How to Use

### Page Toggle Button

In the bottom right corner of the page, you'll see a **toggle switch**:

- 🌙 Dark mode
- ☀️ Light mode

Simply click the switch to toggle between the two themes.

### System Theme Auto-Detection

On first visit, the theme automatically detects your system preference:

- If your system is set to dark mode, the page will display the dark theme
- If your system is set to light mode, the page will display the light theme

### Theme Memory

The theme remembers your choice:

- After manually switching themes, your preference is saved
- On your next visit, it will automatically use your last chosen theme
- Unless you manually switch again, it won't automatically change

## Theme Color Schemes

### Dark Mode

- Background: `#1d1f21` (dark gray-black)
- Text: `#c9cacc` (light gray-white)
- Accent: `#2bbc8a` (green)

Perfect for nighttime browsing, easy on the eyes.

### Light Mode

- Background: `#FFFFFF` (pure white)
- Text: `#383838` (dark gray)
- Accent: `#2bbc8a` (green)

Perfect for daytime browsing, clear and bright.

## Custom Theme Colors

You can set the default theme in your `config.toml`:

```toml
[params]
  colortheme = "light"  # Options: dark, light
```

Or simply switch on the page - your choice will override the default setting.

## Technical Implementation

Theme toggle is implemented using the following modern technologies:

- **CSS Variables**: Runtime dynamic color switching
- **localStorage API**: Browser local storage
- **Media Queries**: Detect system theme preference
- **Vanilla JavaScript**: No third-party dependencies

## FAQ

### Q: After switching themes and refreshing the page, does it return to the default theme?

A: No. Your choice is saved in browser local storage.

### Q: Can I use theme toggle on mobile?

A: Yes. The theme toggle button is available on all devices.

### Q: How do I make the theme default to dark mode?

A: Set `colortheme = "dark"` in your `config.toml`.

Enjoy a comfortable reading experience! 🌓
