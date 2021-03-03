# Mac Setup for Learning Coding

เตรียม แมคบุ๊ค ให้พร้อม สำหรับ เรียนเขียนโปรแกรม

- [Mac Setup for Learning Coding](#mac-setup-for-learning-coding)
  - [Install Xcode](#install-xcode)
  - [Customize Terminal Theme](#customize-terminal-theme)
  - [Install Homebrew](#install-homebrew)
  - [Install Starship Cross-Shell Prompt](#install-starship-cross-shell-prompt)
  - [Install VSCode](#install-vscode)
  - [Install Git](#install-git)
    - [Use macOS.gitignore in .gitignore_global](#use-macosgitignore-in-gitignore_global)
  - [Install Node.js via nvm](#install-nodejs-via-nvm)

## Install Xcode

Open the Terminal and run this command.

```shell
xcode-select --install
```

## Customize Terminal Theme

[Use Terminal theme](https://github.com/lysyi3m/macos-terminal-themes)

## Install Homebrew

[Install Homebrew](https://brew.sh)

## Install Starship Cross-Shell Prompt

1.  [Download Fira Code Nerd Font](https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/FiraCode.zip)
    and install it.
2.  Install [Starship](https://starship.rs) via Homebrew.

```shell
brew install starship
```

## Install VSCode

1. [Install VSCode Insider](https://code.visualstudio.com/insiders)
2. After open the app, press **cmd + shift + P** and type shell and select
   **"Install 'code-insider' command in PATH"** to install the shell command.
3. Create the **'code' alias** in the **~/.zshrc** file.

```shell
# Aliases
alias code='code-insiders'
```

## Install Git

1. Install Git via Homebrew.

```shell
brew install git
```

2. Config Git user and email.

   1. Sign up for a free GitHub account at [GitHub.com](https://github.com).

   2. Go to https://github.com/settings/emails

   3. Check **'Keep my email addresses private'** and **'Block command line
      pushes that expose my email.'**

   4. And copy the **GitHub private email** to clipboard.

   5. Config **GitHub user** and **email** globally via the Terminal.

```shell
git config --global user.name "your-github-username"

git config --global user.email "your-github-private-email"
```

### Use macOS.gitignore in .gitignore_global

```shell
# Create ~/.gitignore_global
code ~/.gitignore_global
```

Copy and Paste the content from
[macOS.gitignore](https://github.com/github/gitignore/blob/master/Global/macOS.gitignore)
to it and save the file.

```shell
# Use ~/.gitignore_global as .gitignore for the global context
git config --global core.excludesfile ~/.gitignore_global
```

## Install Node.js via nvm

1. [Install nvm](https://github.com/nvm-sh/nvm#installing-and-updating)
2. Install Node.js

```shell
nvm install node
```

On M1 Mac, if there is any error after 'nvm install node', press **cmd + C** to
exit then

```shell
# Use Terminal in x64 mode
arch -x86_64 zsh

nvm install node
```
