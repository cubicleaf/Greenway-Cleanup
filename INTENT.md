# Greenway Cleanup — INTENT

**What this file is.** The "why this exists" doc. Not a task list — see [STATUS.md](STATUS.md) for current state and decisions. This file answers: what is this project trying to be, and what does success look like?

---

## Mission

Greenway Cleanup is a community site for Cleveland, TN residents who want to help maintain the local trail system. The job is simple: make it easy to find out when the next cleanup is, sign up to be notified, and show up.

This is not a portfolio piece dressing up a real community need — it is the real community need. The audience is neighbors, not design critics.

---

## What it needs to do

1. **Capture email addresses.** The email list is the only retention mechanism. A visitor who doesn't sign up is gone. The CTA must be the first thing they can interact with.
2. **Work on a phone, outside, in the sun.** The primary use case is someone scanning a QR code off a t-shirt or flyer while standing on the greenway trail. This is a hostile reading environment: bright sunlight, one hand occupied, no patience.
3. **Make the next cleanup legible at a glance.** Date, time, meeting spot. Nothing else matters more than this.

---

## What it is not

- Not a full community platform or forum.
- Not a blog.
- Not a design showpiece (though good design serves the mission).
- Not something that needs to be updated constantly — durability matters more than freshness.

---

## Success looks like

- People show up to cleanups who found the site via QR code.
- The email list grows.
- The site works flawlessly on a phone screen in full sun.

---

## Constraints

- **Deployed on Vercel, GitHub-connected.** No server-side logic beyond Netlify Forms for email capture.
- **Single maintainer.** Updates happen when Tim has time. The site must be low-maintenance by design.
- **Outdoor-first UX** is the guiding constraint for any visual decision (see STATUS.md pivot question).
