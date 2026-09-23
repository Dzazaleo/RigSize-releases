<!--
  Source of the README.md on the public Dzazaleo/RigSize-releases repository.

  The release workflow (.github/workflows/release.yml) copies this file
  byte-for-byte to the releases repository on every release tag. It is NOT run
  through envsubst, so it must contain no dollar-brace placeholder: one would
  appear literally on the public page.

  Everything below this comment is public text: plain language, no internal
  project identifiers, no em dashes.
-->

# RigSize

RigSize is a free desktop app for macOS and Windows that tells you how big each
image in your Spine animation really needs to be.

It plays through every animation and every skin in your skeleton, finds the
largest size each image is ever drawn on screen, and gives you the exact pixel
size to export. That way you can shrink oversized textures before packing
them, instead of guessing or shipping images that are bigger than they need to
be.

RigSize works with skeleton exports from Spine 4.2 or newer. You need your own
Spine licence from Esoteric Software.

- **Download:** get the latest installer from the
  [Releases page](https://github.com/Dzazaleo/RigSize-releases/releases).
- **Install help:** [INSTALL.md](INSTALL.md) explains how to install RigSize
  and open it for the first time on macOS and Windows.
- **Licence:** RigSize is free to use, including for commercial work. See
  [LICENSE](LICENSE) for the full terms.
