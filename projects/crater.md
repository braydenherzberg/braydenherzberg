# Crater

**Research tool · Public release v0.5.1 · Python desktop application**

[Source & documentation](https://github.com/braydenherzberg/Crater_Tracker) · [Downloads](https://github.com/braydenherzberg/Crater_Tracker/releases/latest) · [Method & limits](https://github.com/braydenherzberg/Crater_Tracker/blob/main/docs/analysis_method.md) · [Tracking benchmark](https://github.com/braydenherzberg/Crater_Tracker/blob/main/docs/benchmark.md)

Crater helps researchers review side-camera videos of crater development, including plume–surface interaction experiments. An operator identifies the physical interface; the app refines the line locally, tracks between keyframes, flags weak evidence, and exports calibrated width, vertical depth, and cross-section area. Processing stays offline.

## My contribution

I developed the Python analysis software as part of my work with the UCF Hawking Center's Knights Research Scholar Program team, where my responsibilities include nozzle design and data analysis. The software brings tracing, calibration, review, and export into one desktop workflow.

## Workflow

![Crater showing a seven-point guide on the bundled synthetic practice clip before physical scale is confirmed; measurements remain in pixels.](../assets/crater/01-trace.png)

**1. Define the interface.** Place a guide on the intended boundary. Before calibration is confirmed, the app reports pixels.

![Crater showing an interpolated profile between two keyframes, with a confirmed 64 mm practice-image width and the tracked cross-section below the video.](../assets/crater/02-review.png)

**2. Calibrate and review.** Inspect the tracked profile, its source, and the timeline between operator keyframes.

![Crater showing a reviewed keyframe, a calibrated profile, and the configured time-series export interval on synthetic practice data.](../assets/crater/03-export.png)

**3. Export with provenance.** Write sampled measurements to CSV and retain the JSON metadata describing calibration, keyframes, and settings.

[Watch the three-state workflow demo](../assets/crater/demo.gif). These are captures of the actual PySide6 application rendered locally with the bundled **synthetic** clip. The demonstrated dimensions are practice values, not research measurements.

## Engineering decision

Strong image edges can belong to reflections, dust, or container walls. I use an operator-defined guide with a bounded local edge search instead of treating the strongest automatic boundary as the physical crater. This requires annotation and review, but keeps the measurement tied to an explicitly selected interface. The original threshold tuner remains available for reviewed starting guides.

**Technology:** Python, PySide6, OpenCV, NumPy; calibrated CSV exports and JSON session/provenance records.

## Status and evidence

Version **v0.5.1** has published macOS Apple silicon, macOS Intel, and Windows release assets. The local demonstration exercised tracing, calibration, keyframe interpolation, session saving, and CSV/metadata export on the practice clip; it does not establish experimental accuracy.

The [method notes](https://github.com/braydenherzberg/Crater_Tracker/blob/main/docs/analysis_method.md#measured-repeatability) report a repeatability experiment on **one frame**, Mars Perfect Run 3 frame 9,191: twelve simulated operators placed seven clicks with ±4 px random error near the same line. Reported width standard deviation was **50.8 px without snapping** and **8.9 px with snapping**; depth standard deviation was **4.8 px** and **2.0 px**, respectively.

This measures sensitivity to simulated click placement. It is **not independent physical-accuracy validation**. Representative hand-labelled comparisons, calibration in the crater's optical plane, and review of rim/interface definitions remain necessary. Cross-section area is not volume; the confidence score is a review aid, not an uncertainty interval.

[Back to profile](../README.md)
