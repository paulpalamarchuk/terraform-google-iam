# Module Project IAM

This optional module is used to assign project roles

## Example Usage
```
module "project-iam-bindings" {
  source   = "terraform-google-modules/iam/google//modules/projects_iam"
  projects = ["my-project_one", "my-project_two"]
  mode     = "additive"

  bindings = {
    "roles/compute.networkAdmin" = [
      "serviceAccount:my-sa@my-project.iam.gserviceaccount.com",
      "group:my-group@my-org.com",
      "user:my-user@my-org.com",
    ]
    "roles/appengine.appAdmin" = [
      "serviceAccount:my-sa@my-project.iam.gserviceaccount.com",
      "group:my-group@my-org.com",
      "user:my-user@my-org.com",
    ]
  }
}
```

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| bindings | Map of role (key) and list of members (value) to add the IAM policies/bindings | map(list(string)) | n/a | yes |
| bindings\_num | Number of bindings, in case using dependencies of other resources' outputs | number | `"0"` | no |
| mode | Mode for adding the IAM policies/bindings, additive and authoritative | string | `"additive"` | no |
| project | Project to add the IAM policies/bindings | string | `""` | no |
| projects | Projects list to add the IAM policies/bindings | list(string) | `<list>` | no |
| projects\_num | Number of projects, in case using dependencies of other resources' outputs | number | `"0"` | no |

## Outputs

| Name | Description |
|------|-------------|
| members | Members which were bound to projects. |
| projects | Projects wich received bindings. |
| roles | Roles which were assigned to members. |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
