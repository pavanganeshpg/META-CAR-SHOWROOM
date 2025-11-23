# Contributing to META CAR SHOWROOM

First off, thank you for considering contributing to META CAR SHOWROOM! It's people like you that make this project such a great tool.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Enhancements](#suggesting-enhancements)
  - [Your First Code Contribution](#your-first-code-contribution)
  - [Pull Requests](#pull-requests)
- [Style Guidelines](#style-guidelines)
  - [Git Commit Messages](#git-commit-messages)
  - [C# Style Guide](#c-style-guide)
  - [Documentation Style Guide](#documentation-style-guide)
- [Development Setup](#development-setup)
- [Testing](#testing)

## Code of Conduct

This project and everyone participating in it is governed by our commitment to fostering an open and welcoming environment. We pledge to make participation in our project a harassment-free experience for everyone.

### Our Standards

**Examples of behavior that contributes to a positive environment:**
- Using welcoming and inclusive language
- Being respectful of differing viewpoints and experiences
- Gracefully accepting constructive criticism
- Focusing on what is best for the community
- Showing empathy towards other community members

**Examples of unacceptable behavior:**
- The use of sexualized language or imagery
- Trolling, insulting/derogatory comments, and personal or political attacks
- Public or private harassment
- Publishing others' private information without explicit permission
- Other conduct which could reasonably be considered inappropriate

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check the existing issues as you might find out that you don't need to create one. When you are creating a bug report, please include as many details as possible:

**Bug Report Template:**
```markdown
**Describe the bug**
A clear and concise description of what the bug is.

**To Reproduce**
Steps to reproduce the behavior:
1. Go to '...'
2. Click on '....'
3. Scroll down to '....'
4. See error

**Expected behavior**
A clear and concise description of what you expected to happen.

**Screenshots**
If applicable, add screenshots to help explain your problem.

**System Information:**
 - OS: [e.g. Windows 11, macOS 12]
 - Unity Version: [e.g. 2021.3.15f1]
 - HDRP Version: [e.g. 12.1.7]
 - Graphics Card: [e.g. NVIDIA RTX 3070]

**Additional context**
Add any other context about the problem here.
```

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, please include:

**Enhancement Template:**
```markdown
**Is your feature request related to a problem?**
A clear and concise description of what the problem is.

**Describe the solution you'd like**
A clear and concise description of what you want to happen.

**Describe alternatives you've considered**
A clear and concise description of any alternative solutions or features you've considered.

**Additional context**
Add any other context or screenshots about the feature request here.
```

### Your First Code Contribution

Unsure where to begin? You can start by looking through these `beginner` and `help-wanted` issues:

- **Beginner issues** - issues which should only require a few lines of code
- **Help wanted issues** - issues which should be a bit more involved than beginner issues

### Pull Requests

1. **Fork the repository** and create your branch from `main`
2. **Make your changes** following our style guidelines
3. **Test your changes** thoroughly
4. **Update documentation** if needed
5. **Commit your changes** using our commit message conventions
6. **Push to your fork** and submit a pull request

**Pull Request Template:**
```markdown
## Description
Brief description of what this PR does.

## Type of Change
- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] New feature (non-breaking change which adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Documentation update

## How Has This Been Tested?
Describe the tests you ran to verify your changes.

## Checklist
- [ ] My code follows the style guidelines of this project
- [ ] I have performed a self-review of my own code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings
- [ ] I have added tests that prove my fix is effective or that my feature works
- [ ] New and existing unit tests pass locally with my changes

## Screenshots (if applicable)
Add screenshots to help explain your changes.
```

## Style Guidelines

### Git Commit Messages

We follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types:**
- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Changes that don't affect code meaning (formatting, etc.)
- `refactor`: Code change that neither fixes a bug nor adds a feature
- `perf`: Performance improvements
- `test`: Adding or correcting tests
- `chore`: Changes to build process or auxiliary tools

**Examples:**
```
feat(camera): Add zoom functionality to camera controller

- Implement mouse wheel zoom
- Add zoom limits configuration
- Update camera documentation

Closes #123
```

```
fix(rendering): Resolve shadow flickering on car model

The shadow map resolution was too low causing flickering.
Increased resolution from 1024 to 2048.

Fixes #456
```

### C# Style Guide

We follow the [Microsoft C# Coding Conventions](https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions):

**Key Points:**
- Use PascalCase for class names and method names
- Use camelCase for local variables and parameters
- Use `_camelCase` for private fields
- Use meaningful, descriptive names
- Add XML documentation comments to public APIs
- Keep methods small and focused
- Use `var` when the type is obvious

**Example:**
```csharp
/// <summary>
/// Controls the camera movement and rotation around the car.
/// </summary>
public class CameraController : MonoBehaviour
{
    [SerializeField]
    private float _rotationSpeed = 5f;
    
    private Transform _targetTransform;
    
    /// <summary>
    /// Rotates the camera around the target at the specified speed.
    /// </summary>
    /// <param name="delta">The rotation delta in degrees.</param>
    public void RotateCamera(float delta)
    {
        var rotation = Quaternion.Euler(0, delta * _rotationSpeed, 0);
        transform.rotation *= rotation;
    }
}
```

### Documentation Style Guide

- Use Markdown for all documentation
- Keep line length to 80-100 characters when possible
- Use code blocks with language specification
- Include examples where appropriate
- Use clear, concise language
- Avoid jargon unless necessary

## Development Setup

### Prerequisites
```bash
# Install Unity Hub
# Download from: https://unity.com/download

# Install Unity 2021.3 LTS or newer
# Install Git
git --version
```

### Setup Steps

1. **Clone the repository:**
```bash
git clone https://github.com/pavanganeshpg/META-CAR-SHOWROOM.git
cd META-CAR-SHOWROOM
```

2. **Open in Unity:**
   - Launch Unity Hub
   - Click "Add" and select the project folder
   - Open the project

3. **Install required packages:**
   - Open Package Manager (Window → Package Manager)
   - Ensure HDRP is installed
   - Install any missing dependencies

4. **Configure your IDE:**
   - **Visual Studio**: Unity will generate .sln files
   - **Rider**: Install Unity support plugin
   - **VS Code**: Install C# extension

### Project Structure
```
Assets/
├── Scenes/           # Unity scenes
├── Scripts/          # C# scripts
├── Materials/        # HDRP materials
├── Models/           # 3D models
├── Textures/         # Texture assets
└── Prefabs/          # Reusable prefabs
```

## Testing

### Manual Testing
1. Open the MainScene in Unity
2. Press Play to enter Play Mode
3. Test all camera controls
4. Verify rendering quality
5. Check for console errors

### Performance Testing
1. Open the Profiler (Window → Analysis → Profiler)
2. Run the scene in Play Mode
3. Monitor:
   - FPS (should be 60+ on recommended hardware)
   - Memory usage
   - Draw calls
   - Batch count

### Build Testing
1. Build for your target platform
2. Test the standalone build
3. Verify all features work outside the editor
4. Check for missing assets or errors

## Questions?

Feel free to:
- Open a [Discussion](https://github.com/pavanganeshpg/META-CAR-SHOWROOM/discussions)
- Join our community chat (coming soon)
- Contact the maintainers

---

Thank you for contributing to META CAR SHOWROOM! 🚗✨
