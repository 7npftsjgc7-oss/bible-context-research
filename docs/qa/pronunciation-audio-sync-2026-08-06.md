# Pronunciation and Audio Synchronization QA

Date: 2026-08-06  
Release target: `v0.2.0`  
Repository: `7npftsjgc7-oss/bible-context-research`

## Scope

This report records verification of the pronunciation and audio behavior added in PR #3 and documented in PR #4.

Authoritative commits before this release preparation:

- `35ebb9850d25efde28c04af0abd70b1e97b1b9c6` — pronunciation and audio behavior specification
- `616e596bedb2d53d0d55eaed8dcb20dec046ebcc` — README documentation

The passages and terms used for these checks were development tests, not personal Bible-reading progress.

## Evidence levels

- **Directly verified:** inspected in the merged GitHub repository.
- **User-confirmed:** the user reported completing and passing the manual update or test; the exact output artifact was not preserved in the repository.
- **Not tested:** no completed test was reported.

## Results

| Area | Behavior or instruction checked | Result | Evidence |
|---|---|---|---|
| Repository wiring | `source-policy.md` loads `pronunciation-audio.md` when original-language pronunciation or audio is involved | Pass | Directly verified |
| Pronunciation specification | Hebrew, Aramaic, and Greek rules distinguish written guidance, verified BLB links, native controls, and generated audio | Pass | Directly verified |
| BLB requirement | Native or generated audio does not replace the verified Blue Letter Bible Strong's entry | Pass | Directly verified |
| Multiword and inflected forms | Strong's links remain lexical; phrases are not assigned one unsupported Strong's number | Pass | Directly verified |
| Divine name | יהוה is preserved as `YHWH` and distinguished from the traditional reading `Adonai` | Pass | Directly verified |
| Installed skill | Added `references/pronunciation-audio.md` and updated the `source-policy.md` loader | Pass | User-confirmed |
| Three Bible-study projects | Shared project instructions and downstream pronunciation reference were installed and tested | Pass | User-confirmed |
| Custom GPT | Current configured instructions were compared with the merged repository, revised under the character limit, installed, and tested | Pass | User-confirmed |
| Hebrew phrase test | Multiword handling and the יהוה/`Adonai` distinction were tested | Pass | User-confirmed; output not archived |
| Greek term test | A Greek pronunciation case with convention identification was tested | Pass | User-confirmed; output not archived |
| Uncertain mapping test | The system was tested not to invent a lemma, Strong's number, pronunciation, or BLB URL | Pass | User-confirmed; output not archived |
| Native inline control | Control use remains conditional on actual environment support | Pass at instruction level | Runtime rendering evidence not archived |
| Synthetic audio | ElevenLabs or another external generated-audio integration | Not tested | No completed integration test reported |

## Regression review

No regression was reported in source hierarchy, denominational neutrality, uncertainty handling, menus, shorthand behavior, BLB-link requirements, or reading-progress separation.

No corrective repository change is required from the reported test results.

## Remaining limitations

- The repository has no automated test workflow for this behavior.
- Native inline pronunciation controls are environment-dependent and cannot be guaranteed by skill instructions alone.
- Manual downstream copies do not update automatically after repository changes.
- Synthetic pronunciation audio remains unverified until a specific integration is configured and tested.

## Future retest triggers

Repeat the relevant tests after changes to `SKILL.md`, `source-policy.md`, `pronunciation-audio.md`, the installed skill, Custom GPT instructions, project instructions, BLB URL behavior, or the ChatGPT pronunciation-control interface.
