# @pnpm/self-installer

> Installs pnpm

<!--@shields('npm', 'travis')-->
[![npm version](https://img.shields.io/npm/v/@pnpm/self-installer.svg)](https://www.npmjs.com/package/@pnpm/self-installer) [![Build Status](https://img.shields.io/travis/pnpm/self-installer/master.svg)](https://travis-ci.org/pnpm/self-installer)
<!--/@-->

## Usage

Use [unpkg](https://unpkg.com/) to access the installation script and set up pnpm:

    curl -L https://unpkg.com/@pnpm/self-installer | node

## Configuring

The above script will install the latest version of pnpm but you may also install
a specific version by specifying the `PNPM_VERSION` environment variable:

    curl -L https://unpkg.com/@pnpm/self-installer | PNPM_VERSION=1.16.2 node

Here are all the supported environment variables that can influence pnpm's installation:

| Env variable      | Type                  | Description                                                                              | Example                                           |
| ----------------- | --------------------- | ---------------------------------------------------------------------------------------- | ------------------------------------------------- |
| **PNPM_VERSION**  | _version, range, tag_ | `latest` by default. The pnpm version to be installed.<br>(not older than `pnpm@1.16.2`) | `PNPM_VERSION=next`                               |
| **PNPM_DEST**     | _Path_                | The directory into which pnpm's files will be downloaded.                                | `PNPM_DEST=node_modules/pnpm`                     |
| **PNPM_BIN_DEST** | _Path_                | `process.execPath` by default. The directory into which pnpm's bins will be linked.      | `PNPM_BIN_DEST=node_modules/.bin`                 |
| **PNPM_REGISTRY** | _URL_                 | `https://registry.npmjs.org/` by default. The registry to be used for downloading pnpm.  | `PNPM_REGISTRY=https://registry.node-modules.io/` |

## License

[MIT](./LICENSE) © [Zoltan Kochan](https://www.kochan.io/)
