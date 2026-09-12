# TOS Lesson Readiness Manifest

This file defines the readiness rule used by the TOS Home dashboard.

## Principle

The dashboard must never start a lesson at zero when TOS can already verify that resources exist.

When TOS creates or verifies a lesson pack, update `readiness.json` for the relevant teaching date/time/class.

## Readiness fields

- `presentation`: true only when the presentation file/deck is verified to exist.
- `worksheet`: true when the required student worksheet/task resources are verified to exist and have passed worksheet QA.
- `notes`: true when teacher notes/answers are verified to exist.
- `teams`: true only when the lesson/resources are verified as uploaded/published in Microsoft Teams. A Teams lesson-plan document alone is not sufficient.
- `forms`: true only when the actual usable Microsoft Form/quiz is verified to exist. A Forms AI prompt or question document alone is not sufficient.

## Manual overrides

The browser dashboard may override any manifest value locally. Manual user changes always take precedence over the manifest for that browser/day.

## Future lesson-build workflow

After creating a lesson pack:
1. Verify the produced files in the canonical Google Drive lesson folder.
2. Update the manifest for presentation, worksheet and teacher notes that genuinely exist.
3. Leave Teams and Forms false until those live actions are independently verified.
4. Never infer readiness merely from a filename that suggests an action was completed.
5. Keep pupil/student information out of the public readiness manifest.

This readiness manifest is supporting state only. Canonical Google Drive lesson files and verified live systems remain authoritative.