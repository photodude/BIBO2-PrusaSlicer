# BIBO2-PrusaSlicer
Version: 0.0.1-beta4<br>
Release Date: 2020-03-21<br>

## Summary
A PrusaSlicer configuration bundle for BIBO2 printers following the [vendor bundle design](https://github.com/prusa3d/PrusaSlicer/wiki/Vendor-bundles-and-updating-process)

The original creation of this config bundle was heavily influenced by the included [Creality vendor profiles](https://github.com/prusa3d/PrusaSlicer/blob/master/resources/profiles/Creality.ini) and the [Prusa vendor profiles](https://github.com/prusa3d/PrusaSlicer/blob/master/resources/profiles/PrusaResearch.ini). Further modifications were made based on knowledge about the BIBO2 printer's stock Marlin firmware, dual extruder printers, and work done for a BIBO2 Cura print profile.

## Getting Started
Very important to [import the ini config bundle as a config bundle](https://www.filamentone.com/blogs/how-to/prusa-slicer-how-to-import-configuration-bundle). Failure to do this will result in problems.

Once installed remember you need to select the Printer first, Print profile second and Filaments last. Many of the settings and filaments are tied to the "Printer Compatability" definitions. For instance disolvable filaments like PVA and HIPS are set to only show when the Dual extruder printer is selected.

## Branch configurations
Several branch configurations have been created to benifit the community.

### Master branch
The Master branch is designed for Stock printers with the standard 8-bit MKS Gen L Motherboard and no major hardware modifications.

### 32-bit mod
Thge 32-bit mod branch is designed for users who have modified their printer with upgrades to a 32-bit motherboard, TMC2209 stepper drivers and custom marlin 2.0.x firmware. This branch started as a copy of the Master branch and tuned by users with those modifications.

## Versoning
The versioning system used by PrusaSlicer is based on [Semantic Versioning](https://semver.org/), the config_version field expects a version string formated as Major.minor.patch, optionally there may also be a pre-release string (such as "-alpha") appended.

## Version History
- Pre-release 0.0.1-beta4 (2020-03-21): Revert PrusaSlicer2.2.0-RC3 output naming convention until Prusaslicer 2.2.0 for BC compatability. Change file/folder naming for Vender compliance.  Some print setting and accelleration/jerk changes which seem to improve top surface finish and retraction strings.
- Pre-release 0.0.1-beta3 (2020-03-11): Multiple Print models were unified into a single one. Other improvements were adopted from the changes PrusaSlicer made to their version of this profile.
- Pre-release 0.0.1-beta2 (2020-03-09): Bed model and textures added. Materials all use the BOBO2 identifier. deretract speed set to 0 to use retract speed.
- Pre-release 0.0.1-beta1 (2020-03-04): Added new printer profiles for ditto printing. New retraction settings, new materials. Removed some settings which do not apply. More start gcode improvements.
- Pre-release 0.0.1-alpha13 (2020-02-20): Adjusted Jerk, Acceleration, and maximum feedrates to better match the stock firmware. For Dual extrusion, tool change retractions were increased.
- Github repository created (2020-02-13): development of 0.0.1-alpha12 started with github hosting.
- Pre-release 0.0.1-alpha11 (2020-02-12): Revised version available to community for testing. Removed PVA and HIPS disolvable support materials from single extruder versions. Improved single extruder second nozzle standby temperature.
- Pre-release 0.0.1-alpha8 (2020-02-09): Available to community Early adopters for testing. Corrected filament settings to prevent duplicates, and reworked start and end gcode.
- Pre-release 0.0.1-alpha (2020-01-25): Available to community Early adopters for testing.
