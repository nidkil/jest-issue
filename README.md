## Bug Report

The latest version of jest 23.6.0 does not work with node v10.13.0 and npm 6.20 or pnpm 2.18.2. The combination does work with yarn 1.12.3.

It throws the following error

    Requires Babel "^7.0.0-0", but was loaded with "6.26.3".

This happens both in Ubuntu 18.04 and Windows 10.

Related to issues [#6662](https://github.com/facebook/jest/issues/6662) and  [#6913](https://github.com/facebook/jest/issues/6913). I first tried all suggestions in these issue before switching to yarn in despair.

## To Reproduce

Steps to reproduce the behaviour:

1) Install node version v10.13.0
2) Install npm version 6.20 or pnpm 2.18.2
3) Install yarn version 1.12.3
4) Install example repo
5) npm i
6) jest
7) rm -rf node_modules && rm package-lock.json

Repeat steps 5-7 for pnpm and yarn.

## Expected behaviour

Jest should work with npm, pnpm and yarn.

## Link to repl or repo (highly encouraged)

Minimal [repo](https://github.com/nidkil/jest-issue) on GitHub to demonstrate the issue.

## Run `npx envinfo --preset jest`

Paste the results here:

```bash
System:
    OS: Linux 4.4 Ubuntu 18.04.1 LTS (Bionic Beaver)
    CPU: (4) x64 Intel(R) Core(TM) i7-6650U CPU @ 2.20GHz
  Binaries:
    Node: 10.13.0 - ~/.nvm/versions/node/v10.13.0/bin/node
    Yarn: 1.12.3 - ~/.nvm/versions/node/v10.13.0/bin/yarn
    npm: 6.4.1 - ~/.nvm/versions/node/v10.13.0/bin/npm
  npmPackages:
    jest: ^23.6.0 => 23.6.0
```

