# LIBRA Lab — Stress-Rest Index (experimental v0.1)

## Purpose
A daily 0–100 orientation estimate intended to help the user observe workload and recovery patterns. It is not a medical measurement, diagnosis, performance prediction, or validated readiness score.

## Inputs used in this first implementation
- Morning sleep duration and quality
- Morning feeling and embouchure condition
- Practice category, duration, intensity, load type, embouchure fatigue and mental fatigue
- Rehearsal / concert / other calendar event duration, intensity and fatigue ratings
- Evening feeling and travel
- Coffee count (small modifier only)
- Workload in the preceding two days (decaying delayed-load modifier)

Missing fields are neutral: they are not treated as zero or as negative evidence.

## Provisional calculation
The first-run baseline is 68. The score is adjusted by simple transparent heuristics:
- Sleep duration: roughly -16 to +5
- Sleep quality: -6 to +4
- Morning feeling: -10 to +7
- Embouchure condition: -7 to +4
- Same-day activity load: capped deduction based on duration, category and intensity
- Fatigue ratings: adjustment around the neutral midpoint 3/5
- Evening feeling and travel: small adjustment
- Prior two days' activity: decaying load deduction
- Coffee above two: small deduction

The exact coefficients are engineering placeholders, not agreed or empirically calibrated weights. They are intentionally exposed here so they can be reviewed and replaced after real data is collected. The initial baseline should not be interpreted as a user-specific measurement.

## Activity weighting assumptions
- Free Playing is lighter than focused repertoire work.
- Warm-up is lighter than intensive repertoire.
- Orchestral excerpts and solo repertoire are provisionally higher load.
- Rehearsal and concert events are weighted by duration and user-selected intensity.
- Concerts have a higher provisional category factor than ordinary rehearsals.
- The next 1–3 days' planned workload is not yet incorporated into this first implementation; it is a required next model revision.

## Validation plan
1. Collect 2–4 weeks of actual entries.
2. Compare index movement with morning embouchure, sleep, subjective condition and actual workload.
3. Review false positives and false negatives with the user.
4. Adjust coefficients transparently; never claim clinical validity.
5. Add future schedule/load only after calendar data is reliable.
