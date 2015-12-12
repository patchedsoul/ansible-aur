# ansible-aur

An Ansible module for installing [AUR](https://aur.archlinux.org/) packages.

If [cower](https://github.com/falconindy/cower) is available, it will be used to download packages. Otherwise, cURL will be used. Packages are installed via [makepkg](https://wiki.archlinux.org/index.php/Makepkg).

## Dependencies (Managed Node)

* [Arch Linux](https://www.archlinux.org/) (Obviously)
* [cower](https://github.com/falconindy/cower) (Optional)

## Installation

1. Clone this repo
2. Copy or link the `aur` file into your global Ansible library (usually `/usr/share/ansible`) or into the `./library` folder alongside your top-level playbook

## Usage

### Options

* `name` - required, name of the AUR package to install
* `user` - required, name of the user you want to install the package as
* `dir` - optional, name of the directory you want to download AUR packages into. If this is left blank, the module will try to use `~/aur` for the specified user.

### Examples

```yaml
# Install package foo
- packer: name=foo user=someone

# Install package foo with a specific download directory
- packer: name=foo dir=/opt/packages/aur user=someone

```
