# Sound Docs

It all began with a swing of a CPU clock.

## Repos:

General:

- Gisele sequencer: https://github.com/Lcchy/gisele
- Tadeusz granular synth: https://github.com/Lcchy/tadeusz
- Reverbs: https://github.com/Lcchy/verb
- FAUST Moog Ladder filter: https://github.com/Lcchy/moog_filter
- Dump of Pd patches and externals: https://github.com/Lcchy/pd-stuff

Fates:

- Install/Deploy script for Fates: https://github.com/Lcchy/fates-deploy
- Fates presets backup: https://github.com/Lcchy/fates-presets
- Orac Modules: https://github.com/Lcchy/orac-modules
- MEC fork from Technobear: https://github.com/Lcchy/MEC-private
- NuiLite fork from Technobear: https://github.com/Lcchy/NuiLite-private
- Eyesy for Fates: https://github.com/Lcchy/Eyesy_for_fates

Old:

- MaxMSP external for gesture recognition using knn classification: https://github.com/Lcchy/Gexture
- Audio visual source location and separation model: https://github.com/Lcchy/AVSep_NET
- DDSP sound synthetizer: https://github.com/Lcchy/DDSP

## Mappings:

Note: Midi Channel 0 is OMNI

- MIDI channels:

  - Eyesy : 9
  - Orac :

    - Chains: 1,2,3
    - Clock: In 1 - Out 1
    - Active module: 0-16 ?? TODO Check with Aux: 1 CC 69
    - Router EC4 control ([source](https://github.com/Lcchy/orac-modules/blob/main/fates_usermodules/router/aapart/parallel_dig_mult/module.pd)): 10 (CC 0 to 7)
    - Nui osc dev map ([source](https://github.com/Lcchy/orac-modules/blob/main/fates_usermodules/router/aapart/parallel_dig_mult/module.pd)): Ch 11
      - NRPN CC 98 99, 6 38 - Ids 00-Params#
      - ModuleSelect-PageSelect: CC 0-1

  - QuNexus LEDs: 1?

- OSC UDP ports:

  - Eyesy: 4000 and 4001 (and 4002 for foregd_mode)
  - MEC:

    - Kontrol (Creation, only used by Orac internally): r 6000 - s 6001
    - Nui OSC device ([source](https://github.com/Lcchy/MEC-private/blob/d872dcad8c574281ecfb098f9e593040da49c1e1/mec-api/devices/mec_nui.cpp#L503)): r 6100 - s 6101

  - Sidekick (see NuiLite for source): s 3000 and r 3001
  - Arc (see [doc](https://monome.org/docs/serialosc/osc/)):
  - Grid: ?

## Fates Orac/MEC Arch:

![](fates_arch.svg)
