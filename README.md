# fasal doctor

A crop doctor that tells a farmer the dose, not just the disease, and then checks whether the spray worked.

Built for the Meta Global AI Developer Hackathon (Cerebral Valley, Oct 26 - Nov 4, 2026).

## The problem

Crop diagnosis apps name a disease from a photo, but the farmer still has to guess how much to spray. Surveys of Indian vegetable growers report widespread overdosing and pesticide labels farmers can't read. The diagnosis apps we checked don't re-measure the same leaves to tell the farmer whether to spray again.

## What it does

1. The farmer sends a leaf photo and a voice note in their own language (Hindi, Bengali, Tamil, Telugu, Marathi or Kannada).
2. SAM 3.1 masks every lesion and measures the affected leaf area.
3. Muse Spark turns that measurement into a severity level, reads a photo of the pesticide label, and works out a dose per acre.
4. On day 3 to 5 the farmer re-photographs the same leaves. The masks are compared, and the answer is spreading, stable or shrinking, so the farmer knows whether a second spray is needed.

## Meta models

- SAM 3.1 for lesion segmentation and area measurement
- Muse Spark for severity, label reading, dose reasoning and the follow-up comparison
- Meta voice transcription for the farmer's spoken question

## Inference

Muse Spark runs on Baseten (Muse Spark Open).

## Status

Hackathon build starts Oct 26, 2026.
