## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | n/a |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [aws_instance.worker](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/instance) | resource |
| [aws_security_group.worker_sg](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/security_group) | resource |
| [aws_security_group_rule.worker_egress](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/security_group_rule) | resource |
| [aws_security_group_rule.worker_ssh_ingress](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/security_group_rule) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_ami_id"></a> [ami\_id](#input\_ami\_id) | The ID of the worker instance AMI. | `string` | n/a | yes |
| <a name="input_bastion_sg_id"></a> [bastion\_sg\_id](#input\_bastion\_sg\_id) | The ID of the bastion Security Group. | `string` | n/a | yes |
| <a name="input_block_devices"></a> [block\_devices](#input\_block\_devices) | A list of block devices attached to the worker instance. | <pre>list(object({<br>    name        = string<br>    snapshot_id = string<br>    volume_size = number<br>  }))</pre> | `[]` | no |
| <a name="input_instance_profile_name"></a> [instance\_profile\_name](#input\_instance\_profile\_name) | The name of the instance profile attached to the worker instance. | `string` | n/a | yes |
| <a name="input_name"></a> [name](#input\_name) | The name of the worker. | `string` | n/a | yes |
| <a name="input_subnet_id"></a> [subnet\_id](#input\_subnet\_id) | The ID of the subnet into which the worker instance is placed. | `string` | n/a | yes |
| <a name="input_user_data_template"></a> [user\_data\_template](#input\_user\_data\_template) | The template file used to generate user data injected into the worker instance. | `string` | n/a | yes |
| <a name="input_vpc_id"></a> [vpc\_id](#input\_vpc\_id) | The ID of the VPC into which the worker instance is placed. | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_instance_id"></a> [instance\_id](#output\_instance\_id) | The ID of the worker EC2 instance. |
| <a name="output_sg_id"></a> [sg\_id](#output\_sg\_id) | The ID of the worker Security Group. |
