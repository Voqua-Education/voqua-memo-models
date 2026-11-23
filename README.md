# Voqua Memo models

This directory records the provenance of the local AI models used by Voqua Memo.
The distribution repository is https://github.com/Voqua-Education/voqua-memo-models.

- Whisper base multilingual: local transcription in Portuguese, English and Spanish.
- Qwen2.5-1.5B-Instruct Q4_K_M: local language assistance and translation.

Weights are mirrored from their original publishers, with fixed revisions and SHA-256 checksums in `provenance.json`. The app downloads only from a catalog signed by the Voqua distribution key and checks the content hash and size before installation. Inference is local; downloading weights does not upload notes or recordings.

These are small models with limited accuracy. They do not establish facts and should not execute privileged actions. This release was exercised with synthetic audio, translation and memory-retrieval conversations; real-world quality and performance vary by language, microphone and hardware.

Third-party licenses accompany every release. No endorsement by the original model publishers is implied. This repository contains model distribution metadata and assets, not the proprietary application source.
