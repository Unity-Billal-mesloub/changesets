# @changesets/types

## 7.0.0

### Major Changes

- [#1994](https://github.com/Unity-Billal-mesloub/changesets/pull) [`062530b`](https://github.com/Unity-Billal-mesloub/changesets/commit/062530b825d53abc9d8934f3a50cc61ff3ff82b8) Thanks [@Unity-Billal-mesloub](https://github.com/Unity-Billal-mesloub)! - Replaced the `prettier` config option with `format`. `format` supports `"auto"`, `"prettier"`, `"oxfmt"`, `"deno"`, `"dprint"`, and `false`. If you previously used `prettier: false`, migrate to `format: false`.

- [#2040](https://github.com/Unity-Billal-mesloub/changesets/pull) [`88f2abb`](https://github.com/Unity-Billal-mesloub/changesets/commit/88f2abb5e14748b08e3441fd871df60dd1c4737f) Thanks [@Unity-Billal-mesloub](https://github.com/Unity-Billal-mesloub)! - Use stricter types for the options parameter for `CommitFunctions`, `ChangelogFunctions`, `Config` & `WrittenConfig`'s `commit` and `changelog` properties, to `null | Record<string, unknown>` instead of `any` or `Record<string, any>`

- [#1482](https://github.com/Unity-Billal-mesloub/changesets/pull) [`df424a4`](https://github.com/Unity-Billal-mesloub/changesets/commit/df424a4a09eea15b0fa9159ee0b98af0d95f58a7) Thanks [@Unity-Billal-mesloub](https://github.com/Unity-Billal-mesloub)! - Bumped supported Node versions to `^22.11 || ^24 || >=26`

- [#2133](https://github.com/Unity-Billal-mesloub/changesets/pull) [`4c26f2f`](https://github.com/Unity-Billal-mesloub/changesets/commit/4c26f2faac89b53d3305cf73c9e9cfca5aa88f5f) Thanks [@Unity-Billal-mesloub](https://github.com/Unity-Billal-mesloub)! - Remove `"private"` type support for `WrittenConfig.access`. Only `"public"` and `"restricted"` are valid values. This change was also already made in [#2015](https://github.com/Unity-Billal-mesloub/changesets/pull) in the runtime.

- [#2190](https://github.com/Unity-Billal-mesloub/changesets/pull) [`96b65ee`](https://github.com/Unity-Billal-mesloub/changesets/commit/96b65eec4af2c58301a11cd7dff42a6bde9c9f8a) Thanks [@Unity-Billal-mesloub](https://github.com/Unity-Billal-mesloub)! - Move versioned prerelease changesets to `.changeset/pre/` folder instead of accumulating in the root and tracking the versioned changeset ids in the `.changeset/pre.json` file. Existing `pre.json` will auto-migrate to this new structure on the next run of `changeset version` or when calling `changeset status`.

  This change allows easier management of versioned prerelease changesets (for the final stable release) and current queued changesets (for the next prerelease). Changesets in `.changeset/pre/` can be edited or deleted depending if it's still relevant for the final stable release of a package. There's no need to synchronize the changeset ids in `pre.json` if certain changesets are deleted.

- [#2117](https://github.com/Unity-Billal-mesloub/changesets/pull) [`813bbf3`](https://github.com/Unity-Billal-mesloub/changesets/commit/813bbf314d051bfee3b46a793f94b396ef2a4df1) Thanks [@Unity-Billal-mesloub](https://github.com/Unity-Billal-mesloub)! - Remove the `pre.json` `initialVersions` property and handling as it's unused internally

- [#1482](https://github.com/Unity-Billal-mesloub/changesets/pull) [`df424a4`](https://github.com/Unity-Billal-mesloub/changesets/commit/df424a4a09eea15b0fa9159ee0b98af0d95f58a7) Thanks [@Unity-Billal-mesloub](https://github.com/Unity-Billal-mesloub)! - From now on this package is going to be published as ES module.

,v
