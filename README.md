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
  [latest release](https://github.com/Dzazaleo/RigSize-releases/releases/latest).
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

No. RigSize exports a folder of right-sized images and the skeleton JSON, and
you can still pack them yourself with Spine's Texture Packer or the packer in
your engine. Or tick Pack with Spine in the Export window: RigSize then runs
your own installed copy of Spine to pack the images into a Spine atlas, in the
same export. Pack with Spine is new and still in beta. Your source files are
never changed.

### How can I tell if the smaller images still look right?

The Animation Viewer compares Original and Optimized with a toggle, a split
slider or side by side. Compare them at 100% zoom, where you see the true
pixels.

### Why do soft edges look dark or black after export?

Usually the images are stored with one kind of alpha (premultiplied or
straight) and drawn with the other. Check that the premultiplied alpha setting
in your game engine or viewer matches how the images were exported from Spine.
With an atlas, RigSize reads this from the atlas and keeps it. Without an
atlas, RigSize looks at the pixels and asks you how the images are stored when
it cannot be sure: pick the answer that matches your Spine export. If the
edges still look wrong, please tell us on the
[issues page](https://github.com/Dzazaleo/RigSize-releases/issues).

### What if several skeletons share the same images?

Open them together as a group project. RigSize sizes each shared image for all
of the skeletons and exports them to one images folder.

### Can a group be packed into one atlas?

Yes. With Pack with Spine ticked, a group can pack one atlas for the whole
group, which is the default, or one atlas per skeleton. You choose under
Atlases in the group's Pack settings.

### What do I need for Pack with Spine?

Spine must be installed on the same computer, and activated. RigSize uses the
Spine version each skeleton was exported with. If that version is not
installed, Spine downloads it the first time, so you need the internet then.
To pack a group together, its skeletons must come from the same Spine version
(for example all 4.2).

### Does it run on an Intel Mac?

Not yet. The Mac version runs on Macs with Apple silicon (M1 or newer). On
Windows it needs a 64-bit PC.

Using an Intel Mac and want RigSize on it?
[Tell us here](https://github.com/Dzazaleo/RigSize-releases/issues/new?title=Intel%20Mac%20support).
Each request helps us decide whether to make an Intel version.

## Feedback

Found a problem, or have an idea? Tell us on the
[issues page](https://github.com/Dzazaleo/RigSize-releases/issues). If a rig
packed with Spine looks wrong, please say so there too.

RigSize is free. If it saves you time, a star on this page helps other
animators and developers find it.
