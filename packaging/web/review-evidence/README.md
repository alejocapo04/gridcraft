# GridCraft native provider evidence

Source: `8aac775b335b16bf64b358e5f23be10f8bebf46c`.
Workflow: `be0b8673ce1404b224dbd0d3bd4543e32008ec56`.
[Validation run](https://github.com/alejocapo04/gridcraft/actions/runs/41292359404).
Fonts: `b076417b5880bd4154bd22f00695b1d28c6bea83`.
Artifact ZIP SHA-256: `7b18e89ce7c038267504f67e23086bc380524bb0a90b34caa83eee92c673f40a`.

Both PNGs were produced by the repository native offscreen renderer at 1440×900 and visually inspected. The local image is the normal spreadsheet editor with no registered provider. The provider image explicitly opens Backstage Home with synthetic provider/device history; its synthetic local file is unavailable by design. These are not browser/authentication/backend storage E2E evidence.

The caller-limit fix is separately exercised by real Backstage render tests with 100 provider resources: Home shows 8 and retains device history; Open retains all 100. A negative control makes that Home regression fail when the limit is bypassed, then restores the exact published source before all 6 Backstage tests pass. Format, affected UI/web all-target Clippy and the actual browser WASM package also passed. This is affected-path validation, not a new full-workspace CI claim.

## Save routing validation

[Run 41295082734](https://github.com/alejocapo04/gridcraft/actions/runs/41295082734) validated source `63be89b16b4cd33c7c0bd67bdf2e9e10108e6618` with format, affected UI/web all-target Clippy, **283 UI library tests**, and the actual web WASM package check. The Backstage overwrite regression fails with provider-bound routing removed and passes on restored source. Five new tests cover bound-resource capture/ACK, unbound/disabled Save, explicit UI-command discovery/results, local picker cancellation/browser fallback, and invalid mode rejection. Exact source/workflow provenance is in `save-validation.json`; this test-only run captured no PNGs.

The screenshots above were rendered from `8aac775b335b16bf64b358e5f23be10f8bebf46c` and illustrate the unchanged static editor/Home layout. They were not recaptured from the Save-routing revision and do not prove a browser/backend storage round trip.

## Provider Save As caption

[Run 41297832874](https://github.com/alejocapo04/gridcraft/actions/runs/41297832874) validated the label-only source `c598d96bcda28ca18fe198a3bbc9df7ccef81122` with format, affected UI/web all-target Clippy, the WASM package and the existing native snapshot renderer. Both Save As scenes use the official Spanish locale and `--dialog 'backstage={"page":"saveAs"}'`. `save-as-local.png` shows the normal native `Examinar…` action; `save-as-provider.png` shows `Guardar` with a provider enabled. The browser-only download caption and local export branches are preserved in source; no browser download scene was rendered here. Existing 283 UI library tests and the overwrite negative control passed on `63be89b16b4cd33c7c0bd67bdf2e9e10108e6618` before this caption-only change.

The two PNGs were visually inspected and their hashes matched `save-as-provenance.json`. Artifact ZIP SHA-256: `57e3831bc5d2d475504163a1178c598f253aef7b04bccc147e3fe02a4199024a`.
