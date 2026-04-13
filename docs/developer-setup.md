# Developer Setup Guide

## Purpose
This guide helps a new developer get a Windows machine ready to work with The Trio Startup quickly, using the same core tooling baseline already set up for the project.

## Recommended platform
- Windows
- PowerShell 7+
- GitHub account with access to GitHub Copilot

## Quick-start checklist
1. Install Git
2. Install GitHub CLI
3. Install Copilot CLI
4. Install the core development toolchain
5. Authenticate GitHub CLI
6. Authenticate Copilot CLI
7. Clone the team repositories
8. Verify the baseline toolchain

## Core tools

### Git
**Install**

```powershell
winget install Git.Git
```

**Verify**

```powershell
git --version
```

### GitHub CLI
**Install**

```powershell
winget install GitHub.cli
```

**Verify**

```powershell
gh --version
```

**Authenticate**

```powershell
gh auth login
```

Recommended choices during login:
- GitHub.com
- HTTPS
- Authenticate Git with GitHub credentials
- Login with a web browser

### Copilot CLI
GitHub Copilot CLI is used directly from the terminal.

**Requirements**
- Active GitHub Copilot access
- PowerShell 6 or higher on Windows

**Install**

```powershell
winget install GitHub.Copilot
```

**Verify**

```powershell
copilot --version
```

**Launch**

```powershell
copilot
```

If prompted on first launch, use:

```text
/login
```

## Core development baseline
This is the currently validated baseline from the project setup work.

| Tool | Baseline |
| --- | --- |
| GitHub CLI | 2.76.0 |
| Copilot CLI | 1.0.24 |
| Node.js | 24.11.1 |
| Python | 3.11.3 |
| Go | 1.21.4 |
| Java / JDK | 20.0.1 |
| Kotlin | 2.3.20 |
| Gradle | 9.4.1 |

## Development toolchain setup

### Node.js
Install Node.js:

```powershell
winget install OpenJS.NodeJS
```

Verify:

```powershell
node --version
npm --version
```

### Python
Install Python:

```powershell
winget install Python.Python.3.11
```

Verify:

```powershell
python --version
pip --version
```

### Go
Install Go:

```powershell
winget install GoLang.Go
```

Verify:

```powershell
go version
```

### Java / JDK
Install a JDK:

```powershell
winget install EclipseAdoptium.Temurin.20.JDK
```

Verify:

```powershell
java -version
javac -version
```

### Kotlin
Kotlin was installed in our current setup as a user-local compiler package rather than through a standard package manager.

Recommended target:
- Kotlin compiler 2.3.20

After installation, make sure `KOTLIN_HOME` points to the `kotlinc` directory and `KOTLIN_HOME\bin` is on `PATH`.

Verify:

```powershell
kotlinc -version
```

### Gradle
Gradle was installed in our current setup as a user-local tool.

Recommended target:
- Gradle 9.4.1

After installation, make sure `GRADLE_HOME` points to the Gradle install directory and `GRADLE_HOME\bin` is on `PATH`.

Verify:

```powershell
gradle --version
```

## Environment variables
The current machine setup uses these user-level variables:

```text
JAVA_HOME=C:\Program Files\Java\jdk-20
KOTLIN_HOME=<your Kotlin install path>
GRADLE_HOME=<your Gradle install path>
```

Make sure these `bin` directories are available on `PATH`:
- Python
- Python Scripts
- Node.js
- Go
- `%JAVA_HOME%\bin`
- `%KOTLIN_HOME%\bin`
- `%GRADLE_HOME%\bin`

Open a **new terminal** after changing environment variables.

## Verification commands
Run these after setup:

```powershell
gh --version
gh auth status
copilot --version
node --version
npm --version
python --version
pip --version
go version
java -version
kotlinc -version
gradle --version
```

## Copilot CLI workflow tips
- Launch `copilot` inside the repository you are working in.
- Use `/login` if Copilot asks you to authenticate.
- Use `/help` to see available commands.
- Use `/model` if you need to switch models.
- Use `/plan` when you want implementation planning before code changes.

## Suggested first-day onboarding flow
1. Install `gh` and `copilot`
2. Authenticate both tools
3. Install the language/tool baseline
4. Clone `team-mission-and-documentation`
5. Read:
   - `README.md`
   - `docs/mission-and-values.md`
   - `docs/working-agreements.md`
   - `docs/roadmap.md`
   - `docs/repositories.md`
6. Clone the active project repositories you will contribute to

## Notes
- This setup guide is intentionally Windows-first because that is the current team baseline.
- If the team standardizes on exact install scripts later, this document should be updated to point to those scripts instead of manual steps.
