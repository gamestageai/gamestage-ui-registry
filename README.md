# Gamestage UI registry

This repository serves the Gamestage UI component registry. It holds the
components themselves and nothing else: no build, no tests, no tooling.

You do not clone this. You install from it:

```sh
npx gamestage-ui add choice
```

That writes the component and its stylesheet into your project, brings whatever
it depends on, and installs any npm packages it needs. You own the files it
writes and nothing upgrades them under you.

`npx gamestage-ui list` prints everything served here.

Documentation: https://gamestage.ai/docs/gamestage-ui

## Licence

MIT. The components this serves are written into your project and are yours to
change; the licence is there so copying them in is permitted rather than merely
tolerated.

## What the files are

Each `r/<name>.json` describes one item: its metadata, what it depends on, and
the source of every file it writes. `r/registry.json` is the index the CLI reads
first.

The source of truth is a separate repository. These files are generated from it,
so a change made here would be overwritten rather than kept.
