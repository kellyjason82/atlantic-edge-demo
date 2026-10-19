# Atlantic Edge – rebooking alpha

Internal alpha web app for Atlantic Edge Surf School, Lahinch, Co. Clare
(fictional case study, Case F). It helps the owner rebook lessons cancelled
because of weather, one-handed on a phone on the beach.

**Live demo:** https://kellyjason82.github.io/atlantic-edge-demo/

All names and phone numbers are **SAMPLE DATA** and invented.

## The three views

- **Today** – the day's six sessions. Tap "Cancel session", then confirm with
  the big button: every booking moves to the Rebook list.
- **Rebook** – each waiting booking with a call button and the next three
  sessions that have room for the whole group. One tap moves it.
  Amber after 24 hours waiting (our assumption), red after 48 hours (case rule).
- **Money** – bookings and people waiting, and the euro value at risk
  (people waiting × €45).

## Designed for wet hands

Bottom tab bar, every button at least 64px high, main actions low on the
screen, high contrast, text labels as well as colours, plain taps only (no
swipes or long-presses), and a big confirm before any session is cancelled.

## How to open

Open the live link on a phone, or open `index.html` in any browser. It is one
file with no install or build step.

- Changes are saved in the browser (localStorage) and survive a refresh.
- **Reset demo data** (bottom of Money) rebuilds the sample data from today's
  date, including bookings already waiting over 24h and 48h.
- Demo aid: once all of today's lessons have started (after 16:30), Today shows
  tomorrow's sessions under a labelled banner, so there is always something to
  cancel.

## What this alpha does not do

No real bookings, logins, payments, or SMS/WhatsApp messages, and data is
stored only on the device that opened it.
