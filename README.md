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
