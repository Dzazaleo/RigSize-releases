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



## FAQ

### Does it only check the setup pose, or the whole animation?

It checks the setup pose, every animation and every skin. By default it samples
each animation 120 times a second, and you can change that in Preferences. It
runs on the Spine Runtimes, so IK, constraints and physics all count.

### What about meshes that bend or stretch?

RigSize measures those too, but each image gets one scale. If one small area
stretches far more than the rest of the image, that area can come out softer.
When that happens, you can override the size of that image.

### Can I see why an image needs a certain size?

Yes. The Animation Breakdown shows the largest size of each image in each
animation, along with the chain of bones that leads to it.

### Can I change a size myself?

Yes. Double-click a size in the Optimized column and enter a percentage, where
100% is the size shown. An image is never exported bigger than its original.

### Do I need an atlas?

No. Open your skeleton JSON with its atlas, or with a folder of loose images.

### Do I have to change how I pack?

No. RigSize exports a folder of right-sized images and the skeleton JSON. You
then pack them with Spine's Texture Packer or the packer in your engine. Your
source files are never changed.

### How can I tell if the smaller images still look right?

The Animation Viewer compares Original and Optimized with a toggle, a split
slider or side by side. Compare them at 100% zoom, where you see the true
pixels.

### What if several skeletons share the same images?

Open them together as a group project. RigSize sizes each shared image for all
of the skeletons and exports them to one images folder.

