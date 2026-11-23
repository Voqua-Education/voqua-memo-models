# Voqua Memo models

This directory records the provenance of the local AI models used by Voqua Memo.
The distribution repository is https://github.com/Voqua-Education/voqua-memo-models.

- Whisper base multilingual: local transcription in Portuguese, English and Spanish.
- Qwen2.5-1.5B-Instruct Q4_K_M: local language assistance and translation.
- Kokoro 1.0 FP32: offline speech, with female/male voices in Brazilian Portuguese, British English and Spanish.
- `voices.vqkv`: six original Kokoro voice embeddings, repacked without quantization or training. Fixed little-endian container; no pickle or archive extraction at runtime.

Weights are mirrored from their original publishers, with fixed revisions and SHA-256 checksums in `provenance.json`. The app downloads only from a catalog signed by the Voqua distribution key and checks the content hash and size before installation. Inference is local; downloading weights does not upload notes or recordings.

These are small models with limited accuracy. They do not establish facts and should not execute privileged actions. This release was exercised with synthetic audio, translation and memory-retrieval conversations; real-world quality and performance vary by language, microphone and hardware.

Third-party licenses accompany every release. No endorsement by the original model publishers is implied. This repository contains model distribution metadata and assets, not the proprietary application source.

The voice-capable app reads `catalog-v2.json` (serial 2). The original `catalog.json` remains available for older builds. Existing Whisper and Qwen assets retain their original immutable URLs. Voice weights come from the pinned kokoro-onnx `model-files-v1.1` release; the original model and voices are Apache-2.0. Native inference and phonemization components are packaged separately with their licenses in the app, not downloaded as executable updates through this model catalog.
