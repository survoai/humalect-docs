---
sidebar_position: 5
---

# Pipeline Deletion Process

### Prerequisites for Updating a Pipeline

Before proceeding with the process of updating a pipeline using the Humalect Console, ensure that you satisfy the following prerequisites:

1. **Availability of a Running Cluster:**
   You must have a functional and active cluster established within the Humalect system.

2. **Existing Pipeline Creation:**
   The pipeline you intend to update should have been previously created and exist within the Humalect environment.

### Implications of Deleting a Pipeline

When you delete a pipeline within the Humalect platform, the following consequences will occur:

1. **Sub-domain Deactivation:**
   The sub-domain associated with the deployed pipeline will cease to function.

2. **Deletion of Associated Kubernetes Objects:**
   All Kubernetes objects linked to the pipeline, such as `ingress`, `deployments`, `secrets`, and `services`, will be permanently deleted.

### Precautions before Deleting a Pipeline

Before initiating the deletion of a pipeline, it is advisable to create backups of the following components:

- `YAML` Configuration Files
- `Dockerfile`
- Secrets

### Steps to Delete a Pipeline

1. **Access the Humalect Console Dashboard:**
   Log in to the Humalect Console and navigate to the dashboard.

2. **Select Pipelines:**
   From the right-side menu, choose the "Pipelines" option.

3. **Identify the Pipeline:**
   Locate the specific project pipeline you wish to delete. Click on the highlighted three dots located to the right of the corresponding row.

4. **Initiate Deletion:**
   From the menu that appears, select the "Delete" option to initiate the pipeline deletion process.

5. **Confirm Deletion:**
   Click on the ✅ icon to provide final confirmation for the pipeline deletion.
    
    ![edit-pipeline](./../../static/img/edit_pipeline.png)

   Your selected pipeline will be permanently deleted.

:::info
In case you do not have the option to delete visible, it indicates that your role-based access control (RBAC) permissions are insufficient to perform the deletion. Contact your organization's administrator to grant you the necessary permissions.
:::

### Troubleshooting
Need help? [Contact](./../Contact-us/reach-out-to-us) us

