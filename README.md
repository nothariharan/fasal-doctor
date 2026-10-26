# fasal doctor

A crop doctor that tells Indian vegetable farmers whether to spray again, by re-measuring the damage on the same leaves and checking the bottle label's dose before they spray.

Built for the Meta Global AI Developer Hackathon (Cerebral Valley, Oct 26 - Nov 4, 2026).

## The problem

Crop diagnosis apps name a disease from a photo, but the farmer still has to guess how much to spray. Surveys of Indian vegetable growers report widespread overdosing and pesticide labels farmers can't read. The diagnosis apps we checked don't re-measure the same leaves to tell the farmer whether to spray again.

## What it does

1. The farmer sends a leaf photo next to a printed scale card and a voice note in their own language (Hindi, Tamil, Telugu or Marathi).
2. SAM 3.1 masks every lesion and measures the affected leaf area.
3. Muse Spark reads the pesticide label photo for its dose and spray interval and flags any mix above it. It never computes a dose of its own.
4. On day 3 to 5 the farmer re-photographs the same leaves. The masks are compared, and the answer is spreading, stable or shrinking, so the farmer knows whether a second spray is needed.

## Meta models

- SAM 3.1 for lesion segmentation and area measurement
- Muse Spark for label reading and the spray-or-wait comparison
- Meta voice transcription for the farmer's spoken question

## Inference

Muse Spark Open runs on Baseten or Fireworks, with hosted Spark 1.3 as the fallback. SAM 3.1 open weights run on a Modal GPU endpoint, with the Meta Model API as the fallback.

## Status

Hackathon build starts Oct 26, 2026.

