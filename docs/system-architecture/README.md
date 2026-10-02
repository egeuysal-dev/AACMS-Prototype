# System Architecture

AACMS Prototype combines an interactive interface with a local synthetic computation workflow. The Windows shell hosts the engineering and MFD views; both views consume the same trace and share playback controls.

```mermaid
flowchart TB
    User[User] --> Shell[Windows Application]
    Shell --> UI[Engineering and MFD Interface]
    UI --> Input[Seed and Local Run Request]
    Input --> Runtime[Local Synthetic Computation]
    Runtime --> Trace[Generated Research Trace]
    Recorded[Recorded Scenario Traces] --> Adapter[Trace Adapter]
    Imported[Compatible JSON Trace] --> Adapter
    Trace --> Adapter
    Adapter --> UI
    UI --> Audio[Audio Playback and Preview]
```

## Computation workflow

Synthetic scenario → simulation → RWR observation → feature extraction → model inference → generated trace → AACMS interface.

The packaged inference resources are used locally. Training, model development, and dataset production are outside this distribution. The application has no connection to real aircraft sensors and does not execute aircraft countermeasures.

## Output interpretation

Recorded research output, presentation scenarios, and new local runs retain their respective meanings. Model probabilities are not treated as validated operational threat levels or countermeasure recommendations. Missing observations and unavailable assessments remain visible.

[Return to AACMS Prototype](../../README.md)
