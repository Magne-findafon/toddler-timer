# Toddler Visual Timer — Project Brief

## Purpose
A calm, minimal visual timer web page for children aged 2–3. It translates
a clock into something a toddler can see: a parent sets a time, and the
remaining time is shown as a shrinking area of color.
Rule: **less color = less time.**

## Positioning
Made for families who avoid screen time. It should feel like a quiet object
(closer to a lamp or an hourglass) than an app. Nothing to watch, nothing to
play with, nothing to tap.
- Free, no ads, no account, no download. Just a web page.
- Not playful: no characters, no bright colors, no sounds by default.
- Visual only: no numbers, no countdown text, no clock on the timer itself.
  The parent knows the time; the child sees the color.

## Core behavior
- Start screen: preset buttons (e.g. 5, 10, 15, 30 min) + a custom minutes
  input. One tap on a preset starts the timer.
- Running screen: a large solid bar of color takes up most of the screen
  (roughly 80–90%). Its edge moves from left to right, removing color as
  time passes. When time is up, the bar is gone.
- The moving edge pulses gently (soft breathing glow, ~2–3 s cycle) so the
  child can see the timer is alive even on long timers.
- Bar mode only. No circle mode, no invert option.

## End of timer
- Gentle visual ending (slow fade/soft pulse), never flashing.
- Optional soft, short chime (Web Audio, no external files).
  **Muted by default.** Sound toggle on the start screen, remembered in
  localStorage.

## Look
- Calm and plain. Fill: muted sage green (e.g. #7A9A7E).
- Background around the bar: near-black (e.g. #111), so the page isn't a
  bright light in a dark room.
- No text, icons or numbers on the running screen.

## Controls while running
- Hidden by default. A tap shows a small, low-contrast overlay that fades
  after ~3 s.
- Cancel requires a long-press (~1.5 s) so a toddler's tap can't stop it.
- Pause/resume in the overlay.

## Technical requirements
- Single static site: plain HTML/CSS/JS, no build step, no framework.
- Timing based on a fixed end timestamp (Date.now()), redrawn with
  requestAnimationFrame. Must be correct in real time after switching tabs,
  swiping to another app, or locking the phone.
- Screen Wake Lock API to keep the screen on while running; re-acquire on
  visibilitychange. Fail silently if unsupported.
- No fullscreen requirement. Works well in a normal mobile browser tab.
- If sound is turned on, unlock audio on the Start tap (iOS requires a
  user gesture).
- Respect prefers-reduced-motion (disable the pulse).
- Handle rotation and resizing.

## Testing checklist
- iPhone Safari, Android Chrome, iPad, desktop Chrome/Firefox/Safari.
- Screen stays awake for a 30-minute timer.
- Timer is correct after locking the phone or switching apps/tabs.
- Chime plays at the end on iPhone when sound is on.

## Publishing
Host as a static site (GitHub Pages, Netlify or Cloudflare Pages).
Walk me through creating the repo and publishing step by step; I'm new to this.
