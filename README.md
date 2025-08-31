# direnv ❤️ nRF Connect SDK

When you `cd` into a nRF Connect SDK workspace directory, the correct NCS toolchain environment will be automatically sourced in your shell.

See https://www.hackster.io/cdwilson/automatically-activate-zephyr-build-environments-with-direnv-65af9c for more info.

## Usage

1. Install [direnv](https://direnv.net/) on macOS or Linux.
2. Install NCS toolchains using [nrfutil](https://www.nordicsemi.com/Products/Development-tools/nRF-Util/Download#infotabs), e.g.
   ```
   nrfutil sdk-manager toolchain install --ncs-version v3.1.0
   ```
4. Copy this `.envrc` to the root of your NCS project workspace
5. `cd` into the workspace dir (the first time, you'll need to run `direnv allow`)

If everything worked correctly, you should see output like the following:
```
direnv: loading ~/path/to/your/workspace/.envrc
direnv: export +GIT_EXEC_PATH +GIT_TEMPLATE_DIR +ZEPHYR_BASE +ZEPHYR_SDK_INSTALL_DIR +ZEPHYR_TOOLCHAIN_VARIANT ~PATH
```
