# Atlantic Edge Surf School – alpha demo: how to work on this project

## Project

Internal alpha web app for Atlantic Edge Surf School, Lahinch, Co. Clare (Case F).
Owner: Niamh Considine. We are the consultant building it. The solution below
is already agreed with the owner. **Do not add features beyond it.**

## The business

- 6 lesson slots a day in season, up to 12 people per slot, 5 instructors.
- About 1 day in 4 is cancelled due to weather/surf conditions.
- Rebooking is currently done by phone/WhatsApp from a paper diary
  (~3 hours per cancelled day). About 1 in 5 cancelled bookings never rebooks.
- A lesson costs €45 per person.

## Agreed solution: three views

1. **Today** – the day's sessions. One tap cancels a session and moves every
   booking on it to a to-rebook list.
2. **Rebook** – each affected booking (name, group size, contact), with the
   next three sessions that have enough free places for that group. One tap
   moves the booking. A booking not rebooked within 48 hours of its
   cancellation turns red.
3. **Money** – number of bookings waiting to be rebooked and the euro value at
   risk (sum of group sizes × €45).

## Hard constraint: one-handed, wet hands, on the beach

Niamh uses this on her phone on the beach, often with wet hands. The design
itself must show this, not only the wording.

- Works one-handed.
- Large tap targets: minimum ~60px high.
- Main actions within thumb reach at the bottom of the screen.
- Bottom tab bar for the three views.
- High contrast. No small icons.
- No precise gestures: no swipes, no long-presses.
- Cancelling a session asks for confirmation with one big confirm button, so a
  wet-finger mis-tap can't wipe out a session.

## Technical rules

- The whole app is **one file: `index.html`**, with all HTML, CSS and
  JavaScript inside it. No other app files, no frameworks, no build step.
  It must open directly from the github.io link and work on a phone.
- Save all changes in `localStorage` so they survive a page refresh.
- At least 8 sample bookings, generated relative to today's date (sessions for
  the next 14 days, group sizes 1–6), so the demo works whenever it's opened.
- Label the data visibly on screen as **SAMPLE DATA**, and mark the app as an
  **alpha**.
- The case rules must work on the sample data:
  - **Room left:** only suggest sessions with enough free places for the group.
  - **Red:** booking not rebooked 48h after its cancellation.
  - **Amber** (our assumption, not in the case): not rebooked 24h after
    cancellation.
  - **Value at risk:** sum of group sizes waiting × €45.
- Seed data must include cancelled bookings already past 24h and past 48h, so
  amber and red show immediately.
- Include a clearly labelled **"Reset demo data"** button.

## Workflow rules

- After completing each step, suggest a one-line note for `../build-notes.md`
  under the relevant heading, and **wait for approval before writing it**.
- Commit to git after each working step with a clear plain-English message,
  then push.

## Privacy rule (all pages are public on github.io)

- Never put real personal details in any page, README or commit message:
  no student name, student number, email address, college or similar.
- The business, owner (Niamh Considine) and staff are fictional and safe to use.
- Sample customers must be obviously fictional: made-up names, phone numbers in
  the format `087 000 XXXX`, and emails (if any) only at `@example.com`.
- No author credits, "built by" lines or contact details in page footers.
