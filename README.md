# Inochi Creator
![Image of Inochi Creator](https://user-images.githubusercontent.com/7032834/194462402-74c4a3e0-50ca-4b50-8e8d-164d97371f5a.png)
_Ada model by [ku-ini](https://twitter.com/duckmastah)_

----------------


Aqua2D Editor is an open source editor for the [Aqua2D puppet format](https://github.com/Mizu545/Aqua2d).  This application allows you to rig models for use in games or for other real-time applications such as [VTubing](https://en.wikipedia.org/wiki/VTuber). Animation is achieved by morphing, transforming and in other ways distorting layered 2D textures in real-time. These distortions can trick the end user in to perciving 3D depth in the 2D art.

If you are a VTuber wanting to use Aqua2D, I highly recommend checking out [Aqua2d Live](https://github.com/Mizu545/Aqua-2d-Live) as well.

&nbsp;

## Downloads

### Stable Builds

None as of now. 

### Experimental Builds

&nbsp;&nbsp;&nbsp;&nbsp;
[![Nightly Builds](https://img.shields.io/github/actions/workflow/status/Inochi2D/inochi-creator/release-nightly.yml?label=Nightly&style=for-the-badge)](https://github.com/Inochi2D/inochi-creator/releases/tag/nightly)  

&nbsp;

## For those forking the repo
While the original repo discourages detached forks, I believe that detached forks can be used to create even more options for open source enjoyers (It is how this repo became independent, after all). Therefore, detaching a fork is not only allowed, it's also encouraged.

## For package maintainers
For some packages, I will support the package, especially if it is close to this detached fork.

## Connection to Nijigenerate
Due to Nijigenerate also being a fork of Inochi2d, It will using some of the code in Nijigenerate. Nijigenerate Higher-Ups, please don't get upset, I'm just following your example and will credit you for the code.

## Building
It's occasionally the case that my dependencies are out of sync with dub, so it's somewhat recommended if you're building from source to clone the tip of `main` and `dub add-local . "<version matching inochi-creator dep>"` any of my forked dependencies (i18n-d, psd-d, bindbc-imgui, facetrack-d, inmath, inochi2d). This will generally keep you up to date with what I'm doing, and it's how the primary contributors work. Ideally I'd have a script to help set this up, but currently I have to do it manually, PRs welcome :)

Because my project has dependencies on C++ through bindbc-imgui, and because there's no common way to get imgui binaries across platforms, I require a C++ toolchain as well as a few extra dependencies installed. These will be listed in their respective platform sections below.  
Currently you **have** to _recursively_ clone bindbc-imgui from git and set its version to `0.7.0`, otherwise the build will fail.

Once the below dependencies are met, building and running inochi-creator should be as simple as calling `dub` within this repo.

### Windows
#### Dependencies
- Visual Studio 2022 (With "Desktop development with C++" workflow installed)
  - In theory, "Build Tools for Visual Studio 2022" should also work, but is untested.
- CMake (Currently 3.16 or higher is needed.)
- Dlang, either dmd or ldc (ldc recommended)

### MacOS
#### Dependecies
- MacOS Terminal
- Homebrew, MacPorts, or other package manager
- CMake (Currently 3.27 or higher to avoid deperaction warnings is needed.)
- Dlang, either dmd or ldc (ldc recommended in most cases)
- If able to update to MacOS Sequoia, a container is recommended (Not neccesary if the mac is neither apple silcon nor is able to go to Sequoia. This also does not apply if the complier is dmd.)
- SDL2
- Freetype
- Finally, and most importantly, dub (required to successfully run the app)


### Linux
#### Dependencies
- The equivalent of build-essential on Ubuntu, on centos 7, this was `sudo yum groupinstall 'Development Tools'`, this should get you a working C++ toolchain.
- Dlang, either dmd or ldc (ldc recommended)
- CMake (Currently 3.16 or higher is needed.)
- SDL2 (developer package)
- Freetype (developer package)
- appimagetool (for building an AppImage)

