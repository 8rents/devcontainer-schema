# Using the devcontainer cli tool with fnm on windows limited machines

> *The goal of this guide is to use the devcontainer command line tool to create devcontainers to develop with GitHub codespaces. It will work on a windows limited account using the lastest version of node installed with fast node manager through scoop in powershell.*

---

***Sadly this guide is not going to work because docker can not run in limited accounts. I will need to configure devcontainers in GitHub codespaces with `devcontainer.json` files***

---

## Prerequisites


Have scoop installed and `fnm` installed through scoop

### Install Scoop package manager

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression
```

### Install fast node manager

```powershell
scoop install git fnm
```

### Set up `fnm`

Once fast node manager is installed to set it up in PowerShell run:

> *Alternatively you can add the following to your PowerShell profile*

```powershell
fnm env --use-on-cd --shell powershell | Out-String | Invoke-Expression
```

## Install the latest version of NodeJS through `fnm`

> *`i` is an alias for `install`*

```powershell
fnm i --latest
```

## Using devcontainer cli tool

### Installing

```powershell
npm install -g @devcontainers/cli
```

### Showing help text

Once the command line tool is installed, to show the help page simply run:

```powershell
devcontainer
```

## Quick example: Try out the rust language

To try the rust sample project: https://github.com/microsoft/vscode-remote-try-rust

in your projects folder firsts clone the try rust repo

```powershell
git clone https://github.com/microsoft/vscode-remote-try-rust
```

then run the devcontainer cli on it:

```powershell
devcontainer up --workspace-folder vscode-remote-try-rust
```

