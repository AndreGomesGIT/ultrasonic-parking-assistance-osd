# Testing and Validation

## Evidence status

The project archive includes a recorded display demonstration, physical oscilloscope photographs, a desktop waveform capture, simulation screenshots, and raw binary files.

These materials document development and investigation activity. They do not constitute a complete validation report: test setups, probe locations, reference distances, acceptance criteria, and repeatability records have not been supplied. The raw binary format has not been decoded or verified.

No new hardware tests were performed as part of this documentation review.

## Existing display evidence

The demonstration recording is approximately 91 seconds long. Selected frames were inspected at approximately 9, 36, 64, and 82 seconds.

| Approximate position | Observation | What remains unverified |
| --- | --- | --- |
| 9 s | A numerical value and proximity bars appear over the camera image. | Reference distance, units, and measurement error. |
| 36 s | The `PARE` warning is visible with the bar indicator. | Trigger threshold and repeatability. |
| 64 s and 82 s | Dashes appear in place of the numerical value. | Meaning of the state and conditions that produce it. |

These observations establish visible display states. Sampling a recording does not establish continuous stability, transition timing, or the correctness of the underlying measurement.

See the [demonstration recording](videos/demo.mp4) and the selected frames in [README.md](README.md).

## Existing waveform evidence

### Physical measurements

The oscilloscope photographs contain two-channel traces with burst-like activity and subsequent signal responses. A separate desktop capture also presents waveform data.

Without a documented connection diagram and test setup, channel functions cannot be assigned reliably. Numerical annotations visible on instrument screens should not be promoted to product specifications without the supporting context.

### Simulation

The simulation screenshots display a virtual oscilloscope and circuit responses. They are evidence of simulation work and must remain distinct from physical bench measurements.

The detailed simulation circuit and raw binary files are excluded from the public edition. A future public result can use a simplified plot or a reviewed capture with an explanation of the measured quantities.

## Proposed quantitative validation

The following tests are proposed follow-up work. They are not recorded as passed or completed.

| Test | Method | Required record |
| --- | --- | --- |
| Distance comparison | Place a documented target at measured positions within the intended operating range. | Reference positions, displayed readings, units, sample count, and measurement uncertainty. |
| Repeatability | Repeat measurements with a stationary target and unchanged setup. | Variation, missing readings, and intermittent states. |
| Display transitions | Move a target through numerical, warning, and dash states. | Reference positions, state meanings, transition conditions, and repeatability. |
| Target sensitivity | Compare defined target materials, sizes, and orientations. | Target description and detection behavior. |
| Dynamic response | Move a target along a documented path with a suitable timing reference. | Measurement and display response; uncertainty in any reported delay. |
| Video behavior | Observe changing sensor information while monitoring the camera view. | Overlay readability, visible disturbances, and recovery events. |
| Missing input | Evaluate defined sensing or video input loss conditions. | Display behavior, persistence of old information, and recovery. |
| Extended operation | Operate for a predetermined duration under recorded conditions. | Duration, interruptions, drift, and any abnormal behavior. |

Define the intended operating range and acceptance criteria before executing these tests. Do not substitute a sensor datasheet's limits for measured performance of the assembled system.

## Bench measurement procedure

1. Record hardware and firmware revision, supply conditions, transducer mounting, target geometry, and relevant environmental conditions.
2. Identify each probe location in the private test record and confirm that the probes and instrument are suitable for the signals being measured.
3. Record channel functions, attenuation, time base, voltage scales, trigger settings, and the purpose of the capture.
4. Repeat the observation under controlled conditions and retain the original files.
5. Separate the measured observation from its interpretation and any proposed explanation.
6. Prepare public evidence that supports the conclusion without revealing circuit topology or proprietary parameters.

## Test record template

```text
Test ID:
Date and operator:
Objective:
Hardware / firmware revision:
Setup and environmental conditions:
Target material, dimensions, orientation, and reference position:
Equipment, probe locations, and settings:
Acceptance criterion and source:
Procedure and sample count:
Observed result:
Outcome: Not run / Pass / Fail / Observation only / Inconclusive
Limitations and measurement uncertainty:
Evidence references:
Follow-up action:
```

Use `Pass` or `Fail` only against a defined criterion. Use `Observation only` where behavior is documented without a corresponding acceptance criterion.

## Current limits of the evidence

The reviewed material does not establish calibrated accuracy, operating range, response time, environmental tolerance, electromagnetic compatibility, automotive qualification, or production reliability. Those claims require their own supporting test records.
