# Greenway Cleanup — STATUS

**What this file is.** A running record of where this project stands and what decisions have been made about it. Reference [INTENT.md](INTENT.md) for what the project is trying to be.

**How to use it.** When something changes — a fix ships, a decision lands, the site gets an email blast — add a dated entry. Keep it honest. If the project is dormant, say so.

Last updated: 2026-07-13

---

## Decisions

### 2026-07-13 — Control stroke weights normalized across the modal and hero badge
**What:** The five signup fields now use thicker squircle borders, the modal submit check was scaled down and redrawn with a heavier stroke, and the hero logo badge switched from a circle to the same squircle shell with a thicker outer outline.
**Why:** The UI had drifted into mixed line weights and mixed geometry, which made the controls feel assembled from different passes instead of belonging to one system.
**How to apply:** When reusing the squircle language, keep both the silhouette and stroke weight consistent across buttons, fields, and badge shells rather than matching only one of those traits.

### 2026-07-13 — Hero CTA now shares the squircle button language
**What:** The main hero `Get Involved` button was reshaped from a rounded pill into an asymmetric squircle so it matches the rest of the updated SVG/button system.
**Why:** The hero CTA was lagging behind the newer visual language and still read like an older generic button.
**How to apply:** If the site uses custom organic controls elsewhere, keep the hero CTA in the same family instead of leaving it as a default pill.

### 2026-07-13 — Modal icon controls simplified and the light-mode field note recolored
**What:** The signup modal title no longer carries the edit-pen icon, the submit action is now just the enlarged check-shell SVG without a surrounding pill button, the day-mode field note was recolored to use darker earth-tone text instead of green, and the top-right theme toggle now uses a larger sun/moon icon inside the same squircle-shell language.
**Why:** The prior pass still looked overdesigned in the wrong places: the pen icon muddied the title, the submit action felt nested inside another button, the day field note title was hard to read, and the mode toggle icons were undersized.
**How to apply:** Keep the SVG family as the visual language, but let each icon stand on its own job. Do not add extra decorative shells around controls that already carry their own shape.

### 2026-07-13 — Modal form-shell cleanup after the first SVG pass
**What:** The signup fields were pulled back from the literal stretched-SVG shell treatment and rebuilt as restrained check-shell-inspired squircles with clean borders, native controls, and no pen icons inside the fields.
**Why:** The first pass produced distorted inner ovals and visual clutter. The cleanup keeps the custom spirit without wrecking legibility.
**How to apply:** When borrowing a compact icon shape for larger UI, translate the character of the shape instead of stretching the original geometry until it breaks.

### 2026-07-13 — Signup modal icon and form-field visual system redesigned
**What:** The signup modal now uses the supplied SVG family for close, sun, moon, edit, and submit controls. Form inputs visually adopt the check SVG's squircle shell without the center checkmark, the submit button is narrower and icon-only, and the modal heading/subtitle were enlarged and rewrapped.
**Why:** Tim wanted the modal to feel more elegant, more custom, and more consistent with the new field-note icon language, even if the input-box treatment is intentionally unconventional.
**How to apply:** Keep the actual form controls native for accessibility and Netlify submission, but use SVG-backed styling to carry the squircle visual language.

### 2026-07-13 — Added field note system inside the signup modal
**What:** The `Get Involved` modal now includes a top-left `(?)` field-note trigger mirrored against the close button, plus a shared explanatory note overlay backed by a small note registry.
**Why:** Tim wanted an in-modal explanation of what the group actually does without cluttering the main signup copy.
**How to apply:** Future explanatory notes should reuse the same registry + overlay pattern, keep headings phrased as the user's question, and stay within the field-note copy budget.

### 2026-07-13 — Light-mode CTA text color switched to warmer Option 2
**What:** The day-mode `Get Involved` label was changed from the previous earthy text color to the softer warmer Option 2 selection. Dark mode was left alone.
**Why:** Tim preferred the warmer tone and explicitly liked the existing dark-mode treatment.
**How to apply:** Treat hero CTA label color as mode-specific if needed; light and dark do not have to share the exact same text color.

### 2026-07-13 — Hero footer location line removed
**What:** The bottom-of-hero `Cleveland Greenway Cleanup · Cleveland, TN` footer line was removed.
**Why:** Tim did not want the redundant location/title line lingering at the bottom of the screen.
**How to apply:** Keep the hero cleaner by relying on the main title and badge only unless a future version needs explicit footer metadata again.

### 2026-07-13 — Hero CTA label warmed and enlarged again
**What:** The `Get Involved` label was moved off pure white into the site's earthy cream-dark text color and enlarged another 40%.
**Why:** Tim wanted the CTA typography to feel integrated with the surrounding palette and to read much larger at a glance.
**How to apply:** Favor warm earth-tone text on the hero CTA over stark white unless a future contrast pass intentionally changes the whole button color system.

### 2026-07-13 — Button font switched to slab-serif option; hero tagline enlarged
**What:** The `Get Involved` button adopted the selected Option 5 font direction using a slab-like serif treatment, with the button label increased by 15%. `Just show up.` was also enlarged by 20%.
**Why:** Tim preferred the more distinctive button type treatment and wanted both the CTA label and hero tagline to read with more presence.
**How to apply:** Treat the hero CTA font as its own typographic accent rather than inheriting the sitewide sans by default.

