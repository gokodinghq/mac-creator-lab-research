# Screen Recorder Export Verification Checklist

A short checklist for verifying that what looked correct in the editor is still correct in the exported video.

This is intentionally tool-agnostic. Use the same checks with any recorder or editor, keep timestamps for failures, and preserve the exported file you tested.

## 1. Freeze-frame consistency

Pick 3–5 moments where the frame is visually sensitive: a paused cursor, small interface text, a zoomed region, a transition, or a click animation.

For each moment:

- Compare the editor preview and exported file at the same timestamp.
- Check crop, scale, position, cursor location, and animation state.
- Record the timestamp of any mismatch instead of reducing it to a vague “looks different.”

## 2. Text and UI sharpness

Inspect small interface text at 100% playback size.

- Look for unexpected blur from scaling or re-encoding.
- Check whether thin fonts or icons changed appearance.
- Verify that high-DPI captures were not downscaled more than intended.

## 3. Motion and timing

Use a section with cursor movement, scrolling, or UI animation.

- Check for dropped or duplicated frames.
- Compare animation timing with the preview.
- Look for sudden jumps at edits or zoom boundaries.
- Confirm that cursor and click effects stay synchronized.

## 4. Audio sync

Check the beginning, middle, and end of the exported file.

- Verify microphone/system audio sync against visible events.
- Check for drift on longer recordings.
- Listen around cuts for clicks, gaps, or abrupt level changes.

## 5. Framing and safe area

Inspect the complete frame, not only the subject.

- Verify aspect ratio and output dimensions.
- Check that captions, webcam, cursor, and overlays are not clipped.
- Confirm multi-display or cropped recordings retained the intended region.

## 6. Final-file sanity check

Before publishing:

- Open the exported file in a player outside the editor.
- Scrub through the full timeline once.
- Confirm duration, resolution, and audio tracks.
- Test at least one representative section at normal playback speed.
- If the file will be uploaded to another service, verify one uploaded copy too; platforms may transcode it again.

## Suggested evidence format

| Timestamp | Check | Preview | Export | Result | Notes |
| --- | --- | --- | --- | --- | --- |
| 00:12.500 | Cursor position | expected | expected | Pass | — |
| 00:37.200 | Small UI text | sharp | slightly soft | Review | compare scaling path |

The goal is not to produce a single “quality score.” The useful output is reproducible evidence about where preview and export agree or diverge.

---

**Disclosure:** Mac Creator Lab is run by the team behind ScreenSage Pro. This checklist is a general research method, not an independent ranking or recommendation of ScreenSage Pro.