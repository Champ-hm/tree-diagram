# 🌳 Tree Diagram Creator

A tiny, zero-dependency website for making tree diagrams **fast**. The whole point:
it's really easy to type onto. Build your tree as a list of boxes you type into,
press **Create diagram**, and get a clean visual tree you can export.

## Run it

Open `index.html` in any modern browser — that's the whole app (no build step, no
server, no dependencies). Or serve it locally:

```sh
python3 -m http.server
# then visit http://localhost:8000
```

## How to use it

1. **Build your tree** in the left panel. Every row is a box:
   - Type the box text in the main input.
   - Type an optional **connector label** in the small dashed input (it appears on
     the line from the parent, e.g. `yes`, `no`, `60%`).
   - Toggle any box into a green **result** box with the `box`/`result` pill.
   - Use `+ box` / `+ result` to add children, `✕` to delete.
2. Press **Create diagram ▸** — the visual tree renders in the right panel.
3. Switch **Top → down / Left → right**, zoom, and download as **SVG** or **PNG**.

## Saving your work

Your tree autosaves to the browser's local storage **where the browser allows it**.
Some environments (sandboxed previews, private windows with storage disabled) block
that — the app shows a warning banner when this happens and warns before you leave
the page. Either way, **Save file** downloads your tree as a `.json` file and
**Open file** loads it back, so you can always keep your work.

## AI check — find mistakes in a picture of a tree diagram

The third panel lets you upload, paste (`Ctrl+V`), or drag in a screenshot of any
tree diagram (yours or one drawn elsewhere — decision tree, probability tree,
dichotomous key, …) and have Claude analyze it: it lists every mistake it finds,
quotes where it is on the diagram, and says how to fix it. The
**Use my current diagram** button analyzes the tree you built in the app.

- It needs your own [Anthropic API key](https://console.anthropic.com/) —
  the key is kept only in your browser, and the image is sent directly from your
  browser to the Anthropic API (`claude-opus-4-8`). Nothing goes through any other server.
- This feature needs normal network access, so it works when the site is opened
  locally or hosted (e.g. GitHub Pages) — not inside sandboxed preview iframes.

### Keyboard shortcuts (the fast way)

| Key | Action |
| --- | --- |
| `Enter` | New box below the current one (new sibling) |
| `Tab` | New child box under the current one |
| `Backspace` on an empty box | Delete it |
| `Alt` + `↑` / `↓` | Reorder among siblings |
| `Ctrl`/`Cmd` + `Enter` | Create the diagram |

Your tree autosaves to your browser's local storage and never leaves your device.
Use **Load example** to see a finished decision tree in one click.
