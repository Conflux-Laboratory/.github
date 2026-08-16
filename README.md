# .github

Organisation-level configuration and public presentation for [Conflux-Laboratory](https://github.com/Conflux-Laboratory).

**This repository is public on purpose.** GitHub renders an organisation profile page only from a *public* `.github` repository — if this one were private, [github.com/Conflux-Laboratory](https://github.com/Conflux-Laboratory) would show nothing. The laboratory's actual work lives in private repositories; nothing here reveals more than the website already does.

## Contents

```
.github/
├── profile/
│   ├── README.md              # ← rendered at github.com/Conflux-Laboratory
│   └── assets/
│       ├── banner-dark.png    # 2400×600, shown under prefers-color-scheme: dark
│       └── banner-light.png   # 2400×600, shown otherwise
├── org-assets/
│   ├── avatar-1024.png        # organisation avatar — upload manually, see below
│   ├── logo-color.svg         # two-colour confluence mark
│   └── logo-lockup.svg        # mark + ConfluxLab wordmark (short form)
└── README.md                  # this file
```

## Editing the profile page

Edit `profile/README.md` and push to `main`; the organisation page picks it up immediately.

Two constraints are easy to trip over:

- **Images must use absolute `raw.githubusercontent.com` URLs.** Relative paths are unreliable in organisation profile READMEs — they resolve against the viewer's context rather than this repository. If you move or rename an asset, update the URLs in `profile/README.md` to match.
- **The banner is a `<picture>` element** with `prefers-color-scheme` sources, so it adapts to the viewer's GitHub theme. Keep both variants in step; the `<img>` fallback is the light one, for clients that ignore `<source>`.

## Setting the organisation avatar

The avatar cannot be set through the GitHub API — there is no endpoint for it. Upload it by hand:

**Settings → General → Profile picture → Upload a photo…** and choose `org-assets/avatar-1024.png`.

The description and website URL *are* set via the API and are already configured. If you change them, keep the description consistent with the positioning statement in the brand package.

## Brand

The canonical source for identity, voice, colour, and typography is the private `brand` repository. Rules that apply to anything published here:

- Write the name in full: **Conflux Laboratory** — this is also the legal name. The one-token **ConfluxLab** is the short form, kept for the domain, handles, and the existing logo lockups. Never "Conflux Lab" or "CONFLUX LAB".
- British English (programme, analyse, behaviour).
- No marketing superlatives — *cutting-edge, innovative, world-class, revolutionary* — and no vague abstractions such as *unlock value* or *leverage*.
- Pair the wordmark with a qualifier on first mention, and keep the disambiguation note: the term "Conflux" is used by unrelated projects.
