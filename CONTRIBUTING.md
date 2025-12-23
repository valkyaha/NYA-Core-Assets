# Contributing to NYA Core Assets

Thank you for your interest in contributing to NYA Core! This document provides guidelines for contributing plugins and translations.

## 🎮 Contributing a Plugin

### Plugin Structure

Each plugin must have the following structure:

```
plugins/
└── yourgame/
    └── plugin.toml
```

### Plugin TOML Format

```toml
# Game identification
name = "Your Game Name"
short_name = "YG"
process_name = "yourgame.exe"  # Windows process name
window_title_pattern = "Your Game"  # Part of the window title

# Boss/Split definitions
[[boss]]
name = "First Boss"
icon = ""  # Optional icon character

[[boss]]
name = "Second Boss"
icon = ""

# Memory patterns for hit detection (optional)
[memory]
base_address = "0x12345678"
offset = "0x100"
hit_flag = "0x1"
```

### Testing Your Plugin

1. Place your plugin folder in NYA Core's `plugins/` directory
2. Launch NYA Core and your game
3. Verify the game is detected
4. Test boss splitting functionality
5. Test hit detection if implemented

### Submitting Your Plugin

1. Fork this repository
2. Create a new branch: `git checkout -b plugin/yourgame`
3. Add your plugin folder to `plugins/`
4. Test thoroughly
5. Commit with a clear message: `Add plugin for Your Game Name`
6. Submit a Pull Request with:
   - Game name and version tested
   - What works (detection, splits, hit detection)
   - Any known issues or limitations

## 🌍 Contributing Translations

### Translation Guidelines

1. **Completeness**: Translate all keys, don't leave any in English
2. **Context**: Consider the UI context when translating
3. **Consistency**: Use consistent terminology throughout
4. **Natural Language**: Prefer natural phrasing over literal translation
5. **Technical Terms**: Keep technical terms recognizable (e.g., "OBS", "API")

### Translation File Format

JSON structure with nested objects:

```json
{
    "app": {
        "title": "Your Translation"
    },
    "settings": {
        "language": "Idioma"
    }
}
```

### Key Sections

- `app.*` - Application-wide strings
- `settings.*` - Settings page
- `obs.*` - OBS integration customization
- `games.*` - Game-related strings
- `common.*` - Common UI elements (buttons, labels)
- `messages.*` - User-facing messages

### Adding a New Language

1. Copy an existing language file (e.g., `es.json`)
2. Rename it with the appropriate language code (ISO 639-1)
3. Translate all keys
4. Test in the application
5. Submit a PR

### Updating Existing Translations

1. Check the English UI for the latest strings
2. Update the JSON file with new or changed translations
3. Verify no keys are missing
4. Submit a PR with a clear description of changes

## 📝 Pull Request Process

1. **Fork & Branch**: Fork the repo and create a feature branch
2. **Make Changes**: Add your plugin or update translations
3. **Test**: Verify your changes work correctly
4. **Commit**: Use clear, descriptive commit messages
5. **PR Description**: Explain what you're adding/changing and why
6. **Review**: Address any feedback from maintainers

### PR Title Format

- Plugins: `Add plugin for [Game Name]` or `Update [Game Name] plugin`
- Translations: `Add [Language] translation` or `Update [Language] translation`
- Fixes: `Fix [issue] in [plugin/language]`

## ✅ Quality Standards

### Plugins

- ✅ Must include all required fields in `plugin.toml`
- ✅ Game name and process name must be accurate
- ✅ Boss names should match in-game names
- ✅ Memory addresses (if provided) must be tested and working
- ✅ Should include a brief comment explaining any complex logic

### Translations

- ✅ All keys must be present (no missing translations)
- ✅ Proper grammar and spelling in target language
- ✅ Consistent terminology throughout
- ✅ Natural phrasing (not overly literal)
- ✅ Special characters properly escaped in JSON

## 🐛 Reporting Issues

Found a bug in a plugin or translation? Please report it:

1. Check if the issue already exists
2. Open an issue in [HitTracker-Release](https://github.com/valkyaha/HitTracker-Release/issues)
3. Include:
   - NYA Core version
   - Affected plugin/language
   - Steps to reproduce
   - Expected vs actual behavior

## 💬 Questions?

- Open a discussion in the main [NYA Core repository](https://github.com/valkyaha/HitTracker-Release/discussions)
- Check the [Wiki](https://github.com/valkyaha/HitTracker-Release/wiki) for documentation

## 📜 Code of Conduct

Be respectful and constructive. We're all here to make NYA Core better for the community!

---

Thank you for contributing! 🎮✨
