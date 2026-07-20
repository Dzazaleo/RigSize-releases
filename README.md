<!--
  SOURCE of Dzazaleo/RigSize-releases/README.md (D-10).

  This file is copied VERBATIM to the public releases repo by the `publish`
  job in .github/workflows/release.yml on every release tag. Unlike
  .github/release-template.md (which is rendered through envsubst), this file
  is copied byte-for-byte — it must contain NO envsubst placeholder (no
  dollar-brace variable of any kind), because a placeholder here would ship
  literally to the public repo.

  The source repo's own README.md remains the developer-facing one; this file
  is only the public landing page of the releases repo.
-->

# RigSize

RigSize is a desktop app for macOS and Windows that measures how large each
texture in a skeletal animation rig actually renders. It samples every
animation and skin, finds the peak world-space render scale of every
attachment, and tells you the exact pixel size each image needs — so you can
right-size your textures before packing them, instead of shipping oversized
assets or guessing.

RigSize works with skeleton exports from Spine 4.2 or newer.

- **Download:** grab the latest installer from the
  [Releases page](https://github.com/Dzazaleo/RigSize-releases/releases).
- **Install help:** see [INSTALL.md](INSTALL.md) for per-OS install and
  first-launch instructions.
