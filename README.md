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

## Ownership

- Wallpapers, reusable icon packs, shared font binaries, and shared data files live here.
- Engine code lives in [`gtex62-core`](../gtex62-core/README.md).
- Suite-specific layout, theme, and rendering code stays in each suite repo.

Legacy suites are left intact. Engine-native suites should reference this root
instead of copying shared binary assets into their own trees.
