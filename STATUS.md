---
attention: Reference
state: Live
form: Website
updated: 2026-07-20
live_url: https://greenwaycleanup.vercel.app
---

# Greenway Cleanup — STATUS

**What this file is.** A running record of where this project stands and what decisions have been made about it. Reference [INTENT.md](INTENT.md) for what the project is trying to be.

**How to use it.** When something changes — a fix ships, a decision lands, the site gets an email blast — add a dated entry. Keep it honest. If the project is dormant, say so.

Last updated: 2026-07-20

---

## Decisions

### 2026-07-20 — First Netlify list message sent
**What:** Sent the first test message to the Netlify Forms signup list through Gmail/BCC using the captured form submissions.
**Why:** This proved the operational loop: signup form captures entries, Netlify exposes the list, and Tim can message the group when cleanup details exist.
**Rejected:** Adding an email-list product before there is a real audience size that needs unsubscribe/deliverability tooling.
**How to apply:** For small lists, export/copy Netlify submission emails and send via BCC. If the list grows beyond a small handful of real people, move to a lightweight email-list tool.
**Evidence strength:** Tim-directed.

### 2026-07-20 — Outdoor-first visual direction chosen; light mode is default
**What:** Resolved the outdoor/indoor pivot by making light mode the no-preference default on both `index.html` and `success.html`, while preserving the manual dark-mode toggle and any saved dark preference.
**Why:** The project's core use case is QR-to-phone signup for people who may be standing outside near the Greenway. Daylight readability and fast comprehension should win for first-time visitors; the dark loam version remains available for people who prefer the atmospheric indoor read.
**Rejected:** Removing dark mode or redesigning the light palette in this pass.
**How to apply:** Treat Greenway as outdoor-first by default. Future deeper design work can still tune light mode, but should not return the first-visit default to dark unless the real usage context changes.
**Evidence strength:** Tim-directed.

### 2026-07-20 — Signup and field-note overlays now contain keyboard focus
**What:** Added deliberate focus trapping for the main `Get Involved` signup modal and its nested field-note overlay in `index.html`. Tab/Shift+Tab now stay inside the active overlay, Escape still closes the topmost overlay first, and focus returns to the invoking control after close.
**Why:** The audit flagged missing focus containment as the remaining keyboard-accessibility risk. This changes keyboard behavior, so it was handled separately from the low-risk markup/CSS polish.
**Rejected:** A broader redesign of the modal flow; the signup form, Netlify submission path, and visual treatment are unchanged.
**How to apply:** Reuse the same active-overlay stack pattern if more nested notes or modals are added.
**Evidence strength:** Claude-suggested, Tim-approved.

### 2026-07-20 — Low-risk audit polish landed; stale CTA-delay open item cleared
**What:** Applied the safest remaining audit fixes: `index.html` and `success.html` now use `<main>` landmarks plus keyboard-visible skip links, `100svh` viewport fallbacks, and broad reduced-motion handling; the hero CTA and signup modal close control are explicitly 44px minimum touch targets; the hidden Netlify honeypot is hidden from assistive tech and removed from tab order; the success page copy now opens with "Welcome to the Greenway crew." The old Back Burner item to fix the April CTA-delay P0 was removed because later July work already replaced that pre-audit failure mode with a deliberate, documented CTA entrance treatment.
**Why:** These fixes improve accessibility and mobile robustness without changing the visual direction or signup flow. Removing the stale CTA item prevents future sessions from treating a resolved April audit issue as current work.
**Rejected:** A broader modal focus-trap rewrite in this pass; that touches keyboard behavior and should be handled deliberately rather than bundled into low-hanging CSS/markup cleanup.
**How to apply:** Keep the landmark/skip-link/reduced-motion baseline on both pages. Treat the current CTA timing as the July design direction unless Tim explicitly reopens the outdoor-first speed tradeoff.
**Evidence strength:** Claude-suggested, Tim-approved.

### 2026-07-14 — Dark-mode hero CTA switched to Warm Parchment mockup direction
**What:** The dark-mode `Get Involved` button now uses the selected Warm Parchment treatment from the mockup pass: parchment-tan fill (`#B8A07E`), dark text (`#2E241A`), no border, and a softer grounded shadow. Light mode was left alone.
**Why:** Tim chose mockup option 2 after reviewing the visual comparison and wanted the dark CTA to read warmer and clearer without changing the day version.
**How to apply:** When a mockup direction is selected, implement it mode-specifically if the other mode has already been tuned separately. Do not collapse light and dark into one compromise token set.

### 2026-07-13 — Hero CTA reduced another 15% in physical size
**What:** The main `Get Involved` button was reduced another ~15% by tightening its padding, minimum height, and squircle radius while keeping the larger label size from the previous pass.
**Why:** Tim wanted the button to occupy less physical space without losing its typographic presence.
**How to apply:** If this CTA needs more emphasis, prefer larger type before restoring a bulkier shell.

### 2026-07-13 — Hero CTA hover behavior now matches the modal submit check
**What:** The main `Get Involved` button no longer uses its older brighter/lifted hover treatment; it now uses the same subtle hover response as the modal submit check, including the gentler lift and brightness shift.
**Why:** The page had two different interaction languages for its two primary calls to action, which made the hero button feel disconnected from the modal system it opens.
**How to apply:** If the hero CTA and modal submit belong to one flow, keep their hover and focus behavior aligned unless there is a deliberate reason to differentiate them.

### 2026-07-13 — Modal palette softened again; submit/check and logo outline brought back into line
**What:** The modal ink system was lightened so the field labels, input text, and borders read more clearly without going back to stark white. The submit check-shell was thinned back to the same stroke weight as the close/help icons, and the hero logo outline was both warmed away from light green and reduced to an even thinner parchment-toned stroke.
**Why:** The previous pass fixed coherence but overshot in two places: the submit check became heavier than the rest of the icon family, and the logo outline still felt too present while also carrying the wrong hue.
**How to apply:** Keep related elements in the same color family, not identical values. Match icon stroke weight across the SVG controls unless there is a deliberate reason to break rank.

### 2026-07-13 — Signup modal pulled into one muted ink system; hero CTA tightened again
**What:** The `Get Involved` modal now uses one toned-back dusty tan for its submit check, close/help icons, headings, labels, borders, input text, placeholders, and helper copy instead of mixing bright white text with cooler gray borders. The hero CTA was also tightened down in physical size while its label was enlarged, and the hero logo outline was reduced back to the same stroke weight as the modal close icon.
**Why:** The modal had stopped feeling coherent; its parts belonged to different color systems. Separately, the hero CTA wanted denser typography without occupying as much space, and the logo border had become too heavy.
**How to apply:** For this site, treat the modal as a single warm-ink surface: one dominant ink color with opacity shifts, not separate white, gray, and amber systems fighting each other.

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
Resolved 2026-07-20: outdoor-first default with dark mode preserved as an alternate.

### 2026-04-27 — Canonical folder settled
Single canonical folder: `Greenway-Cleanup/` at Documents root (GitHub-connected, Vercel-deployed). Former `webdev/projects/Greenway Cleanup/` scratch copy deleted 2026-05-17.

### 2026-04-16 — Email capture via Netlify Forms
Netlify Forms wired for email collection. Real list exists. First test message sent 2026-07-20.

---

## Back Burner

No active Greenway open items.
