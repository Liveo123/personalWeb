# TOS Lesson Readiness Manifest

This file defines the evidence model used by TOS Home. The dashboard is a view of verified state, not an authoritative timetable or a substitute for Google Drive, Microsoft Teams, Microsoft Forms, iSAMS, or other live systems.

## Principle

Absence of evidence means **unknown**, not **not started**.

A lesson is not penalised for a component that is deliberately not required. Readiness is requirements-based rather than a fixed checklist.

## Lesson record

Keys use:

`YYYY-MM-DD|HH:MM|Class`

Recommended fields:

- `pack`: `ready`, `partial`, or `unknown`
  - `ready` means the required teaching artefacts for that lesson have been verified in the canonical lesson folder.
  - `partial` means some required artefacts exist but the pack is not yet complete.
  - `unknown` means no current verification is available.
- `live`: `ready`, `action`, `not_required`, or `unknown`
  - `ready` means every required live/manual action has actually been verified complete.
  - `action` means an artefact is prepared but a manual/live action remains, for example uploading to Teams or creating a Form.
  - `not_required` means no live action is needed for this lesson.
  - `unknown` means the live state has not been verified.
- `next_action`: short human-readable description of the most useful remaining action. Empty when none is known.
- `folder_url`: canonical Google Drive lesson-folder URL when known.
- `source`: short statement of what was verified and when.
- `evidence`: object or short text giving useful evidence without duplicating the whole lesson folder.

## Verification rules

- Google Drive files may prove that a lesson artefact exists.
- Teams is only `ready` after the actual student-facing upload/post/assignment is verified live.
- Forms is only `ready` after the actual usable Form/quiz is verified live.
- A prompt, planned upload, filename, lesson-plan document, or intention is not proof of a live action.
- `not_required` is an intentional design decision, not a failure.
- Never add pupil/student personal information to this public manifest.

## Workflow

After creating or checking a lesson:

1. Verify only what can genuinely be proved.
2. Record the pack status.
3. Record any remaining live/manual action.
4. Add the lesson-folder link when known.
5. Do not manufacture a complete timetable in the manifest.
6. Let the dashboard show unknown state where evidence is absent.

Canonical Google Drive files and verified live systems remain authoritative. Manual dashboard controls must never override evidence by falsely marking an unverified live action complete.
