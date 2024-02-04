# Neural Amp Modeler Plug-in with added HD antialias filter

Either compile as instructed below or download the release which contains the AU and VST versions. AU can be unzipped and placed to ~/Library/Audio/Plug-Ins/Components and VST can be unzipped and placed to ~/Library/Audio/Plug-Ins/VST


A VST3/AudioUnit plug-in\* for [Neural Amp Modeler](https://github.com/sdatkinson/neural-amp-modeler), built with [iPlug2](https://iplug2.github.io).

- https://www.youtube.com/user/RunawayThumbtack
- https://github.com/sdatkinson/neural-amp-modeler

## Installation

Check the [Releases](https://github.com/sdatkinson/NeuralAmpModelerPlugin/releases) for pre-built installers for the plugin!

## Supported Platforms

The Neural Amp Modeler plugin currently supports Windows 10 (64bit) or later, and macOS 10.15 (Catalina) or later.

For Linux support, there is an LV2 plugin available: https://github.com/mikeoliphant/neural-amp-modeler-lv2.

## About

This is a cleaned up version of [the original iPlug2-based NAM plugin](https://github.com/sdatkinson/iPlug2) with some refactoring to adopt better practices recommended by the developers of iPlug2.
(Thanks [Oli](https://github.com/olilarkin) for your generous suggestions!)

\*could also support VST2, AAX, CLAP, Linux, iOS soon.

## To compile

### Before opening in xcode

bash -x setup_container.sh
Press ctrl-c when asking for password, this will still fetch all libraries

Then open this in xcode : NeuralAmpModeler/NeuralAmpModeler.xcworkspace

### After opening in xcode

Setup developer keys in xcode. Note: you don't need to pay $99 to apple to dev and test on your own machine.

### Compile from cmd line to see what the heck is going on

xcodebuild -project NeuralAmpModeler/projects/NeuralAmpModeler-macOS.xcodeproj clean

xcodebuild -project NeuralAmpModeler/projects/NeuralAmpModeler-macOS.xcodeproj -configuration Release build

### Test the compiled plugin

Now, the plugin should be in  /Users/USERNAME/Library/Audio/Plug-Ins/VST3/NeuralAmpModeler.vst3 and e.g., Reaper automatically finds it there at the next Reaper launch.
