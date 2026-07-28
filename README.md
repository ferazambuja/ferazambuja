# Fernando Azambuja

Color scientist and imaging engineer working across camera image quality,
color characterization, HDR/SDR perception, research software, measurement,
and photographic systems.

## Portfolio map

### Camera image quality and modern C++

I developed and verified
[`cpp-camera-iq-toolkit`](https://github.com/ferazambuja/cpp-camera-iq-toolkit)
with AI assistance. This public C++20 research toolkit covers:

- RAW/CFA statistics, black-level handling, and demosaic helpers;
- chart localization, patch extraction, color-correction matrices, and
  Delta E reporting;
- camera spectral-sensitivity and color-fidelity analysis;
- dark-frame noise, OECF/tone response, Stepchart checks, and
  slanted-edge SFR/MTF;
- CMake/CTest automation, structured JSON/CSV reports, and private-data
  guardrails.

The repository contains code, tests, small fixtures, and evidence reports.
Its [coverage and known-gaps
report](https://github.com/ferazambuja/cpp-camera-iq-toolkit/blob/main/docs/reports/CAMERA_IQ_COVERAGE.md)
maps the implemented surface without inflating it into production experience.
Large RAW captures and measured laboratory references remain private. It is a
research toolkit—not a production ISP, camera driver, factory-calibration
system, standards-certification suite, or commercial Imatest replacement.

### HDR/SDR psychophysics research platform

Built an end-to-end Swift/Metal macOS research application connecting study
authoring, deterministic execution, response and session records, HDR
presentation state, measurement context, psychometric analysis, and structured
export.

This private M.S. thesis implementation is an infrastructural contribution.
Its encoded case studies are evidence specifications, not participant-result
reports; I do not claim new perceptual findings from them.

### Published imaging research

- [Sensitivity analysis applied to ISO recommended camera color calibration
  methods](https://doi.org/10.2352/ISSN.2470-1173.2017.15.DPMI-072) —
  camera spectral characterization, chart-based profiling, measurement, and
  sensitivity analysis.
- [Assessing simulated laboratory scenes as predictors of mobile HDR
  image-quality performance](https://doi.org/10.2352/ISSN.2470-1173.2017.12.IQSP-251)
  — HDR capture and measurement, laboratory/field comparison, and a
  paired-comparison observer study.

These were team publications. My contributions included hands-on testing,
coding, and data analysis; for the mobile-HDR study I also helped instruct
participants and support study execution.

### Imaging laboratory and photographic systems

My practical background connects engineering analysis to capture and output:

- color-measurement instrumentation and camera/image-quality evaluation;
- camera preparation, lighting, on-set capture review, and retouching handoff;
- digital, film, medium-format, large-format, 360-degree, and video systems;
- color-managed proofing, photographic printing, paper measurement, and
  profile creation; and
- management support for an approximately 3,000-item RIT photography equipment
  inventory spanning cameras, lighting, studios, darkrooms, and print
  resources.

### Current learning direction

I am deepening fixed-point arithmetic and display-pipeline validation through a
private, AI-assisted learning track built from public and properly licensed
sources. This is learning and research-scale implementation—not prior
production SoC/RTL, silicon, panel, factory, or shipped-product experience.

## How I present evidence

I link public code and publications where available, keep private source data
private, preserve negative results, and distinguish portfolio/research work
from employment or production ownership.
