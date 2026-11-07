# Claude guidance for V0id-OS

## Project
V0id-OS is an operating system project. The repository may be incomplete; inspect the existing files and build instructions before making changes.

## Working rules
- Preserve the existing architecture and conventions. Do not invent an OS language, target architecture, build system, package format, or boot process when the repository does not specify one; ask for clarification when it affects the implementation.
- Keep documentation accurate and update it when build, installation, or update behavior changes.
- Never commit credentials, signing keys, tokens, private keys, or other secrets. Use GitHub Actions secrets only when a documented workflow actually requires them.
- Do not claim that updates install automatically on devices unless an OS-side updater is implemented and tested.
- Treat OS update artifacts as security-sensitive. Do not bypass signature or integrity checks; document the verification design before implementing automatic installation.

## GitHub releases
The repository's release workflow runs when a version tag matching `v*` is pushed. It publishes files already built and placed under `dist/` as GitHub Release assets. It does not build the OS. Before changing this process, document the build command, supported target(s), artifact names, and release procedure in the repository.
