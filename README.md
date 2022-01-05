# terraform-credentials-env

A Terraform [credentials
helper](https://www.terraform.io/internals/credentials-helpers) that reads
credentials from environment varialbles.

Environment variable format: `TF_TOKEN_<hostname>`.
Hostname should have `.` characters replaced with `_`, as it is difficult
to set environment variables with dots in name.

Example usage:

```shell
TF_TOKEN_app_terraform_io=abc123
```

[direnv](https://direnv.net/) is recommended when using this plugin.

## Installation

```shell
mkdir -p ~/.terraform.d/plugins/ &&
  wget https://raw.githubusercontent.com/favadi/terraform-credentials-env/main/terraform-credentials-env -O ~/.terraform.d/plugins/terraform-credentials-env &&
  chmod +x ~/.terraform.d/plugins/terraform-credentials-env
```
