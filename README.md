## Colour fork

This fork adds colour and smooth scrolling to the original:

- Four palettes, switchable live: blue-green (qinglu), autumn, snow, and the original ink.
- Mountains carry colour washes that fade with distance; trees, roofs, water and figures have their own colours.
- The page drifts on its own and can be dragged, swiped, scrolled, or moved with the arrow keys.
- Painting runs in a web worker where available, and is time-sliced otherwise, so the page stays responsive.

The landscape generator is Lingdong Huang's original code, modified. Original README follows.

---

# {Shan, Shui}*
Procedurally-generated vector-format infinitely-scrolling Chinese landscape for the browser.
Generate your own on https://lingdong-.github.io/shan-shui-inf/ (or [Alternative link](https://shan-shui-inf.glitch.me)).

Some examples:
![Screenshot1](/screenshots/screen001.jpg?raw=true "")
![Screenshot2](/screenshots/screen002.jpg?raw=true "")

{Shan, Shui}\* is inspired by [traditional Chinese landscape scrolls](https://en.wikipedia.org/wiki/Shan_shui) (such as [this](https://en.wikipedia.org/wiki/Dwelling_in_the_Fuchun_Mountains) and [this](https://en.wikipedia.org/wiki/Wang_Ximeng)) and uses noises and mathematical functions to model the mountains and trees from scratch. It is written entirely in javascript and outputs Scalable Vector Graphics (SVG) format.
