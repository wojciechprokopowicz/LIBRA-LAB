# LIBRA Lab v13 — Check-ins & Practice Log

Flat upload package: six files in repository root, no assets folder.

## Changes
- Morning Check-in now records exact sleep duration from 3 to 12 hours in 30-minute increments.
- Evening Check-in now uses a 1–5 slider with clear condition labels and descriptions.
- Removed Physical Activity and Activity Type from Evening Check-in.
- Nap has an optional duration field; Travel remains a Yes/No context field and does not directly change the index.
- Index now reads exact sleep minutes while remaining compatible with older saved sleep-duration labels.
- Evening condition contributes proportionally using the 1–5 rating.
- Practice Log stays open after saving a session.
- Added a save confirmation and Today's Practice list with total duration and fatigue ratings.
- Form controls use 16px text to prevent iOS Safari automatic input zoom.
- Existing local database key is unchanged.

## Install
Back up your records first. Replace the six files in the root of `LIBRA-LAB` on branch `main`. Keep Pages on `main` / root. Open once with `?v=13`.
