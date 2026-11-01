# Native optional-provider review evidence

Tested source: `e49a77338b2e001636e025fceae9ecd202ec13a3`. QA recipe commit: `ce8c41e47866c838f27a534afc4bafced30d9950`.

The off capture is the default spreadsheet editor, with no provider. The on capture explicitly opens native Backstage Home with synthetic provider and device-history entries; the missing local-history availability is expected, not a real-file open test.

Rendered by the repository native offscreen renderer from synthetic resources. These images do not establish browser/backend end-to-end persistence. Screenshots are contributor-original under the repository license; existing project marks retain their original terms.

Run: https://github.com/alejocapo04/gridcraft/actions/runs/41287541888

- local.png: provider absent.
- provider.png: provider registered.

Hashes and exact inputs are in provenance.json. This evidence branch is separate from the feature PR.
