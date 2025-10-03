# Blank devcontainer template

> *A blank template with as many of the key / value pairs outlined and commented as possible.*

---

## Developing these templates

1. Read through the [Properties list](https://containers.dev/implementors/json_reference/) and implement each of these.
2. Go through the [Base Schema](https://containers.dev/implementors/json_schema/) and add values into the json file.
3. 

## Goals

1. Have all of the properties listed in the templates.
2. Have the properties nested correctly
3. Have the properties listed in the order of most used / essential.
4. Give an explanation of each property key as a comment
5. Have some property values as comments
6. Make sure the file runs with 0, 1, 2 and more properties

## Devcontainer template Roadmap

The goal will be to build one devcontainer template out of a previously completed devcontainer template.

They will be developed in branches in the following order.

### OS

- **Base Template**
  *The base blank template.*

  - Debian `debian.img`
    *An install of the latest version of Debian (headless)*

    - **Full Upgrade** `debian-fu.img`
      *With `apt full-upgrade -y` completed.*

      - Basic Configuration `debian-conf.img`

        *Have a user created, work area set up, git SSH access.*

        - **DotFiles** `debian-df.img`
          *With all of my CLI settings loaded in and installed (zsh, git, wget)* 
    
      

  - Alpine

    - *… and so on…*

---

### Platforms

*After OS versions as listed above:*

Starting from the `debian-df.img`

- **nodejs** `nodejs.img`
  *the latest version of node installed in the latest version of Debian*

  - **typescript** `nodejs-ts.img`
    node with typescript support configured and turnkey

    - **express** `express-ts.img`

      *Express configured with typescript support turnkey*

## How to use

Use the `devcontainer.json` file as a starting point for creating new devcontainers from scratch. 

### The `devcaontainer-template.json` File

Eventually I will have many values populated in this file so that when opening the `devcontainer.json` in smarter programs it will allow you to select items from this template file.

