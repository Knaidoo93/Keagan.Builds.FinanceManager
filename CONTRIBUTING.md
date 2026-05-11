# Contributing to keagan.builds — Finance Manager

Thanks for your interest in contributing! Contributions of all sizes are welcome.

## Ways to Contribute

### 🐛 Bug Reports & Suggestions
Open a GitHub Issue with:
- What you expected Claude to do
- What it actually did
- The conversation context (if helpful)

### 📝 Improving CLAUDE.md
The core `CLAUDE.md` file is the heart of this project. Good PRs:
- Fix ambiguous instructions that cause Claude to behave unexpectedly
- Add missing edge cases or interaction patterns
- Improve the tone or clarity of a section
- Add new quick commands with clear, tested behaviors

### 🗃️ Notion Template
Help improve or build a shareable Notion template:
- Improve formulas in the spec
- Create and publish an actual Notion template and share the duplicate link
- Add screenshots to the README

### 🌍 Translations / Localizations
Create a localized version of `CLAUDE.md` for other languages or regional contexts. Place them in a `/locales` folder:
```
/locales/CLAUDE.fr.md
/locales/CLAUDE.de.md
/locales/CLAUDE.es.md
```

### 🔀 Budget Framework Variants
Create alternative versions for different budget frameworks:
```
/variants/CLAUDE.50-30-20.md
/variants/CLAUDE.zero-based.md
/variants/CLAUDE.envelope-method.md
```

## Pull Request Guidelines

1. **Keep PRs focused** — one change per PR makes review much easier
2. **Test your changes** — paste the updated CLAUDE.md into a Claude Project and verify behavior
3. **Update the README** if you're adding a feature users need to know about
4. **Be kind** — constructive, respectful feedback only

## Project Structure

```
Keagan.Builds.FinanceManager/
├── CLAUDE.md                    # Core system prompt (main file)
├── README.md                    # GitHub readme
├── CONTRIBUTING.md              # This file
├── NOTION-TEMPLATE-SPEC.md      # Notion database structure
├── LICENSE                      # MIT
├── /variants                    # Alternative budget frameworks
│   └── CLAUDE.50-30-20.md
└── /locales                     # Translations
```

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

*[keagan.builds](https://github.com/Keagan) · MIT License*
