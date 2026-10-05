# Drone Sevkiyat

A mobile-friendly browser game where you sort packages coming off a conveyor belt onto the right cargo drones. The rules change as you play: first by color, then by shape, then fragile packages need their own protected drone.

**Play:** https://calkanli5.github.io/Drone-Sevkiyat/

## How to play

- **Drag** a package from the belt and drop it on the matching drone.
- **Tap a drone** to send it the package closest to the end of the belt (keys `1`–`4` on desktop).
- Dropping a package on the wrong drone, or letting one reach the yellow line at the end of the belt, costs a life. You have **3 lives**.

## Rule progression

There are no levels; the rules switch automatically based on how many packages you have delivered.

| Delivered | Rule |
|---|---|
| 0–7 | Sort by **color** |
| 8–17 | Sort by **shape** (ignore the color) |
| 18–29 | Shape, plus **fragile** packages go only to the protected drone |
| 30+ | **Mixed**: some drones take a color, some a shape; drones are reshuffled every 12 packages |

The belt speeds up gradually with both deliveries and elapsed time, and packages arrive more often. Consecutive correct deliveries raise a score multiplier (up to ×5).

## Features

- Touch and mouse support through a single pointer-based input system
- Scales to phone screens, respects notches and safe areas
- Light and dark theme, following the system setting
- Sound effects with a mute toggle, vibration on Android when a life is lost
- Best score saved locally in the browser
- Menu button (or `Esc`) to return to the main menu during a game

## Run locally

It is a single self-contained file with no build step. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Tech

Plain HTML, CSS and JavaScript. Graphics are inline SVG, sounds are generated with the Web Audio API. The only external resource is the Barlow font from Google Fonts, with system fallbacks.

---

## Türkçe

Banttan gelen kargo paketlerini doğru dronlara yerleştirdiğin, mobil uyumlu bir tarayıcı oyunu. Kural oyun ilerledikçe değişir: önce renk, sonra şekil, sonra kırılacak paketler. Paketi sürükleyip drona bırak ya da drona dokunarak en öndeki paketi gönder. Yanlış dron veya bant sonuna kaçan paket bir hak götürür; 3 hakkın var ve bant zamanla hızlanır.
