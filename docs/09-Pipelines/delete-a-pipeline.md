---
sidebar_position: 5
---

# Pipeline Deletion

## Prerequisites for Deleting a Pipeline
1. There should be a `running cluster`.
2. A project should be running as a pipeline is a part of it.
3. A pipeline should exist.

## Consequences of Deleting a Pipeline

1. `Sub-domain` on which the pipeline is deployed won't be functional anymore.
2. All the associated Kubernetes objects like `ingress`, `deployments`, `secrets` and `services` of the pipeline will also be deleted.

## Recommendation before Deleting a Pipeline
It is recommended to have a backup of your `YAML`, `docker file` and `secrets` before deleting a pipeline.

## Deleting the Pipeline
1. Go to Humalect Console's `dashboard`.
2. Click on `Projects`.
3. Click on the `Pipelines` button.
![list-all-projects](./../../static/img/list-all-projects.png)
4. Click on the `highlighted three dots` towards the right of the respective row.
![list-all-pipelines](./../../static/img/list-all-pipelines.png)
5. You will see `delete` button, click on this button.

![delete-dropdown](./../../static/img/delete-dropdown.png)

6. Click on the ✅ icon to delete the pipeline.

![confirm-deletion-pipeline](./../../static/img/confirm-deletion-pipeline.png)

Your pipeline will be deleted.

### Troubleshooting
Need help? [Contact](./../Contact-us/reach-out-to-us) us

