# JalRaksha — Village Water Watch

A village board that shows every hand pump, well, tap and RO plant nearby — working, broken, or not safe to drink — kept up to date by the villagers themselves.

Built for the **Xylem Global Student Innovation Challenge 2026**, Challenge #3: Water Access.

## How to run it

No install, no build step. Pick any one:

1. **Just open the file** — double-click `index.html`, or open it in any phone or computer browser. It works straight from the file.
2. **Local server** (optional):
   ```
   cd xylem-jalraksha
   python3 -m http.server 8000
   ```
   Then open http://localhost:8000 in a browser.
3. **Any static host** — upload `index.html` to GitHub Pages, Netlify, Vercel or any static hosting. It is a single file; there is nothing else to deploy.

**Voice reporting** uses the browser's built-in speech service (Web Speech API). It works in Chrome on Android and desktop. On browsers without it, the app says so plainly and the tap buttons do the same job. Allow the mic when the browser asks.

## What is in the app

- **Water-point board** — a simple village map plus a list of 12 water points for one pilot village (Rampur, Uttar Pradesh). Each point shows its status — Working, Broken, or Not safe to drink — and how many families use it.
- **One-tap reporting** — tap a point, then tap one big button: Working, Broken, or Not safe. No typing, no form.
- **Voice reporting** — hold nothing, fill nothing. Tap the voice button and speak in Hindi ("ye pump kharab hai", "paani ganda hai", "theek chal raha hai"). The app understands and sets the status. If the phone has no voice support, it falls back to the buttons.
- **Flood Mode** — one switch. Open and low-lying points that may have flood water mixed in turn to "Check before drinking", safe points are marked SAFE and rise to the top of the list, and a short safe-water guide appears in Hindi and English (boil, chlorine tablet, what to avoid during floods).
- **Panchayat Repair List** — broken and unsafe points ranked by how many families use them, so the panchayat knows what to fix first and how many people each repair helps. A point leaves the list when someone marks it fixed.
- **Recent reports** — who reported what, and when.

The village data is sample data for one pilot village, labelled as such in the app. Names, family counts and problems are the kind a real village board would hold.

## Xylem submission text

**Project name:** JalRaksha — Village Water Watch

**Challenge:** #3 — Water Access

### The problem

In our villages in Uttar Pradesh, water comes from hand pumps, wells, tap stands and one RO plant. Pumps break often. In the monsoon, flood water gets into open wells and the water turns unsafe. But nobody in the village knows, at any given time, which points are working and which are not. A family walks to a pump, finds it broken, then walks to a well that may not be safe. The panchayat also does not know which broken pump matters most, so repairs happen late and in the wrong order. The information exists — everyone knows their own pump — but it sits in separate heads, not in one place the whole village can see.

### The solution

JalRaksha is one shared board for the village's water points. Every hand pump, well, tap stand, pond and RO plant is on it, with a clear status: working, broken, or not safe to drink.

Anyone can update a point with one tap. People who cannot type can press the voice button and just speak in Hindi — "ye pump kharab hai" — and the board updates. When floods come, one Flood Mode switch marks every open, low-lying point as "check before drinking", brings the safe points to the top, and shows a short guide in Hindi and English on how to make water safe.

The panchayat gets a repair list that ranks broken points by the number of families who use them. Fix first the pump that serves 70 families, not the one that serves 20. That order was guesswork before; now it is written down.

It needs no new pipes and no costly machines. It runs on the phones already in the village, and on any computer.

### How it fits Challenge #3 — Water Access

The challenge asks for better reliable, equitable and resilient access to water, against physical, economic, environmental and infrastructure barriers. JalRaksha answers each word plainly:

- **Infrastructure barrier** — a broken hand pump is useless until someone reports it and it gets fixed. JalRaksha makes reporting take one tap, and puts repairs in the order that helps the most people.
- **Environmental barrier** — floods quietly make open wells unsafe. Flood Mode names that risk the day the water rises, and points people to safe water.
- **Equitable access** — voice reporting in Hindi means a person who cannot read or type can still keep the board true. The board belongs to everyone, not only to those with smartphones and English.
- **Reliable and resilient** — the village always knows where its working water is, in normal weeks and in flood weeks alike.

### Tech

- One single web page: plain HTML, CSS and JavaScript in one file (`index.html`). No build step, no server, no database, no cost to run. It opens from a file or any free static host.
- Voice reports use the Web Speech API built into the browser, set to Hindi (hi-IN), with a plain fallback message and tap buttons where voice is not supported.
- Status, flood rules and the repair ranking are simple, readable JavaScript functions in the same file, so a local developer or student can take it over and change it.
- Demo data for one pilot village is built in and labelled as demo data.

### What we would do next

- A missed-call / SMS version for people without smartphones, so a report can come from any phone.
- A small solar-powered printed board at the chaupal that mirrors the app for people with no phone at all.
- Take it to two real villages near Meerut, sit with the panchayat, and replace the demo data with their real water points.

## Note on the demo data

Rampur is a sample village. The 12 points, family counts and reports in the app are realistic examples, marked as demo data inside the app itself. They are there so judges can see the full working flow: report a pump broken by voice, turn on Flood Mode, and read the repair list.
