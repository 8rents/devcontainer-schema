## Repository Roadmap

> *The roadmap I am going to follow while setting up this repository*

----

## Goals

The goals of this repository are to facilitate the quick creation of new devcontainers from scratch with as much knowledge on each option as possible.

1. Understand as much of the schema and all of the key/value pairs as possible create a schema file for reference.
2. Create a `devcontainer.json` file for setting up Debian with different versions.
3. Create a `devcontainer-template.json` file with some options for Debian.
4. Using the base `devcontainer.json` and `devcontainer-template.json` files update the Debian system and save to an image. 
   `debian-updated.img`
5. Set up a user and add any essential `apt` installs and save to another image.
6. Using the `devcontainer-template.json` file, pull some optional dotfiles to the image from GitHub.
7. Set up a basic nodejs development environment and create another image.
8. Add some NPM installs and save to futher images.
   1. Add typescript support
   2. Linting
   3. LiveReload
9. Redo Puddletown Bootstrap into a devContainer but more modernized

---

## DevContainer Stack

### Debian Stack

Debian will be the base operating system for setting up devcontainers.

Save all versions as .json files and / or .img files.

1. #### `debian`

   Base Debian Image (Latest aka 12)

2. #### `debian-updated`

   `debian` with `apt full-upgrade -y` performed.

3. #### `debian-configured`

   `debian-updated configured without any development environment. With users added, ssh etc… 

4. #### `debian-essentialapps`

   `debian-configured with essential `apt installs` performed.

5. #### `debian-dotfiles`

   `debian-essentialapps with all dotfiles pulled from GitHub.

### Node Stack

Using the .json files, start creating a nodejs development environment.

1. #### `nodejs`

   Based on `debian-dotfiles` but with nodejs installed and synced folders set up for dev and configuration.

   1. #### `typescript`

      Based on `nodejs` but with Typescript Support.

2. #### `frontend-dev`

   Based on `nodejs` and ported from puddetown-bootstrap into a more modernized frontend development enviornment.

### Project Configuration

1. #### `.config` or `.project` folders

   Folders that will hold per project configuration files pertaining to: git, github, editor schemes, vscode, linting and build & deployment processes

​      

