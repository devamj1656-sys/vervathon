# Vocalytics — AI Speech Evaluation System

Vocalytics is a college-level project concept for making spoken-performance evaluation more consistent and actionable. It targets formats such as persuasive oratory, declamation, interpretive reading, and extemporaneous speaking.

## Current status

This repository currently contains a **front-end prototype**. It allows a user to select a local audio recording, enter a transcript, choose a performance type, and view simple transcript/audio metadata.

**Important:** The current prototype does not run AI speech recognition, reference-speech comparison, temporal flaw detection, or automated rubric scoring. Feedback is illustrative and must not be presented as validated AI evaluation.

## Run locally

No build tools or dependencies are required for the demo.

1. Clone or download this repository.
2. Open `index.html` in a modern browser.
3. Select an audio file and optionally paste its transcript.
4. Choose the speech category and click **Generate demo report**.

For local hosting, you can also run:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000.

## Proposed future architecture

- **Audio ingestion:** Validate and normalize user-provided audio.
- **Speech-to-text:** Integrate a speech recognition model such as Whisper.
- **Time alignment:** Align transcript words/phrases to timestamps with a forced-alignment tool.
- **Acoustic features:** Explore speech rate, pause duration, pitch variation, intensity, and MFCC features using Python tools such as librosa, NumPy, and SciPy.
- **Temporal observations:** Identify candidate hesitation, unusually long pauses, rushed sections, and possible emphasis mismatches, with clear uncertainty indicators.
- **Rubric dashboard:** Show explainable, time-stamped observations and practice suggestions for each speaking category.
- **Contrastive evaluation:** Build a consented, labelled dataset of stronger and weaker examples, with a documented rubric and human-review process.

## Suggested project milestones

1. Agree on a transparent evaluation rubric with faculty or speech coaches.
2. Collect and label audio only with informed consent.
3. Build and evaluate transcription and word-level alignment.
4. Implement acoustic feature extraction and compare it with human annotations.
5. Add explainable dashboard visualizations and evaluate feedback quality.
6. Test for reliability, accent variation, noise sensitivity, and fairness before making performance claims.

## Privacy and responsible use

- Get explicit consent before recording or analyzing a person's voice.
- Explain how recordings and transcripts will be stored and used.
- Avoid using automated scores as the sole basis for judging people.
- Report uncertainty and limitations; accents, microphones, background noise, and speaking styles can affect measurements.
- Do not upload sensitive recordings to third-party services without informed consent.

## Repository contents

- `index.html` — responsive, self-contained browser prototype.

## License

No license has been specified yet. Add a license file before inviting external reuse.
