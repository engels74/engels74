# Repository CI

GitHub profile Markdown. Source images are produced by github-stats; this repository does not regenerate them.

Every PR, default-branch push and manual dispatch runs read-only JSON/TOML/YAML,
merge/case conflict, private-key and secret checks through prek. The shared
`ci / required` gate rejects missing, failed, cancelled and skipped prerequisites.
Checks must leave tracked files unchanged. All action references use full release
tags from the shared automation hub; Renovate tracks action and hook versions.

Run `SKIP=no-commit-to-branch prek run --all-files` locally with prek 0.5.2.
Use `prek install` for local checks and `prek install --hook-type commit-msg` for
Conventional Commit validation. The local branch hook is skipped in CI.

Automerge is disabled. No branch protections or rulesets are configured.
Manually review exact head/base, full diff, author/DCO, all expected CI jobs and
relevant artifacts before merging through the maintainer's `ghmerge` function.

Content checks do not prove prose accuracy, external-service availability, or
application behavior. No application build or placeholder tests are introduced.
