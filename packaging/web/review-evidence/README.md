# GridCraft native provider evidence

Source: `8aac775b335b16bf64b358e5f23be10f8bebf46c`.
Workflow: `be0b8673ce1404b224dbd0d3bd4543e32008ec56`.
[Validation run](https://github.com/alejocapo04/gridcraft/actions/runs/41292359404).
Fonts: `b076417b5880bd4154bd22f00695b1d28c6bea83`.
Artifact ZIP SHA-256: `7b18e89ce7c038267504f67e23086bc380524bb0a90b34caa83eee92c673f40a`.

Both PNGs were produced by the repository native offscreen renderer at 1440×900 and visually inspected. The local image is the normal spreadsheet editor with no registered provider. The provider image explicitly opens Backstage Home with synthetic provider/device history; its synthetic local file is unavailable by design. These are not browser/authentication/backend storage E2E evidence.

The caller-limit fix is separately exercised by real Backstage render tests with 100 provider resources: Home shows 8 and retains device history; Open retains all 100. A negative control makes that Home regression fail when the limit is bypassed, then restores the exact published source before all 6 Backstage tests pass. Format, affected UI/web all-target Clippy and the actual browser WASM package also passed. This is affected-path validation, not a new full-workspace CI claim.
