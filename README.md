# Fernando Voltolini de Azambuja

Color scientist and imaging engineer working across camera image quality, color
characterization, HDR/SDR perception, research software, measurement, and
photographic systems.

[LinkedIn](https://www.linkedin.com/in/fernando-voltolini-de-azambuja)

## Selected engineering work

### Camera image quality and modern C++

Developed and verified
[`cpp-camera-iq-toolkit`](https://github.com/ferazambuja/cpp-camera-iq-toolkit),
a public C++20 research toolkit for camera measurement and analysis. The
implemented workflows include:

- RAW/CFA statistics, black-level handling, and demosaic helpers;
- chart localization, patch extraction, color-correction matrices, and
  Delta E reporting;
- camera spectral-sensitivity and color-fidelity analysis;
- dark-frame noise, OECF/tone response, Stepchart checks, and slanted-edge
  SFR/MTF; and
- CMake/CTest automation with structured JSON and CSV outputs.

Featured case:
[SFR/MTF aperture and field analysis](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/reports/SFR_MTF.md).
Developed and tested an AI-assisted C++20 slanted-edge SFR/MTF workflow over
first-party archived Nikon D800/D810 lab captures; processed 414/414 field
ROIs across 18 aperture runs and retained the D800 non-transfer result rather
than retuning the D810-specific criterion.

[Toolkit](https://github.com/ferazambuja/cpp-camera-iq-toolkit) ·
[Coverage map](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/reports/CAMERA_IQ_COVERAGE.md) ·
[SFR/MTF case](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/reports/SFR_MTF.md)

This is research-scale measurement and analysis work, not shipped ISP or
production-camera ownership.

### HDR/SDR psychophysics research platform

Built an end-to-end Swift/Metal macOS research application connecting study
authoring, deterministic execution, response and session records, HDR
presentation state, measurement context, psychometric analysis, and structured
export.

This is a private M.S. thesis implementation. Its case-study configurations
demonstrate the platform and workflow; they are not presented as participant
findings.

## Published imaging research

- [Assessing the Ability of Simulated Laboratory Scenes to Predict the Image
  Quality Performance of HDR Captures (and Rendering) of Exterior Scenes Using
  Mobile Phone Cameras](https://doi.org/10.2352/ISSN.2470-1173.2017.12.IQSP-251)
- [Sensitivity analysis applied to ISO recommended camera color calibration
  methods to determine how much of an advantage, if any, does spectral
  characterization of the camera offer over the chart-based
  approach](https://doi.org/10.2352/ISSN.2470-1173.2017.15.DPMI-072)

These were team publications. My contributions included hands-on testing,
coding, and data analysis. For the mobile-HDR study, I also helped instruct
observers and supported captures, measurements, study execution, and writing.

## Imaging laboratory and photographic systems

My practical background connects engineering analysis to capture and output:

- color-measurement instrumentation and camera/image-quality evaluation;
- camera preparation, lighting, on-set capture review, and retouching handoff;
- digital, film, medium-format, large-format, 360-degree, and video systems;
- color-managed proofing, photographic printing, paper measurement, and
  profile creation; and
- four continuous years, including summers, as an RIT Photographic Equipment
  Student Manager, supporting a 3,000+ item facility and supervising 35+
  student employees.

Before RIT, I worked as a Photographic Assistant and Digital Capture Technician
in a professional advertising studio, supporting a color-managed
capture-to-proof workflow.

## Current technical focus

I am deepening fixed-point arithmetic, display-pipeline validation, modern C++,
and camera measurement through structured learning and portfolio work. Public
artifacts are linked here when they are ready to be inspected.

## Engineering approach

I build around traceable sources, repeatable tests, explicit limitations, and
results that remain useful when a hypothesis or acceptance criterion does not
transfer.
