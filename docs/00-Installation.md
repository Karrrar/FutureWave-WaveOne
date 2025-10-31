# Development Stack Installation Guide

## Prerequisites

Before starting, ensure you have administrative privileges on your computer to install the necessary software.

## 1. Install Windows terminal

You can install `Windows Terminal` from Microsoft store

## 2. Install Git

To install Git on Windows:

1. Go to the official Git website: https://git-scm.com/install/windows
2. The download should start automatically. If not, click on the download link.
3. Run the downloaded installer.
4. During installation:
   - Leave default settings as they are
   - For "Choosing the default editor", select "Use Visual Studio Code as Git's default editor"
   - For the initial branch name, choose "main"
   - For terminal emulator, choose "Use Windows Terminal"
   - Keep other settings as default

After installation, verify Git is installed by opening Windows Terminal and running:

```sh
git --version
```

### Configure Git User Information

After installing Git, you need to configure your user name and email. Open Windows Terminal and run these commands:

```sh
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

Replace "Your Name" and "your.email@example.com" with your actual name and email address.

### Install GitHub CLI

You can install GitHub CLI in two ways:

#### Option 1: Manual Download

1. Go to https://cli.github.com/
2. Click on the download button for Windows
3. Run the installer
4. Follow the installation prompts

#### Option 2: Using winget

```sh
winget install --id GitHub.cli
```

2. Verify the installation:

```sh
gh --version
```

3. Authenticate with GitHub:

```sh
gh auth login
```

Follow the interactive prompts:

- Select "GitHub.com"
- Select "HTTPS"
- Select "Yes" to authenticate with your GitHub credentials
- Choose your preferred way to authenticate (browser or toke)

## 3. Install Visual Studio Code (VS Code)

You can install VS Code on Windows by following these steps:

1. Go to the official Visual Studio Code website: https://code.visualstudio.com/
2. Click on the "Download for Windows" button.
3. Run the downloaded installer and follow the setup instructions.

Alternatively, you can use the Windows Package Manager (winget) from the command prompt:

```sh
winget install --id Microsoft.VisualStudioCode

```

## 3. Installing Node.js and Yarn

### Install NVM (Recommended)

Do not install Node.js if you installed NVM

1. Go to the official NVM repository: [https://github.com/coreybutler/nvm-windows](https://github.com/coreybutler/nvm-windows).
2. Download the LTS (Long Term Support) version for your operating system.
3. Run the installer and follow the on-screen instructions.
4. Run `nvm install 23.1.0`
5. Run `nvm use 23.1.0`

### Install Node.js

1. Go to the official Node.js website: [https://nodejs.org](https://nodejs.org).
2. Download the LTS (Long Term Support) version for your operating system.
3. Run the installer and follow the on-screen instructions.

### Verify Node.js Installation

Open your terminal or command prompt and type:

```console
    node -v
```

This should display the installed Node.js version.

### Install Yarn

#### using corepace

1. Open your terminal or command prompt.
2. Run `corepack enable`
   - if corepack not installed run `npm install -g corepack` and re-run ` corepack enable`

#### using npm

1. Open your terminal or command prompt.
2. Run the following command to install Yarn globally:

```console
   npm install -g yarn
```

### Verify Yarn Installation

Type the following command:

```console
    yarn -v
```

This should display the installed Yarn version.
