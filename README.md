# lagoon-changelog-data
Centralized repo for Lagoon changelog data. Managed via automated workflows and consumed by the [uselagoon/ui-library](https://github.com/uselagoon/ui-library).

### Schema

The changelog data is validated against the [changelog.schema.json](changelog.schema.json) file using standard JSON validation.

### Content Update Workflow

1.  **Edit Data**: Update the [changelog.json](changelog.json) file on a new branch.
2.  **Validation**: Validation runs locally via `npm run validate` or automatically on PR/Push in GitHub Actions.
3.  **Auto-PR**: On any branch push (except `main`) that modifies `changelog.json`, a GitHub Action will automatically create a PR if one doesn't exist.
4.  **Merge**: Once merged, the data is available for consumption in the ChangeLog component in the [uselagoon/ui-library](https://github.com/uselagoon/ui-library).
