# Contributing to BrazilianEngines

## Welcome!

Thank you for your interest in contributing to the BrazilianEngines mod! Whether you're reporting bugs, suggesting features, or submitting code, your contribution is valued.

## How to Contribute

### 1. Reporting Issues

Found a bug or have a suggestion? Please open an issue on GitHub with:

- **Title:** Clear, concise description
- **Description:** Detailed explanation of the issue
- **Steps to Reproduce:** How to replicate the bug
- **Expected Behavior:** What should happen
- **Actual Behavior:** What actually happens
- **Environment:** KSP version, mods installed, OS
- **Screenshots/Logs:** Include if applicable

### 2. Submitting Pull Requests

#### Before You Start
1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Ensure you're up to date with main

#### During Development

**Code Style:**
- Follow existing code conventions
- Use meaningful variable names
- Add comments for complex logic
- Keep lines under 100 characters

**Configuration Files (.cfg):**
```cfg
// Use this format for comments
@PART[BRA-S20]:FOR[xxxRP0]
{
    %TechRequired = solids1956
    %cost = 45
    %entryCost = 2000
    // Clear descriptions
}
```

**Localization:**
- Update BOTH `en-us.cfg` AND `pt-br.cfg`
- Use consistent naming: `#autoLOC_BEng_<ENGINE>_<TYPE>`
- Test that strings display correctly

#### Before Submitting

1. **Test your changes:**
   - Test in a clean KSP installation
   - Test with RP-1, RealFuels, Realism Overhaul
   - Test with Waterfall enabled and disabled
   - Verify no duplicate entries

2. **Update documentation:**
   - Update CHANGELOG.md
   - Update README.md if needed
   - Update DIRECTORY_STRUCTURE.md if structure changes

3. **Commit message format:**
   ```
   type(scope): subject
   
   - Bullet point 1
   - Bullet point 2
   - Bullet point 3
   ```
   
   **Types:** `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`
   
   **Examples:**
   - `feat(engines): add L5 liquid engine configuration`
   - `fix(localization): correct pt-br descriptions`
   - `docs(readme): update installation instructions`

4. **Push and create Pull Request:**
   - Use descriptive title
   - Reference related issues (#123)
   - Explain what changes and why
   - Include testing notes

### 3. Contributing 3D Models

If you're creating 3D models:

1. **File Format:** `.mu` (KSP model format)
2. **Textures:** `.dds` format, 1024x1024 or 2048x2048
3. **Naming:** Follow existing convention
4. **Organization:**
   ```
   Models/<SERIES>/<ENGINE_ID>/
   ├── model.mu
   └── texture.dds
   ```
5. **Documentation:** Include notes on:
   - Source materials/inspiration
   - Real-world references
   - Technical specifications

### 4. Contributing Translations

We welcome additional language support!

1. **New Language:**
   - Create `Localization/xx-xx.cfg` (e.g., `es-es.cfg`)
   - Copy structure from `en-us.cfg`
   - Translate all strings
   - Test in-game

2. **Improving Existing Translation:**
   - Make changes in the .cfg file
   - Test for clarity and accuracy
   - Note cultural context if relevant

### 5. Contributing Documentation

Help us improve our docs:

- **README.md** - Installation, features, overview
- **CHANGELOG.md** - Release history
- **DIRECTORY_STRUCTURE.md** - Organization guide
- **Engine specifications** - Technical details
- **Historical context** - Brazil's space program

## Development Setup

### Prerequisites
- KSP 1.8 or later
- Realism Overhaul
- Real Solar System
- RP-1
- Waterfall (optional but recommended)

### Testing Configuration
```
Create a separate KSP installation for testing
Enable debug logging in KSP settings
Keep console.log for error tracking
```

## Communication

- **Issues:** Use GitHub Issues for tracking
- **Discussions:** Use GitHub Discussions for ideas
- **Quick Questions:** Ask in issue comments

## Code of Conduct

Be respectful and professional:
- Be welcoming to new contributors
- Assume good intent
- Provide constructive feedback
- Focus on ideas, not individuals

## Recognition

All contributors will be recognized in:
- CHANGELOG.md
- README.md contributors section
- GitHub contributors page

## Questions?

Feel free to:
1. Open a Discussion on GitHub
2. Ask in an Issue
3. Contact the maintainers

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

**Thank you for helping make BrazilianEngines better! 🇧🇷🚀**