### 2026-07-13 — Hero CTA now enters later, slower, with overshoot
**What:** The `Get Involved` button entrance was retuned independently from the rest of the hero sequence: it now waits an extra 1 second, runs 50% slower than its prior timing, and scales slightly past full size before settling.
**Why:** Tim wanted the CTA to feel more deliberate and animated, not just delayed.
**How to apply:** Keep the CTA on its own entrance timing track unless the full hero sequence is intentionally rebalanced again.

### 2026-07-13 — Hero CTA shifted toward a squircle shape and earlier entrance
**What:** The `Get Involved` button was changed from a pill to a softer squircle radius, moved 10px upward, and its custom entrance delay was reduced by 0.3 seconds.
**Why:** Tim wanted the CTA to feel a little tighter and arrive a little sooner without losing the overshoot treatment.
**How to apply:** Treat the CTA as a distinct shape/timing exception from the other buttons unless the button system is intentionally unified later.

### 2026-07-13 — Day-mode tagline darkened; hero CTA raised another 5px
**What:** In light mode, `Just show up.` was darkened for better readability, and the `Get Involved` button was moved up another 5px.
**Why:** The day version tagline was washing out, and the CTA still wanted a slightly tighter vertical placement.
**How to apply:** Keep the darker light-mode tagline as a readability exception; dark mode remains unchanged.

### 2026-07-13 — Entrance animations slowed by 50% across the site
**What:** The staged entrance animations on the main page and success page were slowed by 50%, including both animation duration and stagger delay.
**Why:** Tim wanted the page to feel less rushed while keeping the existing entrance order and behavior.
**How to apply:** Treat 0.75s fades and 1.5x stagger delays as the current baseline unless a future pass intentionally retunes the full entrance sequence.

### 2026-07-12 — QR vinyl for t-shirt completed
**What:** The QR vinyl/t-shirt physical follow-through is done.
**Why:** It was still listed as open work, which would misstate the current state of the project.
**How to apply:** Remove it from open items. The remaining deferred items are digital: email blast, CTA timing, and the outdoor/indoor visual-direction decision.

### 2026-07-12 — GWC reclassified Reference (done & live), not Parked; excluded from the going-cold radar
**What:** Tim's call, refined: this isn't "Parked." Parked = deprioritized/on-ice (might resume, serving no one now, e.g. Exhibit Eclectic). GWC is **Reference × Live** — finished, deployed, and anyone can visit and use it tomorrow; it's simply not being actively developed. Outstanding items (the P0 CTA-animation delay, the outdoor/indoor pivot, the never-sent email blast) are real but minor and deferred by choice.
**Why:** It kept hitting the Morning Brief "Going Cold" list because the radar keys off `stage: active/building`, and a finished-but-live project has no honest value in the 5-stage enum. That's a genuine gap in the system, not a GWC problem — "going cold" should only watch things you're *driving*, not things that are done and live.
**How to apply:** Systemic fix applied today — added a Reference-exclude to `Master-Reader/routines/Hearth Routine Instructions.md` Step 4 so `greenway-cleanup` (and `zoomer-slang`) stop being radar'd, no registry edit needed. Durable fix is the two-axis migration: once `relationship: Driving/Parked/Reference` exists, gate the radar on `relationship: Driving` and delete the hand-list. Keep the P0 recorded here; deferred ≠ done.

### 2026-06-24 — Docs initialized
STATUS.md and INTENT.md created as part of a Marius documentation pass. Sourced from marius-data.js registry + April 2026 audit.

### 2026-04-29 — P0 identified: CTA animation delayed to ~2.8s
Three-agent audit confirmed the hero animation cascade is holding the primary CTA off-screen for ~2.8 seconds on load. Fix: reduce animation delay to 0.3s. This is the highest-priority open issue.
**Why it matters:** The QR-on-trail use case means users are standing outside, in the sun, with one hand occupied. A 2.8s wait before the CTA appears costs sign-ups.

### 2026-04-29 — Pivot question: outdoor vs. indoor aesthetic — unresolved
The audit surfaced a real tension: dark loam background looks intentional indoors but fails in sunlight (glare mirror). Three honest paths: (1) commit to outdoor — light bg, dark text, fast paint; (2) commit to indoor — accept QR trail use is rare, optimize browse; (3) both — `prefers-color-scheme` + manual toggle. No decision made yet.
**How to apply:** Any visual changes to the site should acknowledge this choice first. Don't add to either end without picking a lane.

### 2026-04-27 — Canonical folder settled
Single canonical folder: `Greenway-Cleanup/` at Documents root (GitHub-connected, Vercel-deployed). Former `webdev/projects/Greenway Cleanup/` scratch copy deleted 2026-05-17.

### 2026-04-16 — Email capture via Netlify Forms
Netlify Forms wired for email collection. Real list exists. No email has been sent to the list yet.

---

## Ideas / Backlog

- Send one message to the email list — the list exists, use it
- Fix P0 CTA animation before any other visual changes
- Decide the outdoor/indoor pivot before committing to deeper design work
