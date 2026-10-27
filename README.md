# Real-Time ASL Letter Recognition Prototype

A Python webcam demo that runs a saved TensorFlow/Keras image model on a hand region and displays a predicted ASL alphabet class. The script includes a short history-based stabilizer and can send eligible stable letter predictions to a separate text-to-speech process.

## Requirements

Install the packages listed in `requirements.txt`. The script expects a webcam available as camera device `0` and a model file named `asl_image_model.keras` in the current working directory. That model file is not included in this repository; provide a compatible trained model before running the application.

## Run

```bash
python asl_translator.py
```

Press `q` in the OpenCV window to exit. The configured output classes are `A` through `Z`, `del`, `nothing`, and `space`; speech is queued for eligible letter predictions only.

## Scope and limitations

This is an experimental webcam application, not a complete sign-language translator. Its output depends on the external model, its training data, camera framing, and lighting. It recognizes isolated configured classes and does not interpret continuous signed language, grammar, or sentence meaning. Confidence thresholds and frame smoothing are heuristics, not accuracy guarantees.
