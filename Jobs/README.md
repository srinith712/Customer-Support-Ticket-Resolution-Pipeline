## Databricks Job

`job/job_config.json` contains the exported Job definition (task order and
dependencies: Bronze → Silver → Gold). To recreate it in your own workspace:
Jobs & Pipelines → Create Job → ⋮ menu → **View as code**,
paste this in, adjusting the `notebook_path` values to match where you imported
the notebooks.
