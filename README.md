# Imaging Engineering & Color Science

I build camera image-quality, color-characterization, and HDR/SDR research
tools in C++20 and Swift/Metal, grounded in published imaging research,
hands-on color measurement, and a professional photography and digital-capture
foundation.

[LinkedIn](https://www.linkedin.com/in/fernando-voltolini-de-azambuja)

## Selected engineering work

### Camera image quality and C++

Built
[`cpp-camera-iq-toolkit`](https://github.com/ferazambuja/cpp-camera-iq-toolkit),
a public C++20 toolkit for RAW/CFA analysis, chart extraction, color-correction
matrices and Delta E, spectral sensitivity, OECF and noise, slanted-edge
SFR/MTF, and CFA flat-field response.

The
[SFR/MTF case study](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/sfr-mtf-aperture-field.md)
applies aperture and field analysis to Nikon D800/D810 laboratory captures and
keeps the capture-system-specific non-transfer result instead of forcing one
acceptance criterion onto both systems. Its field analysis is bounded by what
fixed-axis edges can support: near-mirror ROI pairs give strong evidence against
a centered rotationally symmetric field, stopping short of a formal exclusion,
and the responsible component—tilt, decentering, or alignment—is left
unresolved.

The
[CFA flat-field case study](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/cfa-flat-field-response.md)
screens 52 integrating-sphere captures down to the three that survive a
signal-referred clipping gate, then reports center-normalized green and
chromatic response. The 19.65% quadrant asymmetry diagnoses departure from a
centered radial field; independently, missing source- and camera-rotation
controls keep the result at capture-system attribution rather than lens
vignetting.

Additional studies connect monochromator RAW sweeps to spectral color-fidelity
analysis and trace a ColorChecker-SG capture through patch extraction and
held-out CCM validation.

[Toolkit](https://github.com/ferazambuja/cpp-camera-iq-toolkit) ·
[Technical documentation](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/README.md) ·
[SFR/MTF](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/sfr-mtf-aperture-field.md) ·
[CFA flat-field response](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/cfa-flat-field-response.md) ·
[Spectral color fidelity](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/spectral-color-fidelity.md) ·
[ColorChecker/CCM](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/colorchecker-ccm.md)

### HDR/SDR psychophysics research platform

Built an end-to-end Swift/Metal macOS research application for study authoring,
controlled execution, response and session records, HDR presentation state,
measurement context, psychometric analysis, and structured export as part of
my M.S. thesis.

## Published imaging research

- [Assessing the Ability of Simulated Laboratory Scenes to Predict the Image
  Quality Performance of HDR Captures (and Rendering) of Exterior Scenes Using
  Mobile Phone Cameras](https://doi.org/10.2352/ISSN.2470-1173.2017.12.IQSP-251)
- [Sensitivity analysis applied to ISO recommended camera color calibration
  methods to determine how much of an advantage, if any, does spectral
  characterization of the camera offer over the chart-based
  approach](https://doi.org/10.2352/ISSN.2470-1173.2017.15.DPMI-072)

These were team publications. My contributions included testing, coding, data
analysis, measurement, and study execution.

## Imaging and photographic systems

My background includes color measurement, camera and image-quality evaluation,
color-managed capture and output, and digital, film, studio, and video systems.
I spent four continuous years, including summers, as an RIT Photographic
Equipment Student Manager, supporting a 3,000+ item facility and supervising
35+ student employees. Before RIT, I worked as a Photographic Assistant and
Digital Capture Technician in a professional advertising studio.

## Current focus

Fixed-point arithmetic, display-pipeline validation, modern C++, and camera
measurement—supported by traceable sources, repeatable tests, and explicit
technical limitations.
