# 🌎 South & Central America Travel Vault

Welcome to your personal travel planning vault! This collection of notes organizes locations across South and Central America, enriched with metadata for easy filtering, mapping, and itinerary planning.

## 📂 Vault Structure

This vault is organized around **Location Notes**. Each note represents a specific destination (city, town, park, or landmark).

### File Naming Convention

Files are named using the format: `({Country}) {Location Name}.md`

_Example:_ `(Argentina) El Calafate.md`

### Note Structure (Frontmatter)

Each note contains YAML frontmatter at the top, which is crucial for the plugins and scripts to work:

```
---
name: "El Calafate"
country: "Argentina"
tags:
  - location
  - Argentina
  - glacier
  - nature
location: [-50.337969, -72.2647981] # [Latitude, Longitude]
color: "#0288d1"
google_maps: "[https://www.google.com/maps?q=](https://www.google.com/maps?q=)..."
---
```

## 🏷️ The Tagging System

Locations are automatically categorized using specific tags to help you find what you are looking for. We limit tags to the **top 2-3 highlights** per location.

**Key Categories:**

- **🏄 Activities:** `surfing`, `diving`, `hiking`, `trekking`, `nightlife`, `shopping`
    
- **🌿 Nature:** `nature`, `beach`, `jungle`, `volcano`, `waterfall`, `glacier`, `desert`
    
- **🏙️ Type:** `city`, `town`, `village`, `history`, `colonial`, `ruins`
    

## 🤖 Automation: Auto-Tagging Script

Included in this vault is a Python script (`tag_locations.py`) that automates the categorization process.

### How it works

1. It reads every `.md` file in the folder.
    
2. It matches the location against a curated dictionary of **16 countries**.
    
3. It inserts relevant tags (e.g., adding `#surfing` to "Bocas del Toro") into the YAML frontmatter.
    
4. If a location is unknown, it scans the text description for keywords.
    

### How to run it

1. Ensure you have **Python** installed.
    
2. Open your terminal/command prompt.
    
3. Run the command:
    
    ```
    python tag_locations.py "path/to/your/obsidian/vault"
    ```
    

## 🗺️ Visualization (Map View Plugin)

This vault is designed to work perfectly with the **Obsidian Map View** plugin.

### Setup

1. Install **Map View** from the Obsidian Community Plugins settings.
    
2. Open the file **`map_view.md`** included in this vault.
    

### Features

The `map_view.md` file contains pre-configured code blocks that generate dynamic maps based on your tags. You can view:

- 🏄 **Surfing Spots** (Filters for `tag:surfing`)
    
- 🥾 **Hiking & Nature** (Filters for `tag:hiking` OR `tag:nature`)
    
- 🏙️ **Cities & Culture** (Filters for `tag:city` OR `history`)
    
- 🤿 **Diving** (Filters for `tag:diving`)
    

## 🌎 Countries Covered

The data includes detailed locations for:

- **South America:** Argentina, Bolivia, Brazil, Chile, Colombia, Ecuador, Peru, Uruguay.
    
- **Central America & Mexico:** Belize, Costa Rica, El Salvador, Guatemala, Honduras, Mexico, Nicaragua, Panama.
