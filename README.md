# 🏴‍☠️ BlackP3arl Theme for Obsidian

**BlackP3arl** is a high-contrast, brutalist cyberpunk theme designed for the Obsidian knowledge base. It merges the commanding presence of the **Anton** typeface with a unique hybrid rendering engine that combines hard brutalist shadows with crisp neon halos.

![BlackP3arl Theme Showcase](https://github.com/ledokter/obsidian-BlackPe4rl-theme/raw/main/SHOWCASE.webp)

## ✨ Core Aesthetics 

*   **Typography**: Powered by **Anton** (via Google Fonts) for impactful, blocky headings, paired with **Space Mono** for a technical, code-like interface feel.
*   **The Hybrid Glow**: A custom CSS text-shadow technique that layers a sharp white core, a vibrant colored halo, and a hard black drop shadow. This creates a "levitating neon" effect that remains strictly legible.
*   **Imperial Hierarchy**: A 12-stage color system ranging from "Hot" (Action/Crimson) to "Cold" (Archive/Lilac).
*   **Deep Immersion**: Optimized solely for Dark Mode to maximize contrast and neon luminance.

## 🎨 The Imperial Color System

The theme organizes your vault's temperature from hot to cold:

| Level | Role | Color | Hex |
| :--- | :--- | :--- | :--- |
| **H1** | Critical / Alert | **Crimson** | `#DC143C` |
| **H2** | High Priority | **Tomato** | `#FF6347` |
| **H3** | Active | **Orange** | `#FFA500` |
| **H4** | Standard | **Gold** | `#FFD700` |
| **H5** | Information | **Cyan** | `#00CED1` |
| **H6** | Reference | **Royal Blue** | `#4169E1` |

*Folders and tags follow a similar violet-to-lilac spectrum for "Cold" storage.*

## 🛠️ Installation

### Option 1: Obsidian Community Themes (Recommended)
1.  Open Obsidian **Settings**.
2.  Go to **Appearance** > **Themes**.
3.  Click **Manage**.
4.  Search for `BlackP3arl`.
5.  Click **Install** and **Use**.

### Option 2: BRAT Plugin (For Beta Testing)
1.  Install the **BRAT** plugin via Community Plugins.
2.  Add beta theme with repository: `https://github.com/ledokter/obsidian-BlackPe4rl-theme`.

### Option 3: Manual Installation
1.  Download `theme.css` and `manifest.json` from the [Releases](https://github.com/ledokter/obsidian-BlackPe4rl-theme/releases) page.
2.  Navigate to your vault's hidden folder: `.obsidian/themes/`.
3.  Create a folder named `BlackP3arl`.
4.  Paste the files inside.
5.  Select **BlackP3arl** in Obsidian Appearance settings.

## � Design Manifestos

This theme isn't just a skin; it's a modular system built on strict architectural principles. **Nothing is left to chance.**

Unlike standard themes, this classification system avoids arbitrary aesthetic choices. Every font size and color shade is the result of **precise mathematical calculations** (rooted in the Golden Ratio φ) as documented in the attached files:

### 1. The Chromatic Codex (`Couleurs.md`)
This document outlines the **Imperial Hierarchy System**, a 12-level color scale designed to visualize information temperature.
*   **Usage**: Refer to this file when adding new custom CSS classes or extending the theme to other apps (like VS Code or Terminal).
*   **Structure**: It defines the exact HSL/Hex values for:
    *   **The Hot Zone (Action)**: From `Crimson` (Immediate Attention) to `Royal Blue` (Cold Storage).
    *   **The Cold Zone (Archive)**: A spectrum of purples and lilacs for folder organization.
    *   **Neon Physics**: The specific glow ratios used to create the signature "levitating text" effect.

### 2. The Typographic Standard (`Polices.md`)
This file details the **Brutalist Typesetting Engine** that powers BlackP3arl.
*   **Usage**: Consult this guide if you want to tweak font sizes while maintaining perfect harmonic proportions.
*   **Core Logic**:
    *   **Golden Ratio Scaling**: All headings are sized using a strict mathematical progression based on Φ (1.618), ensuring natural visual harmony even at massive sizes.
    *   **Font Selection**: Explains the strategic pairing of **Anton** (Impact, Warning, Strength) for headers and **Space Mono** (Data, Precision, Code) for interface elements.
    *   **Kerning & Leading**: Specific tracking values to ensure the brutalist text remains legible.

## 🤝 Contributing
Bug reports and pull requests are welcome on [GitHub](https://github.com/ledokter/obsidian-BlackPe4rl-theme). This theme is a living digital artifact.

## 📜 License
MIT License.

---
*Forged by [ledokter](https://github.com/ledokter).*
