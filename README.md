# fonts

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&amp;logoColor=white)](https://github.com/rolehippie/fonts)
[![General Workflow](https://github.com/rolehippie/fonts/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/fonts/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/fonts/actions/workflows/readme.yml/badge.svg)](https://github.com/rolehippie/fonts/actions/workflows/readme.yml)
[![Galaxy Workflow](https://github.com/rolehippie/fonts/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/fonts/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/fonts)](https://github.com/rolehippie/fonts/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.fonts-blue)](https://galaxy.ansible.com/rolehippie/fonts)

Ansible role to install additional system fonts.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [fonts_extra_archives](#fonts_extra_archives)
  - [fonts_extra_packages](#fonts_extra_packages)
  - [fonts_general_archives](#fonts_general_archives)
  - [fonts_general_packages](#fonts_general_packages)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`


## Default Variables

### fonts_extra_archives

List of extra archives to install

#### Default value

```YAML
fonts_extra_archives: []
```

#### Example usage

```YAML
fonts_extra_archives:
  - name: nerd-font-agave
    url: https://github.com/ryanoasis/nerd-fonts/releases/download/v2.3.3/Agave.zip
    exclude:
      - FILENAME.txt
  - name: nerd-font-arimo
    state: absent
```

### fonts_extra_packages

List of extra packages to install

#### Default value

```YAML
fonts_extra_packages: []
```

### fonts_general_archives

List of general archives to install

#### Default value

```YAML
fonts_general_archives:
  - name: source-code-pro
    url: https://fonts.google.com/download?family=Source%20Code%20Pro
    exclude:
      - README.txt
      - static/*
  - name: source-sans-pro
    url: https://fonts.google.com/download?family=Source%20Sans%20Pro
```

#### Example usage

```YAML
fonts_general_archives:
  - name: nerd-font-agave
    url: https://github.com/ryanoasis/nerd-fonts/releases/download/v2.3.3/Agave.zip
    exclude:
      - FILENAME.txt
  - name: nerd-font-arimo
    state: absent
```

### fonts_general_packages

List of general packages to install

#### Default value

```YAML
fonts_general_packages:
  - fontconfig
  - unzip
  - fonts-firacode
  - fonts-font-awesome
  - fonts-noto
  - fonts-roboto
```

## Discovered Tags

**_fonts_**


## Dependencies

- None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
