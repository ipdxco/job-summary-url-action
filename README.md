# Job Summary URL

The action calculates the permalink to the job summary for a given job ID. It also provides links to the run, job, and the raw summary which are not available in the workflow run context by default.

If no inputs are provided, the action will calculate the URLs for the currently runnnig job.

## Inputs

| Name | Description | Required | Default |
| --- | --- | --- | --- |
| repository | The owner and repository name. Defaults to `GITHUB_REPOSITORY`. | true | github.repository |
| server_url | The URL of the GitHub server. Defaults to `GITHUB_SERVER_URL`. | true | github.server_url |
| workflow | The name or the id of the workflow. Defaults to `GITHUB_WORKFLOW`. | true | github.workflow |
| run_id | The id of the workflow run. Or `latest`. Defaults to `GITHUB_RUN_ID`. | true | github.run_id |
| run_attempt | The number of the attempt of the workflow run. Or `latest`. Defaults to `GITHUB_RUN_ATTEMPT`. | true | github.run_attempt |
| job | A unique string for the workflow run job. Or `latest`. Defaults to `latest`. | true | github.job |

## Outputs

| Name | Description |
| --- | --- |
| run_url | The URL of the run |
| job_url | The URL of the job |
| job_summary_url | The URL of the job summary |
| job_summary_raw_url | The URL of the raw job summary |

## Example

```
- uses: pl-strflt/export-job-urls@v1
```
