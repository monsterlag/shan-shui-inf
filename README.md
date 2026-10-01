## Colour fork

This fork adds colour, smooth scrolling and seeded regional variety to the original:

- Four palettes: blue-green (qinglu), autumn, snow, and the original ink. Switching repaints the visible stretch and cross-fades to it.
- Mountains carry colour washes that fade with distance; trees, roofs, water and figures have their own colours.
- The landscape is drawn once onto bitmap tiles in a web worker, so scrolling only moves images. Without worker support, painting is time-sliced on the main thread.
- Finished tiles are added to the page in batches, and the scroll track grows in large steps, so the page changes as little as possible while a scroll is running.
- Native scrolling (trackpad, touch, wheel, mouse drag, arrow keys), with a slow drift on top that pauses while you scroll.
- A seeded generator with an independent random stream per feature: the same seed always gives the same scroll. Seeds are readable names such as `quiet-ridge-27`, editable on the page and stored in the URL (`#seed=...`).
- Regions: the seed sets slowly shifting traits along the scroll, such as peak height, range density, open water, forest cover and villages.

The landscape generator is Lingdong Huang's original code, modified. Original README follows.

---

# {Shan, Shui}*
Procedurally-generated vector-format infinitely-scrolling Chinese landscape for the browser.
Generate your own on https://lingdong-.github.io/shan-shui-inf/ (or [Alternative link](https://shan-shui-inf.glitch.me)).

Some examples:
![Screenshot1](/screenshots/screen001.jpg?raw=true "")
![Screenshot2](/screenshots/screen002.jpg?raw=true "")

{Shan, Shui}\* is inspired by [traditional Chinese landscape scrolls](https://en.wikipedia.org/wiki/Shan_shui) (such as [this](https://en.wikipedia.org/wiki/Dwelling_in_the_Fuchun_Mountains) and [this](https://en.wikipedia.org/wiki/Wang_Ximeng)) and uses noises and mathematical functions to model the mountains and trees from scratch. It is written entirely in javascript and outputs Scalable Vector Graphics (SVG) format.
