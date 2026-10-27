# ax-prototype

Static hosting (GitHub Pages) for clickable prototypes used in usability studies. Participants
receive direct links to a prototype; the site root does not list them.

## Layout

```
index.html    placeholder page
v1/           shared interaction tracker, copied in from the tracker repo
<prototype>/  one top-level folder per prototype
```

## Rules

- Each prototype lives in its own folder directly at the repo root, beside `v1/`. Pages load the
  tracker from `../v1/tracker.js`, so deeper nesting breaks it.
- Every page keeps the tracker loader block at the end of `<body>` unchanged.
- Folder and file names identify screens in recorded studies. Use lowercase, hyphenated names, and
  never rename, move, or overwrite a folder once a study has used it. A revised prototype goes in a
  new folder (for example `login-test-v2/`).
- `v1/tracker.js` is shared by every prototype and is never edited here; it is only replaced with a
  new copy from the tracker repo.
