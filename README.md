# 🏁 Jason's 2026 Race Tracker

A personal race planning tool for Ontario gravel cycling and running events across the 2026 season — spring through late fall.

**Live:** https://jasonkempers.github.io/race-tracker-2026/race-tracker.html

---

## What it does

- Tracks 19 pre-loaded Ontario races (7 cycling/gravel, 12 running)
- Mark each race as **Interested / Doing / Maybe / Skip**
- One-click **Add to Google Calendar** per race
- Export your "Doing" races as a `.ics` file to import into any calendar
- Detects same-day **conflicts** between races
- Add, edit, or delete races via built-in modal
- Filter by type, status, or search by name
- No login, no backend — everything saves in the browser

---

## Races included

### 🚵 Cycling / Gravel
| Race | Date | Distance |
|------|------|----------|
| Paris to Ancaster (P2A) | Apr 26 | 110km, 60km, 30km |
| Scrappy Badger Gravel | May 2 | TBD |
| R3G3 Gravel Cup Canada | May 30 | TBD |
| Screaming Squirrel | Jun 7 | 85km, 30km |
| Blue Mountains Gravel Fondo | Jun 20 | ~120km, ~80km |
| Rideau Lakes Cycle Tour | Jun 20–21 | 210km, 171km, 170km |
| Reggie Ramble Gravel Grinder | Jul 11 | 200km, 130km, 65km |

### 🏃 Running
| Race | Date | Distance |
|------|------|----------|
| Credit Valley Trail Marathon | Apr 26 | 42km, 21km |
| Beneva Mississauga Marathon | Apr 26 | 42km, 21km |
| GoodLife Toronto Marathon | May 3 | 42km, 21km |
| Sporting Life 10K | May 10 | 10km |
| Tamarack Ottawa Race Weekend | May 23–24 | 42km, 21km, 10km |
| Oakville 21.1 | Oct 4 | 21.1km, 10km, 5km |
| The County Marathon (Picton) | Oct 4 | 42km, 21.1km, 5km |
| Fanshawe Trail Race (London) | Oct 17 | 50km, 25km |
| TCS Toronto Waterfront Marathon | Oct 18 | 42km, 21.1km, 5km |
| Niagara Falls 10K, Half & Marathon | Oct 25 | 42km, 21.1km, 10km |
| Hamilton Marathon Road2Hope | Nov 1 | 42km, 21.1km, 10km, 5km |
| Boxing Day 10 Miler (Hamilton) | Dec 26 | 16.1km, 6.4km |

> **Availability note (as of Oct 6, 2026):** every fall half marathon in range has sold out — Toronto Waterfront (transfer/charity only), Niagara Falls, and now Road2Hope's half. Road2Hope's 5K/10K/marathon stay open until ~Oct 27. The Boxing Day 10 Miler takes same-day registration and cannot sell out.

---

## How to use

1. Open `race-tracker.html` in any browser (or use the live link above)
2. Use the dropdown on each race card to set your status
3. Click **+ Add to Google Calendar** to add a race to GCal
4. Click **+ Add Race** to add a new event
5. Use **Export "Doing" to .ics** to download a calendar file for bulk import

> **Tip:** Import the `.ics` into Google Calendar via Settings → Import to check for conflicts with existing events.

---

## Tech

Plain HTML, CSS, and JavaScript. Zero dependencies. No build step. Open the file and it works.

---

## Updating races

Edit the `races` array at the top of the `<script>` block in `race-tracker.html`. Each race object looks like:

```js
{
  id: 1,
  name: "Paris to Ancaster (P2A)",
  type: "bike",           // "bike" or "run"
  date: "2026-04-26",
  location: "Paris → Ancaster, ON",
  distances: "110km, 60km, 30km",
  status: "interested",   // "interested", "doing", "maybe", "skip"
  url: "https://www.parisancaster.com",
  tags: ["gravel", "UCI", "featured"],
  notes: "Biggest gravel event in Canada."
}
```
