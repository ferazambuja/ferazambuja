# Imaging Engineering & Color Science

I build C++20, Python, and Swift/Metal tools for camera image quality, color
science, and HDR/SDR research. My work combines sensor-level analysis,
numerical methods, and hands-on color measurement with professional studio
experience as a Photographic Assistant and Digital Capture Technician.

[LinkedIn](https://www.linkedin.com/in/fernando-voltolini-de-azambuja)

## Selected engineering work

### Camera image quality and C++

Built
[`cpp-camera-iq-toolkit`](https://github.com/ferazambuja/cpp-camera-iq-toolkit),
a public C++20 toolkit for RAW/CFA analysis, color characterization, spectral
measurement, tone and noise, slanted-edge SFR/MTF, and spatial-response
analysis. Selected results demonstrate both measurement design and technical
judgment:

- [SFR/MTF](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/sfr-mtf-aperture-field.md):
  analyzed 299 field ROIs across Nikon D800 and D810 aperture sweeps. The D810
  capture system peaked at f/5.6; the D800 showed a different aperture trend and
  asymmetric field behavior, so the study retained separate capture-system
  conclusions. Fixed-axis edges constrain the asymmetry but cannot isolate
  tilt, decentering, or alignment.
- [CFA flat-field response](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/cfa-flat-field-response.md):
  screened 52 integrating-sphere captures and retained the three with usable
  headroom. A 19.65% quadrant asymmetry exceeded the declared 5% criterion and
  was inconsistent with a centered radial scalar model for the measured
  composite field; missing source- and camera-rotation controls prevent
  lens-only attribution.
- Measurement qualification: per-CFA screening of the bright central region
  rejected a correction flat because G2 was 11.63% near ceiling there even
  though the same G2 position measured only 0.50% over the full frame. A
  separate ColorChecker localization model was rejected at 16.449 px error
  against a 5 px criterion even though channel
  correlations exceeded 0.999.
- [Spectroradiometer ingest](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/spectroradiometer-ingest.md):
  implemented a scoped C++ reader for the compressed MATLAB Level-5 structures
  present in the archive, removing a MATLAB runtime dependency, and resolved 45
  byte-identical aliases by content hash. A separate MATLAB R2026a parser check
  matched all 89 ledger-bound source files, including exact SHA-256 agreement
  on all 178 numeric vectors. Across 37 multi-reading groups, spectral-integral
  CV was 7.17% median and 41.65% maximum; maximum normalized-shape residual was
  1.076%; and maximum recorded-XYZ pair separation was 0.002852 Δu′v′. These metrics
  describe different properties, their maxima occur in different groups, and
  they do not identify the cause.
- [Spectral and color validation](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/spectral-color-fidelity.md):
  extracted a Canon 5D2 spectral sensitivity from monochromator RAW sweeps and
  closed four same-session camera/chart datasets above 0.992 minimum channel
  correlation. The [ColorChecker/CCM path](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/colorchecker-ccm.md)
  matched an independent extraction above 0.99999998 correlation with sub-0.4
  DN RMSE and reached 4.134 mean held-out CIEDE2000 after flat-field and
  white-balance correction.
- [Color-management algorithms](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/gamut-mapping.md):
  implemented Display-P3-to-sRGB mapping in CIELAB and OkLCh with analytic
  boundary searches and the CSS Color 4 Local-MINDE method. Holding OkLCh fixed
  and changing only the algorithm reduced the 125-point grid's mean/maximum
  CIEDE2000 from 2.947/9.956 to 2.323/7.602. A separate
  [color-model equation audit](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/color-model-equation-audit.md)
  quantified bounded CAM16 lightness/background couplings and retained an
  unfavorable published result; these synthetic studies test algorithms and
  equations, not observer performance or a measured display.

[Toolkit](https://github.com/ferazambuja/cpp-camera-iq-toolkit) ·
[Technical documentation](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/README.md) ·
[SFR/MTF](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/sfr-mtf-aperture-field.md) ·
[CFA flat-field response](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/cfa-flat-field-response.md) ·
[Spectroradiometer ingest](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/spectroradiometer-ingest.md) ·
[Spectral color fidelity](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/spectral-color-fidelity.md) ·
[ColorChecker/CCM](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/colorchecker-ccm.md) ·
[Gamut mapping](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/gamut-mapping.md) ·
[Color-model equation audit](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/color-model-equation-audit.md)

### HDR/SDR psychophysics research platform

Built an end-to-end Swift/Metal macOS research application for study authoring,
controlled execution, response and session records, HDR presentation state,
measurement context, psychometric analysis, and structured export as part of
my M.S. thesis under Dr. Mark D. Fairchild.

## Published imaging research

Both are coauthored team publications, listed in their published author order.

- [Sensitivity analysis applied to ISO recommended camera color calibration
  methods to determine how much of an advantage, if any, does spectral
  characterization of the camera offer over the chart-based
  approach](https://doi.org/10.2352/ISSN.2470-1173.2017.15.DPMI-072) —
  2017(15), 32–36. Keith Borrino; **Fernando Voltolini de Azambuja**; Nitin
  Sampat; J. A. Stephen Viggiano.
  I performed the monochromator-plus-camera and camSPECS spectral-responsivity
  captures and contributed to the team's coding and data analysis.
- [Assessing the Ability of Simulated Laboratory Scenes to Predict the Image
  Quality Performance of HDR Captures (and Rendering) of Exterior Scenes Using
  Mobile Phone Cameras](https://doi.org/10.2352/ISSN.2470-1173.2017.12.IQSP-251)
  — 2017(12), 100–104. Amelia Spooner; Ashley Solter; **Fernando Voltolini de
  Azambuja**; Nitin Sampat; J. A. Stephen Viggiano; Brian Rodricks; Cheng Lu. I
  helped instruct observers, contributed study code and data analysis, and
  supported captures, measurements, and writing.

## Imaging and photographic systems

My background includes color measurement, camera and image-quality evaluation,
color-managed capture and output, and digital, film, studio, and video systems.
In a professional advertising studio, I worked as a Photographic Assistant and
Digital Capture Technician, supporting digital capture, lighting, and
color-managed workflows. I also spent four continuous years, including
summers, as an RIT Photographic Equipment Student Manager, supporting a 3,000+
item facility and supervising 35+ student employees.

## Current focus

Color-management algorithms, camera measurement, display-pipeline validation,
fixed-point arithmetic, and modern C++—supported by traceable sources,
repeatable tests, and explicit technical limitations.
