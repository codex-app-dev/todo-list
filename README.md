# Todo — a calm task list

A tiny, single-file todo app that runs in any modern browser with no build step, no install, and no account. Tasks are saved on your own device, and the interface stays out of the way while you work.

## Features

- **Add tasks fast** — type and press Enter, or tap the plus button.
- **Check things off** — tap the circle to complete a task; completed items fade with a strikethrough.
- **Filters with counts** — switch between All, Active, and Done, and clear everything finished in one tap.
- **Progress ring** — the header shows the share of tasks you have completed.
- **Edit in place** — double-click a task to rename it; press Escape to cancel.
- **Persistent** — everything is stored in the browser's local storage, so it survives reloads and closing the tab.
- **Mobile first** — comfortable tap targets, responsive layout, and a dark theme.

## Run it

Open `index.html` in a browser. That is the whole app — HTML, CSS, and JavaScript in one file, with no dependencies and no network access required.

To keep it around, copy the file to any static host, or just bookmark it locally.

## How it works

The app keeps a list of `{ text, done }` objects in `localStorage` under the key `todo.v1` and re-renders the list whenever that array changes. There is no framework and no state library: a single `render()` function reads the list, applies the active filter, and rebuilds the DOM, which keeps the code small and easy to change.

## Notes

- Delete a task with the small ✕ that appears on hover (always visible on touch screens).
- Data lives per browser and per device. Clearing site data clears the list.
