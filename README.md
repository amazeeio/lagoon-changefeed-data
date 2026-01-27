# lagoon-changefeed-data
Centralized repo for Lagoon change feed data. Managed via automated workflows and consumed by the [uselagoon/ui-library](https://github.com/uselagoon/ui-library).

### Schema

The change feed data is validated against the [changefeed.schema.json](changefeed.schema.json) file using standard JSON validation.

### Content Update Workflow

1.  **Edit Data**: Update the [changefeed.json](changefeed.json) file on a new branch.
2.  **Validation**: Validation runs locally via `npm run validate` or automatically on PR/Push in GitHub Actions.
3.  **Auto-PR**: On any branch push (except `main`) that modifies `changefeed.json`, a GitHub Action will automatically create a PR if one doesn't exist.
4.  **Merge**: Once merged, the data is available for consumption in the ChangeFeed component in the [uselagoon/ui-library](https://github.com/uselagoon/ui-library).
