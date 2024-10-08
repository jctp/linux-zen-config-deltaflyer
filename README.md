# Introduction

This is a config file for the Arch PKGBUILD source of the [Zen Kernel](https://github.com/zen-kernel/zen-kernel) with configurations intended to improve performance on my Dell 3100 Chromebook, which runs Arch. If you've somehow landed here looking for how to do this, [MrChromebox's](https://docs.mrchromebox.tech/) tools for installing a custom firmware (`coreboot`) will help you wave that warranty goodbye.

To get full-fat Linux on this Chromebook, you'll need two USB 3.0 (important!) sticks, one big enough for the installer, one to install it on to - the 16GB MMC inside won't cut it. SanDisk do a very nice one that sits almost flush.

It's also debatable how long a USB drive will last as /, but I digress - this repo is nothing to do with *installing* Linux, rather tuning it once you're already set up.

This repo is almost entirely for my personal use, but is set to public in case anybody else finds it useful. 

## Why?

Mostly for getting a more solid grip with customising the Linux kernel and building it this way. Plus, it's fun!

The changes from default `linux-zen` build config are minor and routine - see the changelog below. As above, the primary value of this project to me is (mostly) as a learning exercise, both in configuration and the differences between `linux` and `linux-zen`. The secondary value is a better-performing computer.

The config is called "Delta Flyer" after the custom-built hotrod spaceship in Star Trek: Voyager. As anybody will tell you, Linux kernel tweaking is not nerdy in the least and needs a ST reference to help it along.

# Building

Pull and build the latest `linux-zen` as you normally would. I use the Arch build system but this should work with any method. When prompted to configure, load this file. I find `gconfig` makes this easiest.

# Disclaimer

I ACCEPT ABSOLUTELY NO RESPONSIBILITY FOR ANY NEGATIVE CONSEQUENCES OF USING THIS KERNEL CONFIG. **NONE.** As stated above, this repo is for my personal education and getting the most out of this inexpensive (and endlessly charming) piece of hardware, and I give no guarantee to this config's reliability or fitness for any given task. **I am not a kernel professional.** The device I am using this on is not mission-critical and contains only data I can afford to lose. 

# Changelog

## 7th Oct 2024

- Goldmont Plus CPU configuration applied.
- CPU frequency scaling enabled, with all options made available - schedutil is default.
- 32-bit emulation enabled.
- Disabled optimisations specific to AMD CPUs (target device is an Intel Celeron of the above family).
- Security and cryptography settings left as default.

All other settings remain the default for `linux-zen`.
