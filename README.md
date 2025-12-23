# NYA Core Assets

Official plugins and language files for **NYA Core** (formerly HitTracker) - A no-hit run tracker for Souls games.

## 📁 Repository Structure

```
NYA-Core-Assets/
├── plugins/          # Game plugins (detection and autosplitter logic)
│   ├── ac6/         # Armored Core VI
│   ├── bb/          # Bloodborne
│   ├── des/         # Demon's Souls
│   ├── ds1/         # Dark Souls
│   ├── ds2/         # Dark Souls II
│   ├── ds3/         # Dark Souls III
│   ├── eldenring/   # Elden Ring
│   └── sekiro/      # Sekiro: Shadows Die Twice
└── languages/        # Localization files
    ├── ca.json      # Catalan
    ├── es.json      # Spanish
    ├── gl.json      # Galician
    └── lolcat.json  # LOLcat (meme language)
```

## 🎮 Plugins

Each plugin folder contains a `plugin.toml` file that defines:
- Game detection patterns (process names, window titles)
- Boss/split definitions
- Auto-splitter logic (memory addresses for hit detection)
- Game-specific configuration

### Supported Games

| Game | Plugin Folder | Status |
|------|---------------|--------|
| Armored Core VI | `ac6/` | ✅ Active |
| Bloodborne | `bb/` | ✅ Active |
| Demon's Souls | `des/` | ✅ Active |
| Dark Souls | `ds1/` | ✅ Active |
| Dark Souls II | `ds2/` | ✅ Active |
| Dark Souls III | `ds3/` | ✅ Active |
| Elden Ring | `eldenring/` | ✅ Active |
| Sekiro | `sekiro/` | ✅ Active |

## 🌍 Languages

NYA Core supports multiple languages. Translation files use JSON format with a simple key-value structure.

### Available Languages

- **Catalan** (`ca.json`)
- **Spanish** (`es.json`)
- **Galician** (`gl.json`)
- **LOLcat** (`lolcat.json`) - For fun! 😺

English is the default language and is built into the application.

## 🤝 Contributing

### Adding a New Plugin

1. Create a new folder in `plugins/` with your game's short name
2. Add a `plugin.toml` file following the existing format
3. Define boss names, memory addresses, and detection logic
4. Test thoroughly before submitting a PR

See existing plugins for reference on the TOML structure.

### Adding/Updating Translations

1. Edit the appropriate language file in `languages/`
2. Follow the existing key structure
3. Ensure all keys are translated (no missing translations)
4. Use proper grammar and context for the target language
5. Submit a PR with your changes

**Translation Keys**: Each key follows the format `section.key` (e.g., `obs.splitsBgImage`, `settings.language`)

## 📥 Using These Assets

### For Users

NYA Core automatically includes these assets in the installation. You don't need to download them separately.

### For Developers

Clone this repository to:
- Develop custom plugins
- Add new language translations
- Reference the plugin API structure
- Contribute improvements

```bash
git clone https://github.com/valkyaha/NYA-Core-Assets.git
```

## 🔄 Update Process

This repository is automatically synced with official NYA Core releases. When a new version is released:

1. Plugin updates are tested and merged
2. Language files are updated with new keys
3. Changes are tagged with version numbers
4. NYA Core can fetch updates from this repo

## 📜 License

These assets are part of NYA Core and follow the same license as the main application.

## 🔗 Related Links

- [NYA Core Releases](https://github.com/valkyaha/HitTracker-Release)
- [Documentation Wiki](https://github.com/valkyaha/HitTracker-Release/wiki)
- [Report Issues](https://github.com/valkyaha/HitTracker-Release/issues)

## 📋 Version

Current assets version: **v2.1.0**

Compatible with NYA Core v2.0.0 and later.

---

**Note**: This repository contains community-contributed plugins and translations. While we strive for accuracy, always test plugins thoroughly before using them in important runs.
