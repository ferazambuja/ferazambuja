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
SFR/MTF, CFA flat-field response, and spectroradiometer archive ingest.

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
screens 52 integrating-sphere captures from a Fujifilm X-T100 and Fujinon XF
14 mm f/2.8 R down to the three that pass a signal-referred near-ceiling gate,
then reports center-normalized green and chromatic response. The 19.65% quadrant
asymmetry diagnoses departure from a centered radial field; independently,
missing source- and camera-rotation controls keep the result at capture-system
attribution rather than lens vignetting.

The same CFA-domain, per-position criterion screens ColorChecker correction
flats before demosaic. On one rejected capture, the worst position (G2) reads
11.63% near ceiling in the centered gate against 0.50% frame-wide and a 1%
limit. The centered and full-frame checks expose local headroom loss that a
pooled frame statistic does not, while the correction normalizer stays the
full-frame valid-sample mean.

The
[spectroradiometer ingest case study](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/spectroradiometer-ingest.md)
reads a MATLAB v5 archive through a parser written from the format
specification, so the analysis runs without MATLAB. Measurement identity comes
from content hashing rather than from filenames, which number acquisitions
rather than scenes: 89 canonical measurements, with 45 further paths shown to be
byte-identical copies and therefore excluded from the counts. Reporting absolute
level, normalized shape, and chromaticity separately is what locates the
variation—across the 37 repeated groups the spectral-integral coefficient of
variation reaches 41.65%, while normalized shape stays within 1.076% and
chromaticity within 0.002852 Δu′v′, with those maxima falling in different
groups. Source output, geometry, acquisition settings, and instrument behavior
are not separable from the retained records, so this is reported as within-group
observed variation rather than drift or repeatability. The spectra reproduce
recorded XYZ below 2e-13% under one fitted scale—numerical closure within a
single record, not an instrument-accuracy test.

Two further studies carry the same standard. One extracts a Canon 5D2 spectral
sensitivity function from monochromator RAW sweeps and closes four same-session
camera and chart datasets above 0.992 minimum channel correlation, then compares
five cameras under Luther and ISO 17321-style fidelity metrics. The other traces
a ColorChecker-SG capture from RAW patch extraction—agreeing with an independent
reference tool above 0.99999998 correlation at sub-0.4 DN RMSE—through flat-field
and white-balance correction to held-out CCM validation at 4.134 mean CIEDE2000.

[Toolkit](https://github.com/ferazambuja/cpp-camera-iq-toolkit) ·
[Technical documentation](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/README.md) ·
[SFR/MTF](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/sfr-mtf-aperture-field.md) ·
[CFA flat-field response](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/cfa-flat-field-response.md) ·
[Spectroradiometer ingest](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/case-studies/spectroradiometer-ingest.md) ·
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
