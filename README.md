# V0id-OS

An OS I'm making currently.

## Repository workflow

Claude project guidance is in [`CLAUDE.md`](CLAUDE.md). GitHub Actions publishes versioned GitHub Releases when a version tag such as `v0.1.0` is pushed. Release files must be placed under `dist/` before the tag is pushed.

### Publish an update

1. Build the OS using the documented build process and put the distributable installer/image/package files in `dist/`.
2. Commit the source and build instructions.
3. Create and push a version tag, for example:
   ```sh
   git tag v0.1.0
   git push origin v0.1.0
   ```
4. Check the **Actions** tab and then the published release under **Releases**.

The workflow creates a GitHub Release and attaches every file in `dist/`. It does not build the OS or install updates on devices. An updater in V0id-OS must be implemented to check GitHub Releases and safely install compatible release assets. Document the required OS format, architectures, and update/install behavior before adding that updater.
