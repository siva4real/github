# Multi-Platform Matrix Build with GitHub Actions

This repository demonstrates a comprehensive GitHub Actions workflow using matrix build strategy for multi-platform CI/CD.

## 🚀 Features

- **Matrix Build Strategy**: Builds across multiple operating systems and Node.js versions
- **Parallel Execution**: All matrix variants run simultaneously for faster builds
- **Artifact Management**: Each build generates and uploads unique artifacts
- **Cross-Platform**: Supports Ubuntu, macOS, and Windows

## 📋 Matrix Configuration

The workflow runs on the following matrix:

| Operating System | Node.js Versions |
| ---------------- | ---------------- |
| Ubuntu Latest    | 16, 18, 20       |
| macOS Latest     | 18, 20           |
| Windows Latest   | 18, 20           |

**Total Matrix Jobs**: 7 parallel builds

## 🔧 Workflow Details

### Triggers

- Push to `main` or `master` branch
- Pull requests to `main` or `master` branch
- Manual workflow dispatch

### Build Artifacts

Each matrix job generates:

- `build-info.txt` - Detailed build information
- `metadata.json` - JSON metadata about the build
- `app.js` - Sample JavaScript output

Artifacts are named: `build-7da31e1-<os>-node<version>`

### Key Steps

1. **Checkout code** - Retrieves repository contents
2. **matrix-7da31e1** - Identifier step for validation
3. **Setup Node.js** - Configures specified Node.js version
4. **Generate artifacts** - Creates build outputs with system info
5. **Upload artifacts** - Uploads to GitHub with 30-day retention

## 📦 Artifacts

After a successful workflow run, you can download artifacts from:

- GitHub Actions UI → Workflow run → Artifacts section
- Each artifact contains complete build information and metadata

## 🎯 Validation

This workflow meets all requirements:

- ✅ At least 3 matrix variants (7 total)
- ✅ Parallel execution of all jobs
- ✅ Unique artifacts with prefix `build-7da31e1-`
- ✅ Step identifier `matrix-7da31e1` included
- ✅ All artifacts contain actual content

## 📧 Contact

**Email**: 24f3004072@ds.study.iitm.ac.in

## 🛠️ Technologies

- GitHub Actions
- Node.js (versions 16, 18, 20)
- Multi-OS support (Ubuntu, macOS, Windows)

## 📝 License

This is a demonstration project for DevOps CI/CD pipeline practices.

---

**Repository**: GitHub Actions Matrix Build Demo  
**Last Updated**: 2025-11-09
