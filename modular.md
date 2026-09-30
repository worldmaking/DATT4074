# Modular Synthesis

We saw back in week 1 how [modular synthesis first emerged in the 1960's in commercial forms via Moog and Buchla](https://nodemusic.cc/horizon), following structures of analog computing, and then resurged since the 1990's in the Eurorack format, which continues to grow today. 

https://docs.google.com/presentation/d/18B0RG7yMWeV9qoKtok4VDIn6UE_LBpKkcyzYGX4op5U/



### Daisy in Modular

Since the Daisy was launched in 2021, there have been very many commercial as well as DIY & open source module designs, and even more firmware designs in the wild. It has become a default platform for many designers. 

I have gen~ patch templates for several different Daisy-powered hardware modules in the Alice Lab rack:
- Versio (https://noiseengineering.us/products/versio/)
- Daisy Patch (x2) (https://modulargrid.net/e/electrosmith-daisy-patch)
- patch.Init (x2) (https://daisy.audio/products/patch-init)
- Bluemchen (https://kxmx-bluemchen.recursinging.com)
- I also have a home-brewed Daisy module, and we may also design another with PCB manufacturing if we move quickly enough. 

Here are some example firmwares people have created just for the [Versio module](https://noiseengineering.us/pages/world-of-versio/), many that are open-source, some which are ports of open source algorithms, some made using gen~/oopsy:
  - Valley Plateau / Campestria Versio (plate reverb based on Dattoro's algorithm)
    - VCV: https://valleyaudio.github.io/rack/plateau/
    - Hardware (Versio, C++): https://github.com/digitalartifactmusic/PlateauNEVersio
  - Mutable Rings (string synthesis) ports:
    - VCV: https://library.vcvrack.com/AudibleInstruments/Rings
    - Versio: https://www.reddit.com/r/modular/comments/1gyxrkd/dont_have_mutable_instruments_rings_i_ported_it/
  - Pyros distortion
    - VST plugin: https://www.audiority.com/shop/pyros/
    - Versio firmware: https://www.audiority.com/shop/pyros-versio/
  - Pleroma mutant reverb: https://recursivefieldinstruments.com/pleroma
  - Praetereo Versio looper (made with `gen~`): https://www.youtube.com/watch?v=pOsEjsxFNU4
  - Acidus Versio (303 acid oscillator): https://github.com/abluenautilus/AcidusVersio/
  - Tapeo (tape delay emulator, made with `gen~`): https://github.com/onoma2/TapeoVersio
  - Clackotron low pass gate: https://bionoid.one//apps/clackotron/index.html
  - Repetita Versio looper (C++) https://github.com/hirnlego/repetita-versio
  - CRCLTR looper (`gen~`) https://github.com/s3g/crcltr
  - MultiVersio (multiFX) https://github.com/peteb4ker/MultiVersio
  - J&OT Stray Drum (drum voice) https://jasmineandolivetrees.com/pages/stray-drum-versio-firmware
  - Reticulum Versio (asynchronous delay) https://www.youtube.com/watch?v=4a6SyudL77M
  - Triwalkmas (made with `gen~`): https://github.com/onoma2/TriwalkmaVersio
  - So many more here: https://github.com/Maxhodges/noise-engineering-firmware-index#versio-third-party-firmware

## VCV Rack

https://vcvrack.com/

VCV Rack is a free and open-source cross-platform software modular synthesizer modeled directly on Eurorack format. It comes with a collection of built-in modules, but many more can be added as **plugins** -- [over 4,000 free plugins](https://library.vcvrack.com/?query=&brand=&tag=&license=free) at the time of writing. 

- [Here's a list of 400+ plugins that clone actual physical modules](https://library.vcvrack.com/?tag=Hardware+clone). Sometimes the VCV module is made first, becomes popular, then is ported to hardware. Sometimes popular hardware modules are cloned in VCV. Sometimes a company will release a new design in both hardware and VCV simultaneously.
  - For example, [this collection](https://library.vcvrack.com/?brand=Nonlinear%20Circuits) by [Michael Hetrick](https://mhetrick.com/) of [Unfiltered](https://www.unfilteredaudio.com/) Audio all emulate [Nonlinear Circuits](https://www.nonlinearcircuits.com/) modules -- and [here is the source code for them](https://github.com/mhetrick/nonlinearcircuits), much of which was created as part of his graduate studies.
  - For example, [this collection](https://vcvrack.com/AudibleInstruments) is an authorized VCV Rack port of [Mutable Instruments open source Eurorack modules](https://mutable-instruments.net/).

Quick tips:
- Add a module by right clicking empty space, or pressing Enter
- To set the output, create an `Audio` module, click the option just under the module title to pick your output device. 
- It can be useful to add a `Scope` too. 
- Use scrollbars or middle mouse button or alt-drag or arrow keys to move around.  Use ctrl +/- or the zoom slider to zoom. 
- Fullscreen with F11
- Drag ports to create and move cables. Stack multiple cables on outputs by holding Ctrl (Cmd on Mac) and dragging from an output.  Disconnect a cable end to remove the cable. 
- Drag knobs up/down to rotate. Hold Ctrl (Cmd on Mac) while dragging to fine-tune. Right-click knobs to edit, and double-click to initialize.
- Right click a module & choose "Info > User Manual" to get to know it
- [Manual](https://vcvrack.com/manual/)

### Developing your own VCV plugins

- [Tutorial](https://vcvrack.com/manual/PluginDevelopmentTutorial)
  - Skip the "building Rack" section of the [development setup](https://vcvrack.com/manual/Building)
  - Download the Rack-SDK, create a folder inside it called `Plugins`
  - In a terminal/console inside of this `Plugins` folder, run `../helper.py createplugin MyPlugin`, where "MyPlugin" is the unique name for your project collection. 
  - Before creating a module in your plugin collection, you'll need to design the [panel as SVG graphics](https://vcvrack.com/manual/Panel)
    - Many people use Inkscape to make their panels. There's an [inkscape plugin here](https://synthpanels.design/) specifically for VCV Rack. 
    - There's an online panel designer [here](https://vpdx.pages.dev/), with a [manual here](https://github.com/transcriptaze/vpd/blob/main/GUIDE.md#getting-started).
  - To create an actual module, first `cd MyPlugin`, and then from there run `../../helper.py createmodule MyModule res/MyModule.svg src/MyModule.cpp`.

I can also share templates for building VCV software modules that emulate the same Daisy-powered hardware modules we have.    