# terraform-aws-tardigrade-route53-zone//modules/query-log

Terraform module to create the query log config for a Route53 Zone.

<!-- BEGIN TFDOCS -->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| aws | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| create\_route53\_query\_log | Controls whether to create the Route53 Query Logging configuration | `bool` | n/a | yes |
| query\_log\_bucket | Sets the destination bucket for Route53 Query Logs delivered by Kinesis Firehose | `string` | n/a | yes |
| zone\_id | ID of the Route53 zone to configure for query logging | `string` | n/a | yes |
| iam\_role\_arn\_cloudwatch | IAM Role ARN for Cloudwatch service permissions | `string` | `null` | no |
| iam\_role\_arn\_firehose | IAM Role ARN for Firehose service permissions | `string` | `null` | no |
| query\_log\_bucket\_kms\_key | ARN of the KMS Key ID or Alias associated with bucket encryption of `route53_query_log_bucket`. Required if bucket is encrypted and `iam_role_arn_firehose` is `null` | `string` | `null` | no |
| query\_log\_retention | Specifies the number of days you want to retain log events in the CloudWatch log group. | `number` | `7` | no |
| tags | A map of tags to add to the query log resources | `map(string)` | `{}` | no |

## Outputs

No output.

<!-- END TFDOCS -->