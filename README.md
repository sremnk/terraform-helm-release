# terraform-helm-release

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| <a name="provider_helm"></a> [helm](#provider\_helm) | 2.5.1 |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [helm_release.this](https://registry.terraform.io/providers/hashicorp/helm/latest/docs/resources/release) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_release"></a> [release](#input\_release) | List application to deploy | <pre>map(object({<br>    repository_name     = string<br>    chart               = string<br>    repository          = string<br>    repository_username = string<br>    repository_password = string<br>    version             = string<br>    verify              = bool<br>    timeout             = number<br>    reuse_values        = bool<br>    reset_values        = bool<br>    force_update        = bool<br>    recreate_pods       = bool<br>    max_history         = number<br>    wait                = bool<br>    values              = list(string)<br>    set = list(object({<br>      name  = string<br>      value = string<br>    }))<br>    namespace        = string<br>    create_namespace = bool<br>  }))</pre> | `{}` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_chart"></a> [chart](#output\_chart) | The name of the chart. |
| <a name="output_namespace"></a> [namespace](#output\_namespace) | Namespace is the kubernetes namespace of the release. |
| <a name="output_status"></a> [status](#output\_status) | Status of the release. |
| <a name="output_values"></a> [values](#output\_values) | The compounded values from values and set* attributes. |
| <a name="output_version"></a> [version](#output\_version) | A SemVer 2 conformant version string of the chart. |
<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
