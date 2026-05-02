# gtex62-shared-assets

Shared binary assets for GTex62 Conky suites.

This repository-level directory keeps large reusable files out of the engine and
out of individual engine-native suite repos.

## Layout

```text
gtex62-shared-assets/
├── data/
├── fonts/
├── icons/
├── wallpapers/
└── docs/
```

## Font Installation

Fonts can be installed into `~/.local/share/fonts/` using the helper script in
`gtex62-core`:

```bash
bash ~/.config/conky/gtex62-core/scripts/install-fonts.sh
```

Running the script is optional, but fonts required by a specific suite must be
installed for that suite to render correctly. Required fonts are listed in each
suite's README. The script copies all fonts from this repo's `fonts/` tree,
preserves subdirectory structure, writes a manifest at
`~/.local/share/fonts/.gtex62-core-fonts.manifest`, and runs `fc-cache -f`.

## Ownership

- Wallpapers, reusable icon packs, shared font binaries, and shared data files live here.
- Engine code lives in [`gtex62-core`](../gtex62-core/README.md).
- Suite-specific layout, theme, and rendering code stays in each suite repo.

Legacy suites are left intact. Engine-native suites should reference this root
instead of copying shared binary assets into their own trees.
