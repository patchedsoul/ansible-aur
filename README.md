# ansible-aur

An Ansible module for installing [AUR](https://aur.archlinux.org/) packages. Packages are downloaded with [cower](https://github.com/falconindy/cower) and installed via [makepkg](https://wiki.archlinux.org/index.php/Makepkg).

This assumes your target node already has cower installed.

## Dependencies (Managed Node)

* [Arch Linux](https://www.archlinux.org/) (Obviously)
* [cower](https://github.com/falconindy/cower)

## Installation

1. Clone this repo
2. Copy or link the `aur` file into your global Ansible library (usually `/usr/share/ansible`) or into the `./library` folder alongside your top-level playbook

## Usage

### Options

* `name` - required, name of the AUR package to install
* `dir` - required, name of the directory you want to download AUR packages into
* `user` - required, name of the user you want to install the package as

### Examples

```yaml
# Install package foo
- packer: name=foo dir=/home/someone/aur user=someone

```
