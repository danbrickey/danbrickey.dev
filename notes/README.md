# Lab Notes

Published write-ups derived from build records in the project repos.

## Why these live here and not in their own repo

Two tiers, and they already exist:

| Tier | Where | State |
|---|---|---|
| Raw | the origin project repos | Private, unreviewed. Notebook entries, build reports, decision logs, specs. |
| Published | this directory | Curated, edited, public. |

The origin repos are private and deliberately unnamed here. What matters to a
reader is that the records exist, that they predate the write-up, and that a
claim can be traced back to one on request.

A third repo in the middle would represent "drafted but not published," which
is a directory or a branch, not a repo. It would also split the source of
truth from the thing that publishes it, and that split is where content rots.

The origin repos stay the vault. This is the consumption view.

## Structure

```
notes/
  README.md                                  this file
  _template.md                               drafting template + the rules
  note.css                                   shared stylesheet
  YYYY-MM-DD_slug.html                       a published note
```

Notes are hand-authored HTML. The site has no build step, and adding one to
convert a handful of markdown files a year would cost more than it saves.
Draft in `_template.md`, then write the page.

`note.css` duplicates the design tokens from `../index.html` rather than
importing them, because `index.html` keeps its CSS inline. If the palette
changes, both need the edit. The token block at the top of `note.css` is the
only part that has to stay in sync.

## Adding a note

1. Copy `_template.md` and draft against the origin repo's records.
2. Check it against the anti-tells in the template and against the voice
   guide.
3. Write `YYYY-MM-DD_slug.html`, linking `note.css`.
4. Add a card to the Lab Notes section of `../index.html` and bump the
   number in its `card__title`.
5. Update the `REV` date in both footers.

## The bar

A note gets published when it has a prediction that could have failed,
numbers with methods attached, named scope limits, and an honest cost. A note
that only reports a success is a press release.

Publish the failures at the same fidelity as the wins. Those are the ones
nobody can fake.
