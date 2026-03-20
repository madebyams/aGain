# aGain

A lightweight audio gain plugin built with the [JUCE](https://juce.com/) framework.

## Overview

aGain is a simple VST3 gain (volume) plugin that applies a linear gain multiplier to a stereo audio signal. The gain parameter is displayed in dB for a familiar user experience, supporting a range from -∞ dB (silence) to approximately +6 dB.

## Building

### Prerequisites

**CMake 3.30+** and a C++23-capable compiler.

On Linux, install the required system libraries:

```bash
sudo apt-get install libxext-dev libxrandr-dev libxinerama-dev libxcursor-dev \
                     libxi-dev libgtk-3-dev libasound2-dev
```

### Compile

```bash
cmake -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build --config Release
```

The VST3 plugin will be placed in the `build/` directory.

## Usage

Load the generated `.vst3` plugin into any compatible DAW (Reaper, Ableton Live, Studio One, etc.) and use the **Gain** parameter to control the output volume in dB.

## Project Structure

```
.
├── CMakeLists.txt          # Build configuration
├── include/
│   └── AGainProcessor.hh   # Plugin class declaration
├── src/
│   └── AGainProcessor.cc   # Audio processing implementation
└── concept/
    └── aGainConcept.scd    # SuperCollider proof-of-concept
```

## Dependencies

- [JUCE 8.0.8](https://github.com/juce-framework/JUCE) — fetched automatically via CMake FetchContent

## License

&copy; anotherSimpleCoder
