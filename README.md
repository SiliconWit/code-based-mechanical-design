---
title: "Code-Based Mechanical Design - Collaboration Guide"
description: "Contributing guide for Code-Based Mechanical Design course content"
tableOfContents: true
sidebar:
  order: 999
---

# Code-Based Mechanical Design

![Build](https://img.shields.io/badge/build-passing-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)
![Contributors Welcome](https://img.shields.io/badge/contributors-welcome-orange)

**Read this course at:** [https://siliconwit.com/education/code-based-mechanical-design/](https://siliconwit.com/education/code-based-mechanical-design/)

A course on programmatic CAD using CadQuery and Python. Covers parametric hardware libraries from engineering standards, involute gear generation, custom enclosures from PCB data, heat sink thermal optimization, lattice structures for additive manufacturing, spring design with stress verification, and FEA-driven structural optimization. Every lesson produces manufacturable STEP and STL output.

## Lessons

| # | Title |
|---|-------|
| 0 | Code-Based CAD in Action |
| 1 | Parametric Hardware Library |
| 2 | Involute Gear Systems |
| 3 | Custom Enclosure from PCB Data |
| 4 | Heat Sink Design and Thermal Optimization |
| 5 | Lattice Structures and TPMS for Additive Manufacturing |
| 6 | Spring Design and Stress Verification |
| 7 | FEA-Driven Structural Optimization |

## File Structure

```
code-based-mechanical-design/
├── index.mdx
├── code-cad-showcase.mdx
├── parametric-hardware-library-engineering-standards.mdx
├── involute-gear-systems.mdx
├── custom-enclosure-pcb-data.mdx
├── heat-sink-design-thermal-optimization.mdx
├── lattice-structures-tpms-additive-manufacturing.mdx
├── spring-design-stress-verification.mdx
├── fea-driven-structural-optimization.mdx
└── README.md
```

## How to Contribute

All commands below work on Linux, macOS, and Windows (using Git Bash, PowerShell, or Command Prompt with Git installed).

### For Team Members (with push access)

**First time setup (clone the repo once):**

```bash
git clone https://github.com/SiliconWit/code-based-mechanical-design.git
cd code-based-mechanical-design
```

**Every time you start working:**

```bash
git pull origin main
```

Always pull before making changes. This avoids conflicts with other contributors.

**After making your changes:**

```bash
git add .
git commit -m "Brief description of what you changed"
git push origin main
```

**If you get a push error** (someone pushed before you):

```bash
git pull origin main
```

Git will merge the changes automatically in most cases. If there is a conflict, Git will mark the conflicting lines in the file. Open the file, choose which version to keep, then:

```bash
git add .
git commit -m "Resolve merge conflict"
git push origin main
```

**Tips to avoid conflicts:**

- Always `git pull origin main` before you start working
- Push your changes as soon as you are done, do not hold onto uncommitted work for long
- Coordinate with other contributors so two people are not editing the same file at the same time

### For External Contributors (without push access)

1. Fork the repository: [SiliconWit/code-based-mechanical-design](https://github.com/SiliconWit/code-based-mechanical-design)
2. Clone your fork:
   ```bash
   git clone https://github.com/YOUR-USERNAME/code-based-mechanical-design.git
   cd code-based-mechanical-design
   ```
3. Make your changes and commit:
   ```bash
   git add .
   git commit -m "Brief description of what you changed"
   git push origin main
   ```
4. Open a Pull Request against `main` on the original repository
5. Describe what you changed and why in the PR description

## Content Standards

- All lesson files use `.mdx` format
- `<BionicText>` may be used in later content sections but not in lesson intro paragraphs
- Code blocks should include a title attribute:
  ````mdx
  ```python title="gear_generator.py"
  import cadquery as cq
  gear = cq.Workplane("XY").circle(pitch_radius)
  ```
  ````
- Use Starlight components (`<Tabs>`, `<TabItem>`, `<Steps>`, `<Card>`) where appropriate
- Keep paragraphs concise and focused on practical application
- Include working CadQuery/Python examples that readers can run directly
- Mathematical notation uses LaTeX in MDX

## Local Development

Clone the main site repository and initialize submodules:

```bash
git clone --recurse-submodules <main-repo-url>
cd siliconwit-com
npm install
npm run dev
```

To test a production build:

```bash
npm run build
```

## License

This course content is released under the [MIT License](LICENSE).
