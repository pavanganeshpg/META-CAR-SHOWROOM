<div align="center">

# 🚗 META CAR SHOWROOM

### *Immersive 3D Automotive Visualization Platform*

[![Unity Version](https://img.shields.io/badge/Unity-2021.3%20LTS+-blueviolet.svg?style=flat&logo=unity)](https://unity.com/)
[![HDRP](https://img.shields.io/badge/Render%20Pipeline-HDRP-blue.svg?style=flat)](https://unity.com/srp/High-Definition-Render-Pipeline)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS-lightgrey.svg?style=flat)](https://github.com/pavanganeshpg/META-CAR-SHOWROOM)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=flat)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat)](http://makeapullrequest.com)

[Features](#-features) • [Quick Start](#-quick-start) • [Documentation](#-documentation) • [System Requirements](#-system-requirements) • [Contributing](#-contributing)

---

![META CAR SHOWROOM Banner](https://via.placeholder.com/1200x400/1a1a2e/eee?text=META+CAR+SHOWROOM)

</div>

---

## �� Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [System Requirements](#-system-requirements)
- [Quick Start](#-quick-start)
  - [For End Users (Pre-built Application)](#for-end-users-pre-built-application)
  - [For Developers (Unity Project)](#for-developers-unity-project)
- [Project Architecture](#-project-architecture)
- [Technical Stack](#-technical-stack)
- [Build Instructions](#-build-instructions)
- [Configuration](#-configuration)
- [Performance Optimization](#-performance-optimization)
- [Troubleshooting](#-troubleshooting)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [Team](#-team)
- [License](#-license)
- [Acknowledgments](#-acknowledgments)

---

## 🎯 Overview

**META CAR SHOWROOM** is a cutting-edge, photorealistic 3D automotive visualization application built with Unity's High Definition Render Pipeline (HDRP). This repository contains the **pre-built executable** for Windows, ready to download and run.

> [!IMPORTANT]
> **This repository contains a compiled executable, not Unity project source files.**  
> You cannot open this in Unity Editor. If you need the Unity source project to modify or rebuild, please contact the repository owner.

### 🎨 What Makes It Special?

- **Photorealistic Rendering**: Built with Unity HDRP's advanced lighting and material systems
- **Real-time Ray Tracing**: Dynamic reflections, global illumination, and ambient occlusion
- **Cinematic Camera System**: Smooth camera controls powered by Cinemachine
- **Ready to Run**: Pre-built executable, no Unity installation required
- **Windows Compatible**: Optimized for Windows 10/11 (64-bit)

---

## ✨ Key Features

### 🎬 Visual Excellence
- **Physically-Based Rendering (PBR)**: Authentic material representation with metallic, roughness, and normal maps
- **HDRP Post-Processing Stack**: Bloom, color grading, depth of field, motion blur, and vignette effects
- **Dynamic Lighting System**: Real-time shadows, volumetric lighting, and HDRI skybox integration
- **High-Fidelity Car Model**: Detailed 3D asset with accurate geometry and textures

### 🎮 Interactive Experience
- **Intuitive Camera Controls**: Orbit, pan, zoom, and focus on specific car details
- **Smooth Animations**: Fluid transitions and camera movements using Cinemachine
- **Responsive UI**: Clean, modern interface for seamless user interaction
- **Performance Monitoring**: Built-in FPS counter and performance metrics

### 🛠️ Developer-Friendly
- **Modular Architecture**: Clean code structure for easy customization
- **Extensible Framework**: Add new cars, environments, or features effortlessly
- **Well-Documented**: Comprehensive inline comments and external documentation
- **Version Control Ready**: Optimized `.gitignore` for Unity projects

---

## 💻 System Requirements

### Minimum Requirements
| Component | Specification |
|-----------|---------------|
| **OS** | Windows 10 (64-bit) / macOS 10.15+ |
| **Processor** | Intel Core i5-7500 / AMD Ryzen 5 1600 |
| **Memory** | 8 GB RAM |
| **Graphics** | NVIDIA GTX 1060 6GB / AMD RX 580 8GB |
| **DirectX** | Version 12 (Windows) |
| **Storage** | 500 MB available space |

### Recommended Requirements
| Component | Specification |
|-----------|---------------|
| **OS** | Windows 11 (64-bit) / macOS 12+ |
| **Processor** | Intel Core i7-9700K / AMD Ryzen 7 3700X |
| **Memory** | 16 GB RAM |
| **Graphics** | NVIDIA RTX 2070 / AMD RX 6700 XT |
| **DirectX** | Version 12 (Windows) |
| **Storage** | 1 GB available space (SSD recommended) |

### For Development
- **Unity Editor**: 2021.3 LTS or newer
- **HDRP Package**: Version 12.x or compatible
- **Visual Studio** / **Rider**: For C# scripting (optional)
- **Git**: For version control

---

## 🚀 Quick Start

### Download and Run (Windows)

#### Option 1: Clone from GitHub
```bash
# Clone the repository
git clone https://github.com/pavanganeshpg/META-CAR-SHOWROOM.git
cd META-CAR-SHOWROOM

# Run the executable
./HDRP_car.exe
```

#### Option 2: Download Release
1. **Download** the latest release from [Releases](https://github.com/pavanganeshpg/META-CAR-SHOWROOM/releases)
2. **Extract** the ZIP file to your desired location
3. **Run** `HDRP_car.exe`
4. **Enjoy** the immersive car showroom experience!

> [!NOTE]
> **For Developers:** This repository does not contain Unity project source files (Assets/, ProjectSettings/, etc.).  
> If you need to modify the project or build from source, please contact [@pavanganeshpg](https://github.com/pavanganeshpg) for access to the Unity project.

---

## 🏗️ Project Architecture

```
META-CAR-SHOWROOM/
│
├── HDRP_car.exe                    # Windows executable
├── HDRP_car_Data/                  # Application data
│   ├── Managed/                    # .NET assemblies
│   │   ├── Assembly-CSharp.dll     # Custom game scripts
│   │   ├── Unity.*.dll             # Unity engine modules
│   │   └── Cinemachine.dll         # Camera system
│   ├── Resources/                  # Embedded resources
│   ├── globalgamemanagers          # Unity scene data
│   ├── level0                      # Main scene binary
│   ├── sharedassets0.assets        # Shared assets (models, textures)
│   └── *.resS                      # Resource files
│
├── MonoBleedingEdge/               # Mono runtime (cross-platform .NET)
│   ├── EmbedRuntime/               # Core Mono libraries
│   └── etc/                        # Mono configuration
│
├── UnityPlayer.dll                 # Unity player runtime
├── UnityCrashHandler64.exe         # Crash reporting
│
├── .gitignore                      # Git ignore rules
└── README.md                       # This file
```

### Key Components

#### 1. **Rendering Pipeline**
- **HDRP (High Definition Render Pipeline)**: Unity's premium rendering solution
- **Post-Processing Stack**: Advanced visual effects
- **Shader Graph**: Custom material shaders

#### 2. **Camera System**
- **Cinemachine**: Professional camera control and animation
- **Virtual Cameras**: Multiple predefined camera angles
- **Smooth Transitions**: Seamless camera blending

#### 3. **Input System**
- **Unity Input System**: Modern, flexible input handling
- **Multi-Platform Support**: Keyboard, mouse, and gamepad

#### 4. **Asset Management**
- **Addressables**: Efficient asset loading and memory management
- **Asset Bundles**: Modular content delivery

---

## 🔧 Technical Stack

| Category | Technology |
|----------|------------|
| **Engine** | Unity 2021.3 LTS+ |
| **Render Pipeline** | High Definition Render Pipeline (HDRP) 12.x |
| **Scripting** | C# (.NET Standard 2.1) |
| **Camera System** | Cinemachine 2.8+ |
| **UI Framework** | Unity UI (uGUI) / TextMeshPro |
| **Input** | Unity Input System 1.4+ |
| **Version Control** | Git / GitHub |
| **Build Platform** | Windows (x64) / macOS (Universal) |

### Unity Packages Used
- `com.unity.render-pipelines.high-definition` - HDRP core
- `com.unity.cinemachine` - Camera management
- `com.unity.inputsystem` - Modern input handling
- `com.unity.textmeshpro` - Advanced text rendering
- `com.unity.timeline` - Cinematic sequencing
- `com.unity.visualeffectgraph` - GPU-accelerated VFX

---

## 🔨 Build Information

### About This Build

This executable was built using:
- **Unity Version**: 2021.3 LTS (or newer)
- **Render Pipeline**: High Definition Render Pipeline (HDRP)
- **Platform**: Windows x64
- **Build Type**: Standalone

### Rebuilding from Source

> [!WARNING]
> **Unity project source files are not included in this repository.**

This repository contains only the compiled executable. To rebuild or modify the project, you would need:
1. Unity Editor 2021.3 LTS or newer
2. The original Unity project source files (Assets/, ProjectSettings/, Packages/)
3. HDRP package installed

If you need access to the Unity source project, please open an issue or contact the repository owner.

---

## ⚙️ Configuration

### Graphics Settings

Edit `HDRP_car_Data/boot.config` to adjust graphics:

```ini
gfx-enable-gfx-jobs=1           # Enable graphics job system
gfx-enable-native-gfx-jobs=1    # Enable native graphics jobs
wait-for-native-debugger=0      # Disable debugger wait
hdr-display-enabled=0           # Enable HDR display (if supported)
```

### Performance Tuning

#### Low-End Systems
- Reduce resolution to 1280x720
- Disable post-processing effects
- Lower shadow quality
- Disable ray tracing

#### High-End Systems
- Enable 4K resolution
- Max out post-processing
- Enable ray tracing (RTX GPUs)
- Increase shadow distance

---

## 🚄 Performance Optimization

### Implemented Optimizations
- ✅ **Occlusion Culling**: Hide objects not visible to camera
- ✅ **LOD System**: Level-of-detail for distant objects
- ✅ **Texture Compression**: Reduced memory footprint
- ✅ **Mesh Batching**: Combine draw calls
- ✅ **GPU Instancing**: Efficient rendering of repeated objects
- ✅ **Async Asset Loading**: Non-blocking resource loading

### Profiling Tools
```
Window → Analysis → Profiler  # Unity Profiler
Window → Analysis → Frame Debugger  # Frame-by-frame analysis
```

---

## 🐛 Troubleshooting

### Common Issues

#### Application Won't Launch
**Problem**: Double-clicking the executable does nothing  
**Solution**:
- Ensure all files (`.exe`, `_Data`, `MonoBleedingEdge`, `.dll`) are in the same directory
- Run as Administrator (Windows)
- Check antivirus/firewall settings

#### Low FPS / Performance Issues
**Problem**: Application runs slowly  
**Solution**:
- Update graphics drivers
- Lower resolution in graphics settings
- Close background applications
- Verify system meets minimum requirements

#### Black Screen on Launch
**Problem**: Application launches but shows black screen  
**Solution**:
- Update DirectX (Windows) or Metal drivers (macOS)
- Disable integrated GPU (use dedicated GPU)
- Check `Player.log` for errors:
  - **Windows**: `%APPDATA%\..\LocalLow\DefaultCompany\HDRP_car\Player.log`
  - **macOS**: `~/Library/Logs/DefaultCompany/HDRP_car/Player.log`

#### macOS "Unidentified Developer" Warning
**Problem**: macOS blocks the application  
**Solution**:
1. Right-click the app → **Open**
2. Click **Open** in the security dialog
3. Or: `System Preferences → Security & Privacy → Allow`

---

## 🗺️ Roadmap

### Version 1.1 (Q1 2026)
- [ ] Multiple car models (sedan, SUV, sports car)
- [ ] Customizable car colors and materials
- [ ] Interior camera view
- [ ] VR support (Oculus, SteamVR)

### Version 1.2 (Q2 2026)
- [ ] Multiplayer showroom (networked)
- [ ] Car configurator (wheels, spoilers, etc.)
- [ ] Day/night cycle
- [ ] Weather effects (rain, fog)

### Version 2.0 (Q3 2026)
- [ ] AI-powered car recommendations
- [ ] Integration with dealership APIs
- [ ] Mobile version (iOS/Android)
- [ ] WebGL build for browsers

---

## 🤝 Contributing

We welcome contributions from the community! Here's how you can help:

### Ways to Contribute
- 🐛 **Report Bugs**: Open an issue with detailed reproduction steps
- 💡 **Suggest Features**: Share your ideas in the Discussions tab
- 📝 **Improve Documentation**: Fix typos, add examples, clarify instructions
- 🎨 **Submit Assets**: High-quality car models, environments, or textures
- 💻 **Code Contributions**: Bug fixes, new features, or optimizations

### Contribution Workflow
1. **Fork** the repository
2. **Create** a feature branch
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Commit** your changes
   ```bash
   git commit -m "Add amazing feature"
   ```
4. **Push** to your fork
   ```bash
   git push origin feature/amazing-feature
   ```
5. **Open** a Pull Request with a clear description

### Code Standards
- Follow Unity C# coding conventions
- Add XML documentation comments to public methods
- Write unit tests for new features
- Ensure builds pass before submitting PR

### Community Guidelines
- Be respectful and inclusive
- Provide constructive feedback
- Help others in Discussions and Issues

---

## 👥 Team

This project is maintained by a dedicated team of developers, artists, and designers:

| Role | Contributor |
|------|-------------|
| **Project Lead** | [@pavanganeshpg](https://github.com/pavanganeshpg) |
| **Lead Developer** | [@pavanganeshpg](https://github.com/pavanganeshpg) |
| **3D Artist** | Community Contributors |
| **UI/UX Designer** | Community Contributors |
| **QA Engineer** | Community Contributors |

### Special Thanks
- Unity Technologies for HDRP and Cinemachine
- The open-source community for inspiration and support
- All contributors who have helped improve this project

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 META CAR SHOWROOM Team

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
```

---

## 🙏 Acknowledgments

### Technologies
- [Unity Engine](https://unity.com/) - Game engine and development platform
- [HDRP](https://unity.com/srp/High-Definition-Render-Pipeline) - High-fidelity rendering
- [Cinemachine](https://unity.com/unity/features/editor/art-and-design/cinemachine) - Professional camera system
- [TextMeshPro](https://docs.unity3d.com/Manual/com.unity.textmeshpro.html) - Advanced text rendering

### Resources
- [Unity Documentation](https://docs.unity3d.com/)
- [HDRP Best Practices](https://docs.unity3d.com/Packages/com.unity.render-pipelines.high-definition@latest)
- [Cinemachine Tutorials](https://learn.unity.com/search?k=%5B%22tag%3ACinemachine%22%5D)

### Inspiration
- Real-world automotive showrooms
- AAA game cinematics
- Architectural visualization projects

---

<div align="center">

### 🌟 Star this repository if you find it helpful!

[![GitHub stars](https://img.shields.io/github/stars/pavanganeshpg/META-CAR-SHOWROOM.svg?style=social&label=Star)](https://github.com/pavanganeshpg/META-CAR-SHOWROOM)
[![GitHub forks](https://img.shields.io/github/forks/pavanganeshpg/META-CAR-SHOWROOM.svg?style=social&label=Fork)](https://github.com/pavanganeshpg/META-CAR-SHOWROOM/fork)
[![GitHub watchers](https://img.shields.io/github/watchers/pavanganeshpg/META-CAR-SHOWROOM.svg?style=social&label=Watch)](https://github.com/pavanganeshpg/META-CAR-SHOWROOM)

---

**[Website](https://pavanganeshpg.github.io/META-CAR-SHOWROOM)** • **[Documentation](https://github.com/pavanganeshpg/META-CAR-SHOWROOM/wiki)** • **[Issues](https://github.com/pavanganeshpg/META-CAR-SHOWROOM/issues)** • **[Discussions](https://github.com/pavanganeshpg/META-CAR-SHOWROOM/discussions)**

Made with ❤️ by the META CAR SHOWROOM Team

*Last Updated: November 2025*

</div>
