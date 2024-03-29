# BIBO2-PrusaSlicer
Version: 0.0.8-alpha3<br>
Release Date: 2023-10-09<br>

## Summary
A PrusaSlicer configuration bundle for BIBO2 printers following the [vendor bundle design](https://github.com/prusa3d/PrusaSlicer/wiki/Vendor-bundles-and-updating-process)
This version has been renamed to as a different vender (BIBO-Development) and different printer (BIBO2-dev) to avoid naming conflicts with the official community version bundled in PrusaSlicer. The official community version bundled in Prusaslicer is derived from the profiles in develpment in the repository,

The original creation of this config bundle was heavily influenced by the PrusaSlicer included [Creality vendor profiles](https://github.com/prusa3d/PrusaSlicer/blob/master/resources/profiles/Creality.ini) and the [Prusa vendor profiles](https://github.com/prusa3d/PrusaSlicer/blob/master/resources/profiles/PrusaResearch.ini). Further modifications were made based on knowledge about the BIBO2 printer's stock Marlin firmware, dual extruder printers, work done for a BIBO2 Cura print profile, and community testing by users in the BIBO official Facebook Group.

## Getting Started
**Very important to [import the ini config bundle as a config bundle](https://www.filamentone.com/blogs/3d-printing-blog/prusa-slicer-how-to-import-configuration-bundle)**. Failure to do this will result in problems. This version has been renamed to as a different vender (BIBO-Development) and different printer (BIBO2-dev) to avoid naming conflicts with the official community version bundled in PrusaSlicer.

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
- Pre-release 0.0.8-alpha3 (2023-10-09): Renamed to as a different vender (BIBO-Development) and different printer (BIBO2-dev) to avoid naming conflicts with the official community version bundled in PrusaSlicer.
- Pre-release 0.0.8-alpha2 (2023-03-07): Continue Alpha 1 fixes, improve end gcode by reseting each extruder removing and ambiguous state. Reduce G92 E0 calls in start gcode to minimum needed to prevent Issue #1
- Pre-release 0.0.8-alpha1 (2023-03-06): Fix for Issue #1 filament unloading at start of print. Other start gcode fixes, improve supports by setting default support contact distance to layer height.
- Pre-release 0.0.6-alpha2 (2023-01-28): Adopts the 2022 Maker's Muse "common changed" slicer settings video https://youtu.be/mE521Q4H6aY
  - List of modifications:
    - perimeters = 3 (was 2)
    - infill = 15% (was 20%)
    - fill_pattern = cubic or support cubic (was grid)
    - elephant_foot_compensation = 0.3 (was 0)
    - seam_position = aligned (current setting)
    - ensure_vertical_shell_thickness = off (current setting)
- Pre-release 0.0.6-alpha1 (2023-01-13):copies some settings from Prusa Slicer's 0.0.5 configuration file.Match Machine limits to Firmware limits for correct time estimation. These are only telling the slicer what the right values to use for time estimation and are not affecting gcode. Also reorganized the machine limit values to match with the user interface order in the GUI. Removed duplicate homing from all start gcode (and other duplicates where found). Added T0 for all gcode just before homing to avoid tool offset issues. in some cases this was already implemented and was only reorganized for consistency.
- Pre-release 0.0.4-alpha1 (2021-01-09): copies some settings from Prusa Slicer's RC3 0.0.3 configuration file. Modifies some extrusion width and speed settings. Machine Jerk settings were increased (but machine limits do not matter as it's only used for time estimates).
- Pre-release 0.0.2-beta1 (2020-04-06): Fixes the first layer temp for ditto printing. Re-impliments the new conditional output naming convention as PrusaSlicer 2.2.0 has been released. Moved this to 0.0.2-beta1 to remove conflicts with v0.0.1 included in PrusaSlicer 2.2.0
- 0.0.1 (2020-03-23) First offical release included in PrusaSlicer 2.2.0 release but not released in this repo, most closly resembles our 0.0.1-beta3
- Pre-release 0.0.1-beta4 (2020-03-21): Revert PrusaSlicer2.2.0-RC3 output naming convention until Prusaslicer 2.2.0 for BC compatability. Change file/folder naming for Vender compliance. Some print setting and accelleration/jerk changes which seem to improve top surface finish and retraction strings.
- Pre-release 0.0.1-beta3 (2020-03-11): Multiple Print models were unified into a single one. Other improvements were adopted from the changes PrusaSlicer made to their version of this profile.
- Pre-release 0.0.1-beta2 (2020-03-09): Bed model and textures added. Materials all use the BOBO2 identifier. deretract speed set to 0 to use retract speed.
- Pre-release 0.0.1-beta1 (2020-03-04): Added new printer profiles for ditto printing. New retraction settings, new materials. Removed some settings which do not apply. More start gcode improvements.
- Pre-release 0.0.1-alpha13 (2020-02-20): Adjusted Jerk, Acceleration, and maximum feedrates to better match the stock firmware. For Dual extrusion, tool change retractions were increased.
- Github repository created (2020-02-13): development of 0.0.1-alpha12 started with github hosting.
- Pre-release 0.0.1-alpha11 (2020-02-12): Revised version available to community for testing. Removed PVA and HIPS disolvable support materials from single extruder versions. Improved single extruder second nozzle standby temperature.
- Pre-release 0.0.1-alpha8 (2020-02-09): Available to community Early adopters for testing. Corrected filament settings to prevent duplicates, and reworked start and end gcode.
- Pre-release 0.0.1-alpha (2020-01-25): Available to community Early adopters for testing.
