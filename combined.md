# Acceptance Testing Environment Variable Dictionary

Environment variables (beyond standard AWS Go SDK ones) used by acceptance testing. See also the `internal/acctest` package.

| Variable | Description |
|----------|-------------|
| `ACM_CERTIFICATE_ROOT_DOMAIN` | Root domain name to use with ACM Certificate testing. |
| `ADM_CLIENT_ID` | Identifier for Amazon Device Manager Client in Pinpoint testing. |
| `AMPLIFY_DOMAIN_NAME` | Domain name to use for Amplify domain association testing. |
| `AMPLIFY_GITHUB_ACCESS_TOKEN` | GitHub access token used for AWS Amplify testing. |
| `AMPLIFY_GITHUB_REPOSITORY` | GitHub repository used for AWS Amplify testing. |
| `ADM_CLIENT_SECRET` | Secret for Amazon Device Manager Client in Pinpoint testing. |
| `APNS_BUNDLE_ID` | Identifier for Apple Push Notification Service Bundle in Pinpoint testing. |
| `APNS_CERTIFICATE` | Certificate (PEM format) for Apple Push Notification Service in Pinpoint testing. |
| `APNS_CERTIFICATE_PRIVATE_KEY` | Private key for Apple Push Notification Service in Pinpoint testing. |
| `APNS_SANDBOX_BUNDLE_ID` | Identifier for Sandbox Apple Push Notification Service Bundle in Pinpoint testing. |
| `APNS_SANDBOX_CERTIFICATE` | Certificate (PEM format) for Sandbox Apple Push Notification Service in Pinpoint testing. |
| `APNS_SANDBOX_CERTIFICATE_PRIVATE_KEY` | Private key for Sandbox Apple Push Notification Service in Pinpoint testing. |
| `APNS_SANDBOX_CREDENTIAL` | Credential contents for Sandbox Apple Push Notification Service in SNS Application Platform testing. Conflicts with `APNS_SANDBOX_CREDENTIAL_PATH`. |
| `APNS_SANDBOX_CREDENTIAL_PATH` | Path to credential for Sandbox Apple Push Notification Service in SNS Application Platform testing. Conflicts with `APNS_SANDBOX_CREDENTIAL`. |
| `APNS_SANDBOX_PRINCIPAL` | Principal contents for Sandbox Apple Push Notification Service in SNS Application Platform testing. Conflicts with `APNS_SANDBOX_PRINCIPAL_PATH`. |
| `APNS_SANDBOX_PRINCIPAL_PATH` | Path to the principal for Sandbox Apple Push Notification Service in SNS Application Platform testing. Conflicts with `APNS_SANDBOX_PRINCIPAL`. |
| `APNS_SANDBOX_TEAM_ID` | Identifier for Sandbox Apple Push Notification Service Team in Pinpoint testing. |
| `APNS_SANDBOX_TOKEN_KEY` | Token key file content (.p8 format) for Sandbox Apple Push Notification Service in Pinpoint testing. |
| `APNS_SANDBOX_TOKEN_KEY_ID` | Identifier for Sandbox Apple Push Notification Service Token Key in Pinpoint testing. |
| `APNS_TEAM_ID` | Identifier for Apple Push Notification Service Team in Pinpoint testing. |
| `APNS_TOKEN_KEY` | Token key file content (.p8 format) for Apple Push Notification Service in Pinpoint testing. |
| `APNS_TOKEN_KEY_ID` | Identifier for Apple Push Notification Service Token Key in Pinpoint testing. |
| `APNS_VOIP_BUNDLE_ID` | Identifier for VOIP Apple Push Notification Service Bundle in Pinpoint testing. |
| `APNS_VOIP_CERTIFICATE` | Certificate (PEM format) for VOIP Apple Push Notification Service in Pinpoint testing. |
| `APNS_VOIP_CERTIFICATE_PRIVATE_KEY` | Private key for VOIP Apple Push Notification Service in Pinpoint testing. |
| `APNS_VOIP_TEAM_ID` | Identifier for VOIP Apple Push Notification Service Team in Pinpoint testing. |
| `APNS_VOIP_TOKEN_KEY` | Token key file content (.p8 format) for VOIP Apple Push Notification Service in Pinpoint testing. |
| `APNS_VOIP_TOKEN_KEY_ID` | Identifier for VOIP Apple Push Notification Service Token Key in Pinpoint testing. |
| `APPRUNNER_CUSTOM_DOMAIN` | A custom domain endpoint (root domain, subdomain, or wildcard) for AppRunner Custom Domain Association testing. |
| `AUDITMANAGER_DEREGISTER_ACCOUNT_ON_DESTROY` | Flag to execute tests that will disable AuditManager in the account upon destruction. |
| `AUDITMANAGER_ORGANIZATION_ADMIN_ACCOUNT_ID` | Organization admin account identifier for use in AuditManager testing. |
| `AWS_ALTERNATE_ACCESS_KEY_ID` | AWS access key ID with access to a secondary AWS account for tests requiring multiple accounts. Requires `AWS_ALTERNATE_SECRET_ACCESS_KEY`. Conflicts with `AWS_ALTERNATE_PROFILE`. |
| `AWS_ALTERNATE_SECRET_ACCESS_KEY` | AWS secret access key with access to a secondary AWS account for tests requiring multiple accounts. Requires `AWS_ALTERNATE_ACCESS_KEY_ID`. Conflicts with `AWS_ALTERNATE_PROFILE`. |
| `AWS_ALTERNATE_PROFILE` | AWS profile with access to a secondary AWS account for tests requiring multiple accounts. Conflicts with `AWS_ALTERNATE_ACCESS_KEY_ID` and `AWS_ALTERNATE_SECRET_ACCESS_KEY`. |
| `AWS_ALTERNATE_REGION` | Secondary AWS region for tests requiring multiple regions. Defaults to `us-east-1`. |
| `AWS_API_GATEWAY_DOMAIN_NAME_CERTIFICATE_BODY` | Certificate body of publicly trusted certificate for API Gateway Domain Name testing. |
| `AWS_API_GATEWAY_DOMAIN_NAME_CERTIFICATE_CHAIN` | Certificate chain of publicly trusted certificate for API Gateway Domain Name testing. |
| `AWS_API_GATEWAY_DOMAIN_NAME_CERTIFICATE_PRIVATE_KEY` | Private key of publicly trusted certificate for API Gateway Domain Name testing. |
| `AWS_API_GATEWAY_DOMAIN_NAME_REGIONAL_CERTIFICATE_NAME_ENABLED` | Flag to enable API Gateway Domain Name regional certificate upload testing. |
| `AWS_CODEBUILD_BITBUCKET_SOURCE_LOCATION` | BitBucket source URL for CodeBuild testing. CodeBuild must have access to this repository via OAuth or Source Credentials. Defaults to `https://terraform@bitbucket.org/terraform/aws-test.git`. |
| `AWS_CODEBUILD_GITHUB_SOURCE_LOCATION` | GitHub source URL for CodeBuild testing. CodeBuild must have access to this repository via OAuth or Source Credentials. Defaults to `https://github.com/hashibot-test/aws-test.git`. |
| `AWS_DEFAULT_REGION` | Primary AWS region for tests. Defaults to `us-west-2`. |
| `AWS_DETECTIVE_MEMBER_EMAIL` | Email address for Detective Member testing. A valid email address associated with an AWS root account is required for tests to pass. |
| `AWS_EC2_CLIENT_VPN_LIMIT` | Concurrency limit for Client VPN acceptance tests. [Default is 5](https://docs.aws.amazon.com/vpn/latest/clientvpn-admin/limits.html) if not specified. |
| `AWS_EC2_EIP_PUBLIC_IPV4_POOL` | Identifier for EC2 Public IPv4 Pool for EC2 EIP testing. |
| `AWS_EC2_TRANSIT_GATEWAY_LIMIT` | Concurrency limit for Transit Gateway acceptance tests. [Default is 5](https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-quotas.html) if not specified. |
| `AWS_EC2_VERIFIED_ACCESS_INSTANCE_LIMIT` | Concurrency limit for Verified Access acceptance tests. [Default is 5](https://docs.aws.amazon.com/verified-access/latest/ug/verified-access-quotas.html) if not specified. |
| `AWS_GUARDDUTY_MEMBER_ACCOUNT_ID` | Identifier of AWS Account for GuardDuty Member testing. **DEPRECATED:** Should be replaced with standard alternate account handling for tests. |
| `AWS_GUARDDUTY_MEMBER_EMAIL` | Email address for GuardDuty Member testing. **DEPRECATED:** It may be possible to use a placeholder email address instead. |
| `AWS_LAMBDA_IMAGE_LATEST_ID` | ECR repository image URI (tagged as `latest`) for Lambda container image acceptance tests. |
| `AWS_LAMBDA_IMAGE_V1_ID` | ECR repository image URI (tagged as `v1`) for Lambda container image acceptance tests. |
| `AWS_LAMBDA_IMAGE_V2_ID` | ECR repository image URI (tagged as `v2`) for Lambda container image acceptance tests. |
| `AWS_THIRD_ACCESS_KEY_ID` | AWS access key ID with access to a third AWS account for tests requiring multiple accounts. Requires `AWS_THIRD_SECRET_ACCESS_KEY`. Conflicts with `AWS_THIRD_PROFILE`. |
| `AWS_THIRD_SECRET_ACCESS_KEY` | AWS secret access key with access to a third AWS account for tests requiring multiple accounts. Requires `AWS_THIRD_ACCESS_KEY_ID`. Conflicts with `AWS_THIRD_PROFILE`. |
| `AWS_THIRD_PROFILE` | AWS profile with access to a third AWS account for tests requiring multiple accounts. Conflicts with `AWS_THIRD_ACCESS_KEY_ID` and `AWS_THIRD_SECRET_ACCESS_KEY`. |
| `AWS_THIRD_REGION` | Third AWS region for tests requiring multiple regions. Defaults to `us-east-2`. |
| `CHATBOT_SLACK_CHANNEL_ID` | ID of the Slack channel. |
| `CHATBOT_SLACK_TEAM_ID` | ID of the Slack workspace authorized with AWS Chatbot. |
| `CHATBOT_TEAMS_CHANNEL_ID` | ID of the Microsoft Teams channel. |
| `CHATBOT_TEAMS_TEAM_ID` | ID of the Microsoft Teams workspace authorized with AWS Chatbot. |
| `CHATBOT_TEAMS_TENANT_ID` | ID of the Microsoft Teams tenant. |
| `DX_CONNECTION_ID` | Identifier for Direct Connect Connection testing. |
| `DX_VIRTUAL_INTERFACE_ID` | Identifier for Direct Connect Virtual Interface testing. |
| `EC2_SECURITY_GROUP_RULES_PER_GROUP_LIMIT` | EC2 Quota for Rules per Security Group. Defaults to 50. **DEPRECATED:** Can be augmented or replaced with Service Quotas lookup. |
| `EVENT_BRIDGE_PARTNER_EVENT_BUS_NAME` | Amazon EventBridge partner event bus name. |
| `EVENT_BRIDGE_PARTNER_EVENT_SOURCE_NAME` | Amazon EventBridge partner event source name. |
| `FINSPACE_MANAGED_KX_LICENSE_ENABLED` | Enables tests requiring a license to provision managed KX resources. |
| `GCM_API_KEY` | API Key for Google Cloud Messaging in Pinpoint and SNS Platform Application testing. |
| `GITHUB_TOKEN` | GitHub token for CodePipeline testing. |
| `GLOBALACCERATOR_BYOIP_IPV4_ADDRESS` | IPv4 address from a BYOIP CIDR of AWS Account used for testing Global Accelerator's BYOIP accelerator. |
| `GRAFANA_SSO_GROUP_ID` | AWS SSO group ID for Grafana testing. |
| `GRAFANA_SSO_USER_ID` | AWS SSO user ID for Grafana testing. |
| `MACIE_MEMBER_ACCOUNT_ID` | Identifier of AWS Account for Macie Member testing. **DEPRECATED:** Should be replaced with standard alternate account handling for tests. |
| `QUICKSIGHT_NAMESPACE` | QuickSight namespace name for testing. |
| `QUICKSIGHT_ATHENA_TESTING_ENABLED` | Enable QuickSight tests dependent on Amazon Athena resources. |
| `ROUTE53DOMAINS_DOMAIN_NAME` | Registered domain for Route 53 Domains testing. |
| `RESOURCEEXPLORER_INDEX_TYPE` | Index Type for Resource Explorer 2 Search datasource testing. |
| `SAGEMAKER_IMAGE_VERSION_BASE_IMAGE` | SageMaker base image to use for tests. |
| `SERVICEQUOTAS_INCREASE_ON_CREATE_QUOTA_CODE` | Quota Code for Service Quotas testing (submits support case). |
| `SERVICEQUOTAS_INCREASE_ON_CREATE_SERVICE_CODE` | Service Code for Service Quotas testing (submits support case). |
| `SERVICEQUOTAS_INCREASE_ON_CREATE_VALUE` | Value of quota increase for Service Quotas testing (submits support case). |
| `SES_DOMAIN_IDENTITY_ROOT_DOMAIN` | Root domain name of publicly accessible and Route 53 configurable domain for SES Domain Identity testing. |
| `SES_DEDICATED_IP` | Dedicated IP address for testing IP assignment with a "Standard" (non-managed) SES dedicated IP pool. |
| `SWF_DOMAIN_TESTING_ENABLED` | Enables SWF Domain testing (API does not support deletions). |
| `TEST_AWS_ORGANIZATION_ACCOUNT_EMAIL_DOMAIN` | Email address for Organizations Account testing. |
| `TEST_AWS_SES_VERIFIED_EMAIL_ARN` | Verified SES Email Identity for use in Cognito User Pool testing. |
| `TF_ACC` | Enables Go tests containing `resource.Test()` and `resource.ParallelTest()`. |
| `TF_ACC_ASSUME_ROLE_ARN` | Amazon Resource Name of existing IAM Role to use for limited permissions acceptance testing. |
| `TF_AWS_LICENSE_MANAGER_GRANT_HOME_REGION` | Region where a License Manager license is imported. |
| `TF_AWS_LICENSE_MANAGER_GRANT_LICENSE_ARN` | ARN for a License Manager license imported into the current account. |
| `TF_AWS_LICENSE_MANAGER_GRANT_PRINCIPAL` | ARN of a principal to share the License Manager license with. Either a root user, Organization, or Organizational Unit. |
| `TF_TEST_CLOUDFRONT_RETAIN` | Flag to disable but dangle CloudFront Distributions during testing to reduce feedback time (must be manually destroyed afterwards) |
| `TF_TEST_ELASTICACHE_RESERVED_CACHE_NODE` | Flag to enable resource tests for ElastiCache reserved nodes. Set to `1` to run tests |
<!-- markdownlint-configure-file { "code-block-style": false } -->
# Adding a New Data Source

New data sources are required when AWS adds a new service, or adds new features within an existing service which would require a new data source to allow practitioners to query existing resources of that type for use in their configurations. Anything with a Describe or Get endpoint could make a data source, but some are more useful than others.

Each data source should be submitted for review in isolation, pull requests containing multiple data sources and/or resources are harder to review and the maintainers will normally ask for them to be broken apart.

## Prerequisites

If this is the first addition of a data source for a new service, please ensure the Service Client for the new service has been added and merged. See [Adding a new Service](add-a-new-service.md) for details.

## Steps to Add a Data Source

### Fork the Provider and Create a Feature Branch

For a new data source use a branch named `f-{datasource name}` for example: `f-ec2-vpc`. See [Raising a Pull Request](raising-a-pull-request.md) for more details.

### Create and Name the Data Source

See the [Naming Guide](naming.md#resources-and-data-sources) for details on how to name the new data source and the data source file. Not following the naming standards will cause extra delay as maintainers request that you make changes.

Use the [skaff](skaff.md) provider scaffolding tool to generate new data source and test templates using your chosen name. Doing so will ensure that any boilerplate code, structural best practices and repetitive naming are done for you and always represent our most current standards.

### Fill out the Data Source Schema

In the `internal/service/<service>/<service>_data_source.go` file you will see a `Schema` property which exists as a map of `Schema` objects. This relates the AWS API data model with the Terraform resource itself. For each property you want to make available in Terraform, you will need to add it as an attribute, and choose the correct data type.

Attribute names are to be specified in `snake_case` as opposed to the AWS API which is `CamelCase`.

### Implement Read Handler

These will map the AWS API response to the data source schema. You will also need to handle different response types (including errors correctly). For complex attributes you will need to implement Flattener or Expander functions. The [Data Handling and Conversion Guide](data-handling-and-conversion.md) covers everything you need to know for mapping AWS API responses to Terraform State and vice-versa. The [Error Handling Guide](error-handling.md) covers everything you need to know about handling AWS API responses consistently.

### Register Data Source to the provider

Data Sources use a self-registration process that adds them to the provider using the `@SDKDataSource()` annotation in the data source's comments. Run `make gen` to register the data source. This will add an entry to the `service_package_gen.go` file located in the service package folder.

=== "Terraform Plugin Framework (Preferred)"

    ```go
    package something

    import (
        "github.com/hashicorp/terraform-plugin-framework/datasource"
        "github.com/hashicorp/terraform-provider-aws/internal/framework"
    )

    // @FrameworkDataSource(name="Example")
    func newResourceExample(_ context.Context) (datasource.ResourceWithConfigure, error) {
    	return &dataSourceExample{}, nil
    }

    type dataSourceExample struct {
	    framework.DataSourceWithConfigure
    }

    func (r *dataSourceExample) Metadata(_ context.Context, request datasource.MetadataRequest, response *datasource.MetadataResponse) {
    	response.TypeName = "aws_something_example"
    }
    ```

=== "Terraform Plugin SDK V2"

    ```go
    package something

    import "github.com/hashicorp/terraform-plugin-sdk/v2/helper/schema"

    // @SDKDataSource("aws_something_example", name="Example")
    func DataSourceExample() *schema.Resource {
    	return &schema.Resource{
    	    // some configuration
    	}
    }
    ```

### Write Passing Acceptance Tests

To adequately test the data source we will need to write a complete set of Acceptance Tests. You will need an AWS account for this which allows the provider to read to state of the associated resource. See [Writing Acceptance Tests](running-and-writing-acceptance-tests.md) for a detailed guide on how to approach these.

You will need at a minimum:

- Basic Test - Tests full lifecycle (CRUD + Import) of a minimal configuration (all required fields, no optional).
- Disappears Test - Tests what Terraform does if a resource it is tracking can no longer be found.
- Per Attribute Tests - For each attribute a test should exist which tests that particular attribute in isolation alongside any required fields.

### Create Documentation for the Data Source

Add a file covering the use of the new data source in `website/docs/d/<service>_<name>.md`. You may want to also add examples of the data source in use particularly if its use is complex, or relies on resources in another service. This documentation will appear on the [Terraform Registry](https://registry.terraform.io/providers/hashicorp/aws/latest) when the data source is made available in a provider release. It is fine to link out to AWS Documentation where appropriate, particularly for values which are likely to change.

### Ensure Format and Lint Checks are Passing Locally

Run `go fmt` to format your code, and install and run all linters to detect and resolve any structural issues with the implementation or documentation.

```sh
make fmt
make tools        # install linters and dependencies
make lint         # run provider linters
make docs-lint    # run documentation linters
make website-lint # run website documentation linters
```

### Raise a Pull Request

See [Raising a Pull Request](raising-a-pull-request.md).

### Wait for Prioritization

In general, pull requests are triaged within a few days of creation and are prioritized based on community reactions. Please view our [prioritization](prioritization.md) guide for full details of the process.
# Adding a New Function

Provider-defined functions were introduced with Terraform 1.8, enabling provider developers to expose functions specific to a given cloud provider or use case.
Functions in the AWS provider provide a utility that is valuable when paired with AWS resources.

See the Terraform Plugin Framework [Function documentation](https://developer.hashicorp.com/terraform/plugin/framework/functions) for additional details.

## Prerequisites

The only prerequisite for creating a function is ensuring the desired functionality is appropriate for a provider-defined function.
Functions must be reproducible across executions ("pure" functions), where the same input always results in the same output.
This requirement precludes the use of network calls, so operations requiring an AWS API call should instead consider utilizing a [data source](add-a-new-datasource.md).
Data manipulation tasks tend to be the most common use cases.

## Steps to add a function

### Fork the provider and create a feature branch

For a new function use a branch named `f-{function name}`, for example, `f-arn_parse`.
See [Raising a Pull Request](raising-a-pull-request.md) for more details.

### Generate function scaffolding

The `skaff function` subcommand can be used to generate an outline for the new function.

First, install `skaff` and navigate to the directory where provider functions are defined (`internal/function`).

```console
make skaff
```

```console
cd internal/function
```

Next, run the `skaff function` subcommand.
The name and description flags are required.
The name argument should be [mixed caps](naming.md#mixed-caps) (ie. `FooBar`), and the generator will handle converting the name to snake case where appropriate.

```console
skaff function -n Example -d "Makes some output from an input."
```

This will generate files storing the function definition, unit tests, and registry documentation.
The following steps describe how to complete the function implementation.

### Fill out the function parameter(s) and return value

The function struct's `Definition` method will document the expected parameters and return value.
Parameter names and return values should be specified in `snake_case`.

```go
func (f exampleFunction) Definition(ctx context.Context, req function.DefinitionRequest, resp *function.DefinitionResponse) {
	resp.Definition = function.Definition{
		Parameters: []function.Parameter{
			function.StringParameter{Name: "some_arg"},
		},
		Return: function.StringReturn{},
	}
}
```

The example above defines a function which accepts a string parameter, `some_arg`, and returns a string value.

### Implement the function logic

The function struct's `Run` method will contain the function logic.
This includes processing the arguments, setting the return value, and any data processing that needs to happen in between.

```go
func (f exampleFunction) Run(ctx context.Context, req function.RunRequest, resp *function.RunResponse) {
	var data string

	resp.Error = function.ConcatFuncErrors(req.Arguments.Get(ctx, &data))
	if resp.Error != nil {
		return
	}

	//
	// Function logic goes here
	//

	resp.Error = function.ConcatFuncErrors(resp.Result.Set(ctx, data))
}
```

### Register function to the provider

Once the function is implemented, it must be registered to the provider to be used.
As only Terraform Plugin Framework supports provider-defined functions, registration occurs on the Plugin Framework provider inside `internal/provider/fwprovider/provider.go`.
Add the `New*` factory function in the `Functions` method to register it.

```go
func (p *fwprovider) Functions(_ context.Context) []func() function.Function {
	return []func() function.Function{
            // Append to list of existing functions here
            tffunction.NewExampleFunction,
	}
}
```

### Write passing acceptance tests

All functions should have corresponding acceptance tests.
For functions with variadic arguments, or which can potentially return an error, tests should be written to exercise those conditions.

An example outline is included below:

```go
// Copyright (c) HashiCorp, Inc.
// SPDX-License-Identifier: MPL-2.0

package function_test

import (
	"fmt"
	"testing"

	"github.com/hashicorp/go-version"
	"github.com/hashicorp/terraform-plugin-testing/helper/resource"
	"github.com/hashicorp/terraform-plugin-testing/tfversion"
	"github.com/hashicorp/terraform-provider-aws/internal/acctest"
)

func TestExampleFunction_basic(t *testing.T) {
	t.Parallel()

	resource.UnitTest(t, resource.TestCase{
		ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
		TerraformVersionChecks: []tfversion.TerraformVersionCheck{
			tfversion.SkipBelow(version.Must(version.NewVersion("1.8.0"))),
		},
		Steps: []resource.TestStep{
			{
				Config: testExampleFunctionConfig("foo"),
				Check: resource.ComposeAggregateTestCheckFunc(
					resource.TestCheckOutput("test", "foo"),
				),
			},
		},
	})
}

func testExampleFunctionConfig(arg string) string {
	return fmt.Sprintf(`
output "test" {
  value = provider::aws::example(%[1]q)
}`, arg)
}
```

With Terraform 1.8+ installed, individual tests can be run like:

```console
go test -run='^TestExampleFunction' -v ./internal/function/
```

### Create documentation for the resource

`skaff` will have generated framed out registry documentation in `website/docs/functions/<function name>.html.markdown`.
The `Example Usage`, `Signature`, and `Arguments` sections should all be updated with the appropriate content.
Once released, this documentation will appear on the [Terraform Registry](https://registry.terraform.io/providers/hashicorp/aws/latest).

### Raise a pull request

See [Raising a Pull Request](raising-a-pull-request.md).

### Wait for prioritization

In general, pull requests are triaged within a few days of creation and are prioritized based on community reactions.
Please view our [Prioritization Guide](prioritization.md) for full details of the process.
# Adding a Newly Released AWS Region

New regions can typically be used immediately with the provider, with two important caveats:

- Regions often need to be explicitly enabled via the AWS console. See [ap-east-1 launch blog](https://aws.amazon.com/blogs/aws/now-open-aws-asia-pacific-hong-kong-region/) for an example of how to enable a new region for use.
- Until the provider is aware of the new region, automatic region validation will fail. To use the region before validation support is added to the provider you will need to disable region validation by doing the following:

```terraform
provider "aws" {
  # ... potentially other configuration ...

  region                 = "me-south-1"
  skip_region_validation = true
}
```

## Enabling Region Validation

Support for region validation requires that the provider has an updated [AWS SDK Go Base](aws-sdk-go-base.md) dependency that includes the new region. This also needs to be done in the core Terraform binary itself to enable it for the S3 backend. Many of the authentication and provider-level configuration interactions are also located in the `aws-go-sdk-base` library. As all of these things take direct dependencies and as a result there end up being quite a few places where these dependency updates need to be made.

### Update aws-go-sdk-base

[aws-go-sdk-base](https://github.com/hashicorp/aws-sdk-go-base)

- Update [aws-go-sdk-v2](https://github.com/aws/aws-sdk-go-v2)

### Update Terraform AWS Provider

[provider](https://github.com/hashicorp/terraform-provider-aws)

- Update [aws-go-sdk-v2](https://github.com/aws/aws-sdk-go-v2)
- Update [aws-go-sdk-base](https://github.com/hashicorp/aws-sdk-go-base)

### Update Terraform Core (S3 Backend)

[core](https://github.com/hashicorp/terraform)

- Update [aws-go-sdk-v2](https://github.com/aws/aws-sdk-go-v2)
- Update [aws-go-sdk-base](https://github.com/hashicorp/aws-sdk-go-base)

See the [Changelog Process](changelog-process.md) document for example changelog format.

## Update Region Specific values in static Data Sources

Some data sources include static values specific to regions that are not available via a standard AWS API call. These will need to be manually updated. AWS employees can code search previous region values to find new region values in internal packages like RIPStaticConfig if they are not documented yet.

- Check [Elastic Load Balancing endpoints and quotas](https://docs.aws.amazon.com/general/latest/gr/elb.html#elb_region) and add Route53 Hosted Zone ID if available to [`internal/service/elb/hosted_zone_id_data_source.go`](https://github.com/hashicorp/terraform-provider-aws/tree/main/internal/service/elb/hosted_zone_id_data_source.go) and [`internal/service/elbv2/hosted_zone_id_data_source.go`](https://github.com/hashicorp/terraform-provider-aws/tree/main/internal/service/elbv2/hosted_zone_id_data_source.go)
- Check [Amazon Simple Storage Service endpoints and quotas](https://docs.aws.amazon.com/general/latest/gr/s3.html#s3_website_region_endpoints) and add Route53 Hosted Zone ID if available to [`internal/service/s3/hosted_zones.go`](https://github.com/hashicorp/terraform-provider-aws/tree/main/internal/service/s3/hosted_zones.go)
- Check [AWS Elastic Beanstalk endpoints and quotas](https://docs.aws.amazon.com/general/latest/gr/elasticbeanstalk.html) and add Route53 Hosted Zone ID if available to [`internal/service/elasticbeanstalk/hosted_zone_data_source.go`](https://github.com/hashicorp/terraform-provider-aws/tree/main/internal/service/elasticbeanstalk/hosted_zone_data_source.go)
- Check [SageMaker docs](https://docs.aws.amazon.com/sagemaker/latest/dg/sagemaker-algo-docker-registry-paths.html) and add AWS Account IDs if available to [`internal/service/sagemaker/prebuilt_ecr_image_data_source.go`](https://github.com/hashicorp/terraform-provider-aws/tree/main/internal/service/sagemaker/prebuilt_ecr_image_data_source.go)
- Check [App Runner docs](https://docs.aws.amazon.com/general/latest/gr/apprunner.html#apprunner_region) and add Route53 Hosted Zone ID if available to [`internal/service/apprunner/hosted_zone_id_data_source.go`](https://github.com/hashicorp/terraform-provider-aws/tree/main/internal/service/apprunner/hosted_zone_id_data_source.go)
<!-- markdownlint-configure-file { "code-block-style": false } -->
# Adding a New Resource

New resources are required when AWS adds a new service, or adds new features within an existing service which would require a new resource to manage in Terraform. Typically anything with a new set of CRUD API endpoints is a great candidate for a new resource.

Each resource should be submitted for review in isolation. Pull requests containing multiple resources are harder to review and the maintainers will normally ask for them to be broken apart.

## Prerequisites

If this is the first resource for a new service, please ensure the Service Client for the new service has been added and merged. See [Adding a new Service](add-a-new-service.md) for details.

## Steps to Add a Resource

### Fork the provider and create a feature branch

For new resources use a branch named `f-{resource name}` for example: `f-ec2-vpc`. See [Raising a Pull Request](raising-a-pull-request.md) for more details.

### Create and Name the Resource

See the [Naming Guide](naming.md#resources-and-data-sources) for details on how to name the new resource and the resource file. Not following the naming standards will cause extra delay as maintainers request that you make changes.

Use the [skaff](skaff.md) provider scaffolding tool to generate new resource and test templates using your chosen name. Doing so will ensure that any boilerplate code, structural best practices and repetitive naming are done for you and always represent our most current standards.

### Fill out the Resource Schema

In the `internal/service/<service>/<service>.go` file you will see a `Schema` property which exists as a map of `Schema` objects. This relates the AWS API data model with the Terraform resource itself. For each property you want to make available in Terraform, you will need to add it as an attribute, choose the correct data type and supply the correct [Schema Behaviors](https://www.terraform.io/plugin/sdkv2/schemas/schema-behaviors) to ensure Terraform knows how to correctly handle the value.

Typically you will add arguments to represent the values that are under control by Terraform, and attributes to supply read-only values as references for Terraform. These are distinguished by Schema Behavior.

Attribute names are to be specified in `snake_case` as opposed to the AWS API which is `CamelCase`.

### Implement CRUD handlers

These will map the planned Terraform state to the AWS API call, or an AWS API response to an applied Terraform state. You will also need to handle different response types (including errors correctly). For complex attributes, you will need to implement Flattener or Expander functions. The [Data Handling and Conversion Guide](data-handling-and-conversion.md) covers everything you need to know for mapping AWS API responses to Terraform State and vice-versa. The [Error Handling Guide](error-handling.md) covers everything you need to know about handling AWS API responses consistently.

### Register Resource to the provider

Resources use a self-registration process that adds them to the provider using the `@FrameworkResource()` or `@SDKResource()` annotation in the resource's comments. Run `make gen` to register the resource. This will add an entry to the `service_package_gen.go` file located in the service package folder.

=== "Terraform Plugin Framework (Preferred)"

    ```go
    package something

    import (
        "github.com/hashicorp/terraform-plugin-framework/resource"
        "github.com/hashicorp/terraform-provider-aws/internal/framework"
    )

    // @FrameworkResource("aws_something_example", name="Example")
    func newResourceExample(_ context.Context) (resource.ResourceWithConfigure, error) {
    	return &resourceExample{}, nil
    }

    type resourceExample struct {
    	framework.ResourceWithConfigure
    }

    func (r *resourceExample) Metadata(_ context.Context, request resource.MetadataRequest, response *resource.MetadataResponse) {
    	response.TypeName = "aws_something_example"
    }
    ```

=== "Terraform Plugin SDK V2"

    ```go
    package something

    import "github.com/hashicorp/terraform-plugin-sdk/v2/helper/schema"

    // @SDKResource("aws_something_example", name="Example)
    func ResourceExample() *schema.Resource {
    	return &schema.Resource{
    	    // some configuration
    	}
    }
    ```

### Write passing Acceptance Tests

To adequately test the resource we will need to write a complete set of Acceptance Tests. You will need an AWS account for this which allows the creation of that resource. See [Writing Acceptance Tests](running-and-writing-acceptance-tests.md) for a detailed guide on how to approach these.

You will need at a minimum:

- Basic Test - Tests full lifecycle (CRUD + Import) of a minimal configuration (all required fields, no optional).
- Disappears Test - Tests what Terraform does if a resource it is tracking can no longer be found.
- Argument Tests - All arguments should be tested in a pragmatic way. Ensure that each argument can be initially set, updated, and cleared, as applicable. Depending on the logic and interaction of arguments, this may take one to several separate tests.

### Create documentation for the resource

Add a file covering the use of the new resource in `website/docs/r/<service>_<name>.md`. Add more examples if it is complex or relies on resources in another service. This documentation will appear on the [Terraform Registry](https://registry.terraform.io/providers/hashicorp/aws/latest) when the resource is made available in a provider release. Link to AWS Documentation where appropriate, particularly for values which are likely to change.

### Ensure format and lint checks are passing locally

Format your code and check linters to detect various issues.

```sh
make fmt
make tools     # install linters and dependencies
make lint      # run provider linters
make docs-lint # run documentation linters
```

### Raise a Pull Request

See [Raising a Pull Request](raising-a-pull-request.md).

### Wait for Prioritization

In general, pull requests are triaged within a few days of creation and are prioritized based on community reactions. Please view our [Prioritization Guide](prioritization.md) for full details of the process.
<!-- markdownlint-configure-file { "code-block-style": false } -->
# Adding a New AWS Service

AWS frequently launches new services, and Terraform support is frequently desired by the community shortly after launch. Depending on the API surface area of the new service, this could be a major undertaking. The following steps should be followed to prepare for adding the resources that allow for Terraform management of that service.

## Perform Service Design

Before adding a new service to the provider it's a good idea to familiarize yourself with the primary workflows practitioners are likely to want to accomplish with the provider to ensure the provider design can solve this. It's not always necessary to cover 100% of the AWS service offering to unblock most workflows.

You should have an idea of what resources and data sources should be added, their dependencies and relative importance concerning the workflow. This should give you an idea of the order in which resources are to be added. It's important to note that generally, we like to review and merge resources in isolation, and avoid combining multiple new resources in one Pull Request.

Using the AWS API documentation as a reference, identify the various APIs that correspond to the CRUD operations which consist of the management surface for that resource. These will be the set of APIs called from the new resource. The API's model attributes will correspond to your resource schema.

From there begin to map out the list of resources you would like to implement, and note your plan on the GitHub issue relating to the service (or create one if one does not exist) for the community and maintainers to feedback.

## Add a Service Client

Before new resources are submitted, please raise a separate pull request containing just the new AWS SDK for Go service client.

To add an AWS SDK for Go service client:

1. Check the file `names/data/names_data.hcl` for the service.

1. If the service is there and the `not_implemented` attribute does not exist, you are ready to implement the first [resource](./add-a-new-resource.md) or [data source](./add-a-new-datasource.md).

1. If the service is there and the `not_implemented` attribute is true, remove it and submit the client pull request as described below.

1. Otherwise, determine the service identifier using the rule described in [the Naming Guide](naming.md#service-identifier).

1. In `names/data/names_data.hcl`, add a new hcl block with all the requested information for the service following the guidance in the [`names` README](https://github.com/hashicorp/terraform-provider-aws/blob/main/names/README.md).

    !!! tip
        Be very careful when adding or changing data in `names_data.hcl`!
        The Provider and generators depend on the file being correct.
        We strongly recommend using an editor with HCL support.

Once the names data is ready, create a new service directory with the appropriate service name.

```console
mkdir internal/service/<service>
```

Add a new file `internal/service/<service>/generate.go` with the following content. This will generate the structs required for [resource self-registration](./add-a-new-resource.md#register-resource-to-the-provider).

```go
// Copyright (c) HashiCorp, Inc.
// SPDX-License-Identifier: MPL-2.0

//go:generate go run ../../generate/servicepackage/main.go
// ONLY generate directives and package declaration! Do not add anything else to this file.

package <service>
```

Next, generate the client and ensure all dependencies are fetched.

```console
make gen
```

```console
go mod tidy
```

At this point a pull request with the re-generated files and new service client can be submitted.

Once the service client has been added, implement the first [resource](./add-a-new-resource.md) or [data source](./add-a-new-datasource.md) in a separate PR.

## Adding a Custom Service Client

If an AWS service must be created in a non-standard way, for example, the service API's endpoint must be accessed via a single AWS Region, then:

1. Make the `skip_client_generate` attribute `true` for the service in [`names/data/names_data.hcl`](https://github.com/hashicorp/terraform-provider-aws/blob/main/names/README.md)

1. Run `make gen`

1. Add a file `internal/<service>/service_package.go` that contains an API client factory function, for example:

    ```go
    package costoptimizationhub

    import (
        "context"

        "github.com/aws/aws-sdk-go-v2/aws"
        "github.com/aws/aws-sdk-go-v2/service/costoptimizationhub"
        "github.com/hashicorp/terraform-provider-aws/names"
    )

    // NewClient returns a new AWS SDK for Go v2 client for this service package's AWS API.
    func (p *servicePackage) NewClient(ctx context.Context, config map[string]any) (*costoptimizationhub.Client, error) {
        cfg := *(config["aws_sdkv2_config"].(*aws.Config))

        return costoptimizationhub.NewFromConfig(cfg,
            costoptimizationhub.WithEndpointResolverV2(newEndpointResolverSDKv2()),
            withBaseEndpoint(config[names.AttrEndpoint].(string)),
            func(o *costoptimizationhub.Options) {
                if config["partition"].(string) == names.StandardPartitionID {
                    // Cost Optimization Hub endpoint is available only in us-east-1 Region.
                    if cfg.Region != names.USEast1RegionID {
                        tflog.Info(ctx, "overriding region", map[string]any{
                            "original_region": cfg.Region,
                            "override_region": names.USEast1RegionID,
                        })
                        o.Region = names.USEast1RegionID
                    }
                }
            },
        ), nil
    }
    ```

## Customizing a new Service Client

If an AWS service must be customized after creation, for example, retry handling must be changed, then:

1. Add a file `internal/<service>/service_package.go` that contains an API client customization function, for example:

```go
package shield

import (
	"context"

	"github.com/aws/aws-sdk-go-v2/aws"
	"github.com/aws/aws-sdk-go-v2/service/shield"
	"github.com/hashicorp/aws-sdk-go-base/v2/endpoints"
	"github.com/hashicorp/terraform-plugin-log/tflog"
	"github.com/hashicorp/terraform-provider-aws/names"
)

// NewClient returns a new AWS SDK for Go v2 client for this service package's AWS API.
func (p *servicePackage) NewClient(ctx context.Context, config map[string]any) (*shield.Client, error) {
	cfg := *(config["aws_sdkv2_config"].(*aws.Config))

	return shield.NewFromConfig(cfg,
		shield.WithEndpointResolverV2(newEndpointResolverV2()),
		withBaseEndpoint(config[names.AttrEndpoint].(string)),
		func(o *shield.Options) {
			// Force "global" services to correct Regions.
			if config["partition"].(string) == endpoints.AwsPartitionID {
				if cfg.Region != names.USEast1RegionID {
					tflog.Info(ctx, "overriding region", map[string]any{
						"original_region": cfg.Region,
						"override_region": names.USEast1RegionID,
					})
					o.Region = names.USEast1RegionID
				}
			}
		},
	), nil
}
```
# Adding Resource Import Support

Adding import support for Terraform resources will allow existing infrastructure to be managed within Terraform. This type of enhancement generally requires a small to moderate amount of code changes. Comprehensive code examples and information about resource import support can be found in the [Terraform Plugin Framework documentation](https://developer.hashicorp.com/terraform/plugin/framework/resources/import).

- _Resource Code_: In the resource code (e.g., `internal/service/{service}/{thing}.go`),
    - **Plugin Framework (Preferred)** Implement the `ImportState` method on the resource struct. When possible, prefer using the [`resource.ImportStatePassthroughID` function](https://pkg.go.dev/github.com/hashicorp/terraform-plugin-framework/resource#ImportStatePassthroughID).
    - **Plugin SDK V2**: Implement an `Importer` `State` function. When possible, prefer using [`schema.ImportStatePassthroughContext`](https://www.terraform.io/plugin/sdkv2/resources/import#importer-state-function).
- _Resource Acceptance Tests_: In the resource acceptance tests (e.g., `internal/service/{service}/{thing}_test.go`), implement one or more tests containing a `TestStep` with `ImportState: true`.
- _Resource Documentation_: In the resource documentation (e.g., `website/docs/r/service_thing.html.markdown`), add an `Import` section at the bottom of the page.
# Adding a New Tag Resource

Adding a tag resource, similar to the `aws_ecs_tag` resource, has its own implementation procedure since the resource code and initial acceptance testing functions are automatically generated. The rest of the resource acceptance testing and resource documentation must still be manually created.

- In `internal/generate`: Ensure the service is supported by all generators. Run `make gen` after any modifications.
- In `internal/service/{service}/generate.go`: Add the new `//go:generate` call with the correct generator directives. Run `make gen` after any modifications.
- In `internal/provider/provider.go`: Add the new resource.
- Run `make test` and ensure there are no failures.
- Create `internal/service/{service}/tag_gen_test.go` with initial acceptance testing similar to the following (where the parent resource is simple to provision):

```go
import (
	"fmt"
	"testing"

	"github.com/hashicorp/terraform-plugin-testing/helper/acctest"
	"github.com/hashicorp/terraform-plugin-testing/helper/resource"
	"github.com/hashicorp/terraform-provider-aws/names"
)

func TestAcc{Service}Tag_basic(t *testing.T) {
	ctx := acctest.Context(t)
	rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)
	resourceName := "aws_{service}_tag.test"

	resource.ParallelTest(t, resource.TestCase{
		PreCheck:                 func() { acctest.PreCheck(ctx, t) },
		ErrorCheck:               acctest.ErrorCheck(t, names.{Service}ServiceID),
		ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
		CheckDestroy:             testAccCheck{Service}TagDestroy(ctx),
		Steps: []resource.TestStep{
			{
				Config: testAcc{Service}TagConfig(rName, "key1", "value1"),
				Check: resource.ComposeTestCheckFunc(
					testAccCheck{Service}TagExists(ctx, resourceName),
					resource.TestCheckResourceAttr(resourceName, "key", "key1"),
					resource.TestCheckResourceAttr(resourceName, "value", "value1"),
				),
			},
			{
				ResourceName:      resourceName,
				ImportState:       true,
				ImportStateVerify: true,
			},
		},
	})
}

func TestAcc{Service}Tag_disappears(t *testing.T) {
	ctx := acctest.Context(t)
	rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)
	resourceName := "aws_{service}_tag.test"

	resource.ParallelTest(t, resource.TestCase{
		PreCheck:                 func() { acctest.PreCheck(ctx, t) },
		ErrorCheck:               acctest.ErrorCheck(t, names.{Service}ServiceID),
		ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
		CheckDestroy:             testAccCheck{Service}TagDestroy(ctx),
		Steps: []resource.TestStep{
			{
				Config: testAcc{Service}TagConfig(rName, "key1", "value1"),
				Check: resource.ComposeTestCheckFunc(
					testAccCheck{Service}TagExists(ctx, resourceName),
					acctest.CheckResourceDisappears(ctx, acctest.Provider, resourceAws{Service}Tag(), resourceName),
				),
				ExpectNonEmptyPlan: true,
			},
		},
	})
}

func TestAcc{Service}Tag_Value(t *testing.T) {
	ctx := acctest.Context(t)
	rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)
	resourceName := "aws_{service}_tag.test"

	resource.ParallelTest(t, resource.TestCase{
		PreCheck:                 func() { acctest.PreCheck(ctx, t) },
		ErrorCheck:               acctest.ErrorCheck(t, names.{Service}ServiceID),
		ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
		CheckDestroy:             testAccCheck{Service}TagDestroy(ctx),
		Steps: []resource.TestStep{
			{
				Config: testAcc{Service}TagConfig(rName, "key1", "value1"),
				Check: resource.ComposeTestCheckFunc(
					testAccCheck{Service}TagExists(ctx, resourceName),
					resource.TestCheckResourceAttr(resourceName, "key", "key1"),
					resource.TestCheckResourceAttr(resourceName, "value", "value1"),
				),
			},
			{
				ResourceName:      resourceName,
				ImportState:       true,
				ImportStateVerify: true,
			},
			{
				Config: testAcc{Service}TagConfig(rName, "key1", "value1updated"),
				Check: resource.ComposeTestCheckFunc(
					testAccCheck{Service}TagExists(ctx, resourceName),
					resource.TestCheckResourceAttr(resourceName, "key", "key1"),
					resource.TestCheckResourceAttr(resourceName, "value", "value1updated"),
				),
			},
		},
	})
}

func testAcc{Service}TagConfig(rName string, key string, value string) string {
	return fmt.Sprintf(`
resource "aws_{service}_{thing}" "test" {
  name = %[1]q

  lifecycle {
    ignore_changes = [tags]
  }
}

resource "aws_{service}_tag" "test" {
  resource_arn = aws_{service}_{thing}.test.arn
  key          = %[2]q
  value        = %[3]q
}
`, rName, key, value)
}
```

- Run `make testacc TESTS=TestAcc{Service}Tags_ PKG={Service}` and ensure there are no failures.
- Create `website/docs/r/{service}_tag.html.markdown` with initial documentation similar to the following:

``````markdown
---
subcategory: "{SERVICE}"
layout: "aws"
page_title: "AWS: aws_{service}_tag"
description: |-
  Manages an individual {SERVICE} resource tag
---

# Resource: aws_{service}_tag

Manages an individual {SERVICE} resource tag. This resource should only be used in cases where {SERVICE} resources are created outside Terraform (e.g., {SERVICE} {THING}s implicitly created by {OTHER SERVICE THING}).

~> **NOTE:** This tagging resource should not be combined with the Terraform resource for managing the parent resource. For example, using `aws_{service}_{thing}` and `aws_{service}_tag` to manage tags of the same {SERVICE} {THING} will cause a perpetual difference where the `aws_{service}_{thing}` resource will try to remove the tag being added by the `aws_{service}_tag` resource.

~> **NOTE:** This tagging resource does not use the [provider `ignore_tags` configuration](/docs/providers/aws/index.html#ignore_tags).

## Example Usage

```terraform
resource "aws_{service}_tag" "example" {
  resource_arn = "..."
  key          = "Name"
  value        = "Hello World"
}
```

## Argument Reference

This resource supports the following arguments:

* `resource_arn` - (Required) ARN of the {SERVICE} resource to tag.
* `key` - (Required) Tag name.
* `value` - (Required) Tag value.

## Attribute Reference

This resource exports the following attributes in addition to the arguments above:

* `id` - {SERVICE} resource identifier and key, separated by a comma (`,`)

## Import

Import `aws_{service}_tag` using the {SERVICE} resource identifier and key, separated by a comma (`,`). For example:

```console
$ terraform import aws_{service}_tag.example arn:aws:{service}:us-east-1:123456789012:{thing}/example,Name
```
``````
# AWS SDK Go Base

[AWS SDK Go Base](https://github.com/hashicorp/aws-sdk-go-base) is a shared library used by the [AWS Provider](https://github.com/hashicorp/terraform-provider-aws), [AWSCC Provider](https://github.com/hashicorp/terraform-provider-awscc) and the [Terraform S3 Backend](https://github.com/hashicorp/terraform/tree/main/internal/backend/remote-state/s3) to handle authentication and other non-service level AWS interactions consistently.

Changes are infrequent and normally performed by HashiCorp maintainers.
It should not be necessary to change this library for the majority of provider contributions.
# Making Small Changes to Existing Resources

Most contributions to the provider will take the form of small additions or bug-fixes on existing resources/data sources. In this case the existing resource will give you the best guidance on how the change should be structured, but we require the following to allow the change to be merged:

- __Acceptance test coverage of new behavior__: Existing resources each
   have a set of [acceptance tests](running-and-writing-acceptance-tests.md) covering their functionality.
   These tests should exercise all the behavior of the resource. Whether you are
   adding something or fixing a bug, the idea is to have an acceptance test that
   fails if your code were to be removed. Sometimes it is sufficient to
   "enhance" an existing test by adding an assertion or tweaking the config
   that is used, but it's often better to add a new test. You can copy/paste an
   existing test and follow the conventions you see there, modifying the test
   to exercise the behavior of your code.
- __Documentation updates__: If your code makes any changes that need to
   be documented, you should include those [documentation changes](documentation-changes.md)
   in the same PR. This includes things like new resource attributes or changes in default values.
- __Well-formed Code__: Do your best to follow existing conventions you
   see in the codebase, and ensure your code is formatted with `go fmt`.
   The PR reviewers can help out on this front, and may provide comments with
   suggestions on how to improve the code.
- __Dependency updates__: Create a separate PR if you are updating dependencies.
   This is to avoid conflicts as version updates tend to be fast-
   moving targets. We will plan to merge the PR with this change first.
- __Changelog entry__: Assuming the code change affects Terraform operators,
   the relevant PR ought to include a user-facing [changelog entry](changelog-process.md)
   describing the new behavior.
# Changelog Process

HashiCorp’s open-source projects have always maintained user-friendly, readable `CHANGELOG.md` that allows users to tell at a glance whether a release should have any effect on them, and to gauge the risk of an upgrade.

We use [go-changelog](https://github.com/hashicorp/go-changelog) to generate the changelog from files created in the `.changelog/` directory.
It is important that when you raise your pull request, there is a changelog entry which describes the changes your contribution makes.
Not all changes require an entry in the changelog, guidance follows on what changes do.

## Changelog format

The changelog format requires an entry in the following format, where HEADER corresponds to the changelog category, and the entry is the changelog entry itself. The entry should be included in a file in the `.changelog` directory with the naming convention `{PR-NUMBER}.txt`. For example, to create a changelog entry for pull request 1234, there should be a file named `.changelog/1234.txt`.

``````
```release-note:{HEADER}
{ENTRY}
```
``````

If a pull request should contain multiple changelog entries, then multiple blocks can be added to the same changelog file. For example:

``````
```release-note:note
resource/aws_example_thing: The `broken` attribute has been deprecated. All configurations using `broken` should be updated to use the new `not_broken` attribute instead.
```

```release-note:enhancement
resource/aws_example_thing: Add `not_broken` attribute
```
``````

## Pull request types to CHANGELOG

The CHANGELOG is intended to show operator-impacting changes to the codebase for a particular version. If every change or commit to the code resulted in an entry, the CHANGELOG would become less useful for operators. The lists below are general guidelines and examples for when a decision needs to be made to decide whether a change should have an entry.

### Changes that should have a CHANGELOG entry

#### New resource

A new resource entry should only contain the name of the resource, and use the `release-note:new-resource` header.

``````
```release-note:new-resource
aws_secretsmanager_secret_policy
```
``````

#### New data source

A new data source entry should only contain the name of the data source, and use the `release-note:new-data-source` header.

``````
```release-note:new-data-source
aws_workspaces_workspace
```
``````

#### New full-length documentation guides (e.g., EKS Getting Started Guide, IAM Policy Documents with Terraform)

A new full-length documentation entry gives the title of the documentation added, using the `release-note:new-guide` header.

``````
```release-note:new-guide
Custom Service Endpoint Configuration
```
``````

#### Resource and provider bug fixes

A new bug entry should use the `release-note:bug` header and have a prefix indicating the resource or data source it corresponds to, a colon, then followed by a brief summary. Use a `provider` prefix for provider-level fixes.

``````
```release-note:bug
resource/aws_glue_classifier: Fix quote_symbol being optional
```
``````

#### Resource and provider enhancements

A new enhancement entry should use the `release-note:enhancement` header and have a prefix indicating the resource or data source it corresponds to, a colon, then followed by a brief summary. Use a `provider` prefix for provider-level enhancements.

``````
```release-note:enhancement
resource/aws_eip: Add network_border_group argument
```
``````

#### Deprecations

A deprecation entry should use the `release-note:note` header and have a prefix indicating the resource or data source it corresponds to, a colon, then followed by a brief summary. Use a `provider` prefix for provider-level changes.

``````
```release-note:note
resource/aws_dx_gateway_association: The vpn_gateway_id attribute is being deprecated in favor of the new associated_gateway_id attribute to support transit gateway associations
```
``````

#### Breaking changes and removals

A breaking-change entry should use the `release-note:breaking-change` header and have a prefix indicating the resource or data source it corresponds to, a colon, then followed by a brief summary. Use a `provider` prefix for provider-level changes.

``````
```release-note:breaking-change
resource/aws_lambda_alias: Resource import no longer converts Lambda Function name to ARN
```
``````

#### Region validation support

``````
```release-note:note
provider: Region validation now automatically supports the new `XX-XXXXX-#` (Location) region. For AWS operations to work in the new region, the region must be explicitly enabled as outlined in the [AWS Documentation](https://docs.aws.amazon.com/general/latest/gr/rande-manage.html#rande-manage-enable). When the region is not enabled, the Terraform AWS Provider will return errors during credential validation (e.g., `error validating provider credentials: error calling sts:GetCallerIdentity: InvalidClientTokenId: The security token included in the request is invalid`) or AWS operations will throw their own errors (e.g., `data.aws_availability_zones.available: Error fetching Availability Zones: AuthFailure: AWS was not able to validate the provided access credentials`). [GH-####]
```

```release-note:enhancement
provider: Support automatic region validation for `XX-XXXXX-#` [GH-####]
```
``````

### Changes that may have a CHANGELOG entry

Dependency updates: If the update contains relevant bug fixes or enhancements that affect operators, those should be called out.
Any changes which do not fit into the above categories but warrant highlighting.
Use resource/data source/provider prefixes where appropriate.

``````
```release-note:note
resource/aws_lambda_alias: Resource import no longer converts Lambda Function name to ARN
```
``````

### Changes that should _not_ have a CHANGELOG entry

- Resource and provider documentation updates
- Testing updates
- Code refactoring
# Acceptance Testing Environment Variable Dictionary

Environment variables (beyond standard AWS Go SDK ones) used by acceptance testing. See also the `internal/acctest` package.

| Variable | Description |
|----------|-------------|
| `ACM_CERTIFICATE_ROOT_DOMAIN` | Root domain name to use with ACM Certificate testing. |
| `ADM_CLIENT_ID` | Identifier for Amazon Device Manager Client in Pinpoint testing. |
| `AMPLIFY_DOMAIN_NAME` | Domain name to use for Amplify domain association testing. |
| `AMPLIFY_GITHUB_ACCESS_TOKEN` | GitHub access token used for AWS Amplify testing. |
| `AMPLIFY_GITHUB_REPOSITORY` | GitHub repository used for AWS Amplify testing. |
| `ADM_CLIENT_SECRET` | Secret for Amazon Device Manager Client in Pinpoint testing. |
| `APNS_BUNDLE_ID` | Identifier for Apple Push Notification Service Bundle in Pinpoint testing. |
| `APNS_CERTIFICATE` | Certificate (PEM format) for Apple Push Notification Service in Pinpoint testing. |
| `APNS_CERTIFICATE_PRIVATE_KEY` | Private key for Apple Push Notification Service in Pinpoint testing. |
| `APNS_SANDBOX_BUNDLE_ID` | Identifier for Sandbox Apple Push Notification Service Bundle in Pinpoint testing. |
| `APNS_SANDBOX_CERTIFICATE` | Certificate (PEM format) for Sandbox Apple Push Notification Service in Pinpoint testing. |
| `APNS_SANDBOX_CERTIFICATE_PRIVATE_KEY` | Private key for Sandbox Apple Push Notification Service in Pinpoint testing. |
| `APNS_SANDBOX_CREDENTIAL` | Credential contents for Sandbox Apple Push Notification Service in SNS Application Platform testing. Conflicts with `APNS_SANDBOX_CREDENTIAL_PATH`. |
| `APNS_SANDBOX_CREDENTIAL_PATH` | Path to credential for Sandbox Apple Push Notification Service in SNS Application Platform testing. Conflicts with `APNS_SANDBOX_CREDENTIAL`. |
| `APNS_SANDBOX_PRINCIPAL` | Principal contents for Sandbox Apple Push Notification Service in SNS Application Platform testing. Conflicts with `APNS_SANDBOX_PRINCIPAL_PATH`. |
| `APNS_SANDBOX_PRINCIPAL_PATH` | Path to the principal for Sandbox Apple Push Notification Service in SNS Application Platform testing. Conflicts with `APNS_SANDBOX_PRINCIPAL`. |
| `APNS_SANDBOX_TEAM_ID` | Identifier for Sandbox Apple Push Notification Service Team in Pinpoint testing. |
| `APNS_SANDBOX_TOKEN_KEY` | Token key file content (.p8 format) for Sandbox Apple Push Notification Service in Pinpoint testing. |
| `APNS_SANDBOX_TOKEN_KEY_ID` | Identifier for Sandbox Apple Push Notification Service Token Key in Pinpoint testing. |
| `APNS_TEAM_ID` | Identifier for Apple Push Notification Service Team in Pinpoint testing. |
| `APNS_TOKEN_KEY` | Token key file content (.p8 format) for Apple Push Notification Service in Pinpoint testing. |
| `APNS_TOKEN_KEY_ID` | Identifier for Apple Push Notification Service Token Key in Pinpoint testing. |
| `APNS_VOIP_BUNDLE_ID` | Identifier for VOIP Apple Push Notification Service Bundle in Pinpoint testing. |
| `APNS_VOIP_CERTIFICATE` | Certificate (PEM format) for VOIP Apple Push Notification Service in Pinpoint testing. |
| `APNS_VOIP_CERTIFICATE_PRIVATE_KEY` | Private key for VOIP Apple Push Notification Service in Pinpoint testing. |
| `APNS_VOIP_TEAM_ID` | Identifier for VOIP Apple Push Notification Service Team in Pinpoint testing. |
| `APNS_VOIP_TOKEN_KEY` | Token key file content (.p8 format) for VOIP Apple Push Notification Service in Pinpoint testing. |
| `APNS_VOIP_TOKEN_KEY_ID` | Identifier for VOIP Apple Push Notification Service Token Key in Pinpoint testing. |
| `APPRUNNER_CUSTOM_DOMAIN` | A custom domain endpoint (root domain, subdomain, or wildcard) for AppRunner Custom Domain Association testing. |
| `AUDITMANAGER_DEREGISTER_ACCOUNT_ON_DESTROY` | Flag to execute tests that will disable AuditManager in the account upon destruction. |
| `AUDITMANAGER_ORGANIZATION_ADMIN_ACCOUNT_ID` | Organization admin account identifier for use in AuditManager testing. |
| `AWS_ALTERNATE_ACCESS_KEY_ID` | AWS access key ID with access to a secondary AWS account for tests requiring multiple accounts. Requires `AWS_ALTERNATE_SECRET_ACCESS_KEY`. Conflicts with `AWS_ALTERNATE_PROFILE`. |
| `AWS_ALTERNATE_SECRET_ACCESS_KEY` | AWS secret access key with access to a secondary AWS account for tests requiring multiple accounts. Requires `AWS_ALTERNATE_ACCESS_KEY_ID`. Conflicts with `AWS_ALTERNATE_PROFILE`. |
| `AWS_ALTERNATE_PROFILE` | AWS profile with access to a secondary AWS account for tests requiring multiple accounts. Conflicts with `AWS_ALTERNATE_ACCESS_KEY_ID` and `AWS_ALTERNATE_SECRET_ACCESS_KEY`. |
| `AWS_ALTERNATE_REGION` | Secondary AWS region for tests requiring multiple regions. Defaults to `us-east-1`. |
| `AWS_API_GATEWAY_DOMAIN_NAME_CERTIFICATE_BODY` | Certificate body of publicly trusted certificate for API Gateway Domain Name testing. |
| `AWS_API_GATEWAY_DOMAIN_NAME_CERTIFICATE_CHAIN` | Certificate chain of publicly trusted certificate for API Gateway Domain Name testing. |
| `AWS_API_GATEWAY_DOMAIN_NAME_CERTIFICATE_PRIVATE_KEY` | Private key of publicly trusted certificate for API Gateway Domain Name testing. |
| `AWS_API_GATEWAY_DOMAIN_NAME_REGIONAL_CERTIFICATE_NAME_ENABLED` | Flag to enable API Gateway Domain Name regional certificate upload testing. |
| `AWS_CODEBUILD_BITBUCKET_SOURCE_LOCATION` | BitBucket source URL for CodeBuild testing. CodeBuild must have access to this repository via OAuth or Source Credentials. Defaults to `https://terraform@bitbucket.org/terraform/aws-test.git`. |
| `AWS_CODEBUILD_GITHUB_SOURCE_LOCATION` | GitHub source URL for CodeBuild testing. CodeBuild must have access to this repository via OAuth or Source Credentials. Defaults to `https://github.com/hashibot-test/aws-test.git`. |
| `AWS_DEFAULT_REGION` | Primary AWS region for tests. Defaults to `us-west-2`. |
| `AWS_DETECTIVE_MEMBER_EMAIL` | Email address for Detective Member testing. A valid email address associated with an AWS root account is required for tests to pass. |
| `AWS_EC2_CLIENT_VPN_LIMIT` | Concurrency limit for Client VPN acceptance tests. [Default is 5](https://docs.aws.amazon.com/vpn/latest/clientvpn-admin/limits.html) if not specified. |
| `AWS_EC2_EIP_PUBLIC_IPV4_POOL` | Identifier for EC2 Public IPv4 Pool for EC2 EIP testing. |
| `AWS_EC2_TRANSIT_GATEWAY_LIMIT` | Concurrency limit for Transit Gateway acceptance tests. [Default is 5](https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-quotas.html) if not specified. |
| `AWS_EC2_VERIFIED_ACCESS_INSTANCE_LIMIT` | Concurrency limit for Verified Access acceptance tests. [Default is 5](https://docs.aws.amazon.com/verified-access/latest/ug/verified-access-quotas.html) if not specified. |
| `AWS_GUARDDUTY_MEMBER_ACCOUNT_ID` | Identifier of AWS Account for GuardDuty Member testing. **DEPRECATED:** Should be replaced with standard alternate account handling for tests. |
| `AWS_GUARDDUTY_MEMBER_EMAIL` | Email address for GuardDuty Member testing. **DEPRECATED:** It may be possible to use a placeholder email address instead. |
| `AWS_LAMBDA_IMAGE_LATEST_ID` | ECR repository image URI (tagged as `latest`) for Lambda container image acceptance tests. |
| `AWS_LAMBDA_IMAGE_V1_ID` | ECR repository image URI (tagged as `v1`) for Lambda container image acceptance tests. |
| `AWS_LAMBDA_IMAGE_V2_ID` | ECR repository image URI (tagged as `v2`) for Lambda container image acceptance tests. |
| `AWS_THIRD_ACCESS_KEY_ID` | AWS access key ID with access to a third AWS account for tests requiring multiple accounts. Requires `AWS_THIRD_SECRET_ACCESS_KEY`. Conflicts with `AWS_THIRD_PROFILE`. |
| `AWS_THIRD_SECRET_ACCESS_KEY` | AWS secret access key with access to a third AWS account for tests requiring multiple accounts. Requires `AWS_THIRD_ACCESS_KEY_ID`. Conflicts with `AWS_THIRD_PROFILE`. |
| `AWS_THIRD_PROFILE` | AWS profile with access to a third AWS account for tests requiring multiple accounts. Conflicts with `AWS_THIRD_ACCESS_KEY_ID` and `AWS_THIRD_SECRET_ACCESS_KEY`. |
| `AWS_THIRD_REGION` | Third AWS region for tests requiring multiple regions. Defaults to `us-east-2`. |
| `CHATBOT_SLACK_CHANNEL_ID` | ID of the Slack channel. |
| `CHATBOT_SLACK_TEAM_ID` | ID of the Slack workspace authorized with AWS Chatbot. |
| `CHATBOT_TEAMS_CHANNEL_ID` | ID of the Microsoft Teams channel. |
| `CHATBOT_TEAMS_TEAM_ID` | ID of the Microsoft Teams workspace authorized with AWS Chatbot. |
| `CHATBOT_TEAMS_TENANT_ID` | ID of the Microsoft Teams tenant. |
| `DX_CONNECTION_ID` | Identifier for Direct Connect Connection testing. |
| `DX_VIRTUAL_INTERFACE_ID` | Identifier for Direct Connect Virtual Interface testing. |
| `EC2_SECURITY_GROUP_RULES_PER_GROUP_LIMIT` | EC2 Quota for Rules per Security Group. Defaults to 50. **DEPRECATED:** Can be augmented or replaced with Service Quotas lookup. |
| `EVENT_BRIDGE_PARTNER_EVENT_BUS_NAME` | Amazon EventBridge partner event bus name. |
| `EVENT_BRIDGE_PARTNER_EVENT_SOURCE_NAME` | Amazon EventBridge partner event source name. |
| `FINSPACE_MANAGED_KX_LICENSE_ENABLED` | Enables tests requiring a license to provision managed KX resources. |
| `GCM_API_KEY` | API Key for Google Cloud Messaging in Pinpoint and SNS Platform Application testing. |
| `GITHUB_TOKEN` | GitHub token for CodePipeline testing. |
| `GLOBALACCERATOR_BYOIP_IPV4_ADDRESS` | IPv4 address from a BYOIP CIDR of AWS Account used for testing Global Accelerator's BYOIP accelerator. |
| `GRAFANA_SSO_GROUP_ID` | AWS SSO group ID for Grafana testing. |
| `GRAFANA_SSO_USER_ID` | AWS SSO user ID for Grafana testing. |
| `MACIE_MEMBER_ACCOUNT_ID` | Identifier of AWS Account for Macie Member testing. **DEPRECATED:** Should be replaced with standard alternate account handling for tests. |
| `QUICKSIGHT_NAMESPACE` | QuickSight namespace name for testing. |
| `QUICKSIGHT_ATHENA_TESTING_ENABLED` | Enable QuickSight tests dependent on Amazon Athena resources. |
| `ROUTE53DOMAINS_DOMAIN_NAME` | Registered domain for Route 53 Domains testing. |
| `RESOURCEEXPLORER_INDEX_TYPE` | Index Type for Resource Explorer 2 Search datasource testing. |
| `SAGEMAKER_IMAGE_VERSION_BASE_IMAGE` | SageMaker base image to use for tests. |
| `SERVICEQUOTAS_INCREASE_ON_CREATE_QUOTA_CODE` | Quota Code for Service Quotas testing (submits support case). |
| `SERVICEQUOTAS_INCREASE_ON_CREATE_SERVICE_CODE` | Service Code for Service Quotas testing (submits support case). |
| `SERVICEQUOTAS_INCREASE_ON_CREATE_VALUE` | Value of quota increase for Service Quotas testing (submits support case). |
| `SES_DOMAIN_IDENTITY_ROOT_DOMAIN` | Root domain name of publicly accessible and Route 53 configurable domain for SES Domain Identity testing. |
| `SES_DEDICATED_IP` | Dedicated IP address for testing IP assignment with a "Standard" (non-managed) SES dedicated IP pool. |
| `SWF_DOMAIN_TESTING_ENABLED` | Enables SWF Domain testing (API does not support deletions). |
| `TEST_AWS_ORGANIZATION_ACCOUNT_EMAIL_DOMAIN` | Email address for Organizations Account testing. |
| `TEST_AWS_SES_VERIFIED_EMAIL_ARN` | Verified SES Email Identity for use in Cognito User Pool testing. |
| `TF_ACC` | Enables Go tests containing `resource.Test()` and `resource.ParallelTest()`. |
| `TF_ACC_ASSUME_ROLE_ARN` | Amazon Resource Name of existing IAM Role to use for limited permissions acceptance testing. |
| `TF_AWS_LICENSE_MANAGER_GRANT_HOME_REGION` | Region where a License Manager license is imported. |
| `TF_AWS_LICENSE_MANAGER_GRANT_LICENSE_ARN` | ARN for a License Manager license imported into the current account. |
| `TF_AWS_LICENSE_MANAGER_GRANT_PRINCIPAL` | ARN of a principal to share the License Manager license with. Either a root user, Organization, or Organizational Unit. |
| `TF_TEST_CLOUDFRONT_RETAIN` | Flag to disable but dangle CloudFront Distributions during testing to reduce feedback time (must be manually destroyed afterwards) |
| `TF_TEST_ELASTICACHE_RESERVED_CACHE_NODE` | Flag to enable resource tests for ElastiCache reserved nodes. Set to `1` to run tests |
<!-- markdownlint-configure-file { "code-block-style": false } -->
# Adding a New Data Source

New data sources are required when AWS adds a new service, or adds new features within an existing service which would require a new data source to allow practitioners to query existing resources of that type for use in their configurations. Anything with a Describe or Get endpoint could make a data source, but some are more useful than others.

Each data source should be submitted for review in isolation, pull requests containing multiple data sources and/or resources are harder to review and the maintainers will normally ask for them to be broken apart.

## Prerequisites

If this is the first addition of a data source for a new service, please ensure the Service Client for the new service has been added and merged. See [Adding a new Service](add-a-new-service.md) for details.

## Steps to Add a Data Source

### Fork the Provider and Create a Feature Branch

For a new data source use a branch named `f-{datasource name}` for example: `f-ec2-vpc`. See [Raising a Pull Request](raising-a-pull-request.md) for more details.

### Create and Name the Data Source

See the [Naming Guide](naming.md#resources-and-data-sources) for details on how to name the new data source and the data source file. Not following the naming standards will cause extra delay as maintainers request that you make changes.

Use the [skaff](skaff.md) provider scaffolding tool to generate new data source and test templates using your chosen name. Doing so will ensure that any boilerplate code, structural best practices and repetitive naming are done for you and always represent our most current standards.

### Fill out the Data Source Schema

In the `internal/service/<service>/<service>_data_source.go` file you will see a `Schema` property which exists as a map of `Schema` objects. This relates the AWS API data model with the Terraform resource itself. For each property you want to make available in Terraform, you will need to add it as an attribute, and choose the correct data type.

Attribute names are to be specified in `snake_case` as opposed to the AWS API which is `CamelCase`.

### Implement Read Handler

These will map the AWS API response to the data source schema. You will also need to handle different response types (including errors correctly). For complex attributes you will need to implement Flattener or Expander functions. The [Data Handling and Conversion Guide](data-handling-and-conversion.md) covers everything you need to know for mapping AWS API responses to Terraform State and vice-versa. The [Error Handling Guide](error-handling.md) covers everything you need to know about handling AWS API responses consistently.

### Register Data Source to the provider

Data Sources use a self-registration process that adds them to the provider using the `@SDKDataSource()` annotation in the data source's comments. Run `make gen` to register the data source. This will add an entry to the `service_package_gen.go` file located in the service package folder.

=== "Terraform Plugin Framework (Preferred)"

    ```go
    package something

    import (
        "github.com/hashicorp/terraform-plugin-framework/datasource"
        "github.com/hashicorp/terraform-provider-aws/internal/framework"
    )

    // @FrameworkDataSource(name="Example")
    func newResourceExample(_ context.Context) (datasource.ResourceWithConfigure, error) {
    	return &dataSourceExample{}, nil
    }

    type dataSourceExample struct {
	    framework.DataSourceWithConfigure
    }

    func (r *dataSourceExample) Metadata(_ context.Context, request datasource.MetadataRequest, response *datasource.MetadataResponse) {
    	response.TypeName = "aws_something_example"
    }
    ```

=== "Terraform Plugin SDK V2"

    ```go
    package something

    import "github.com/hashicorp/terraform-plugin-sdk/v2/helper/schema"

    // @SDKDataSource("aws_something_example", name="Example")
    func DataSourceExample() *schema.Resource {
    	return &schema.Resource{
    	    // some configuration
    	}
    }
    ```

### Write Passing Acceptance Tests

To adequately test the data source we will need to write a complete set of Acceptance Tests. You will need an AWS account for this which allows the provider to read to state of the associated resource. See [Writing Acceptance Tests](running-and-writing-acceptance-tests.md) for a detailed guide on how to approach these.

You will need at a minimum:

- Basic Test - Tests full lifecycle (CRUD + Import) of a minimal configuration (all required fields, no optional).
- Disappears Test - Tests what Terraform does if a resource it is tracking can no longer be found.
- Per Attribute Tests - For each attribute a test should exist which tests that particular attribute in isolation alongside any required fields.

### Create Documentation for the Data Source

Add a file covering the use of the new data source in `website/docs/d/<service>_<name>.md`. You may want to also add examples of the data source in use particularly if its use is complex, or relies on resources in another service. This documentation will appear on the [Terraform Registry](https://registry.terraform.io/providers/hashicorp/aws/latest) when the data source is made available in a provider release. It is fine to link out to AWS Documentation where appropriate, particularly for values which are likely to change.

### Ensure Format and Lint Checks are Passing Locally

Run `go fmt` to format your code, and install and run all linters to detect and resolve any structural issues with the implementation or documentation.

```sh
make fmt
make tools        # install linters and dependencies
make lint         # run provider linters
make docs-lint    # run documentation linters
make website-lint # run website documentation linters
```

### Raise a Pull Request

See [Raising a Pull Request](raising-a-pull-request.md).

### Wait for Prioritization

In general, pull requests are triaged within a few days of creation and are prioritized based on community reactions. Please view our [prioritization](prioritization.md) guide for full details of the process.
# Adding a New Function

Provider-defined functions were introduced with Terraform 1.8, enabling provider developers to expose functions specific to a given cloud provider or use case.
Functions in the AWS provider provide a utility that is valuable when paired with AWS resources.

See the Terraform Plugin Framework [Function documentation](https://developer.hashicorp.com/terraform/plugin/framework/functions) for additional details.

## Prerequisites

The only prerequisite for creating a function is ensuring the desired functionality is appropriate for a provider-defined function.
Functions must be reproducible across executions ("pure" functions), where the same input always results in the same output.
This requirement precludes the use of network calls, so operations requiring an AWS API call should instead consider utilizing a [data source](add-a-new-datasource.md).
Data manipulation tasks tend to be the most common use cases.

## Steps to add a function

### Fork the provider and create a feature branch

For a new function use a branch named `f-{function name}`, for example, `f-arn_parse`.
See [Raising a Pull Request](raising-a-pull-request.md) for more details.

### Generate function scaffolding

The `skaff function` subcommand can be used to generate an outline for the new function.

First, install `skaff` and navigate to the directory where provider functions are defined (`internal/function`).

```console
make skaff
```

```console
cd internal/function
```

Next, run the `skaff function` subcommand.
The name and description flags are required.
The name argument should be [mixed caps](naming.md#mixed-caps) (ie. `FooBar`), and the generator will handle converting the name to snake case where appropriate.

```console
skaff function -n Example -d "Makes some output from an input."
```

This will generate files storing the function definition, unit tests, and registry documentation.
The following steps describe how to complete the function implementation.

### Fill out the function parameter(s) and return value

The function struct's `Definition` method will document the expected parameters and return value.
Parameter names and return values should be specified in `snake_case`.

```go
func (f exampleFunction) Definition(ctx context.Context, req function.DefinitionRequest, resp *function.DefinitionResponse) {
	resp.Definition = function.Definition{
		Parameters: []function.Parameter{
			function.StringParameter{Name: "some_arg"},
		},
		Return: function.StringReturn{},
	}
}
```

The example above defines a function which accepts a string parameter, `some_arg`, and returns a string value.

### Implement the function logic

The function struct's `Run` method will contain the function logic.
This includes processing the arguments, setting the return value, and any data processing that needs to happen in between.

```go
func (f exampleFunction) Run(ctx context.Context, req function.RunRequest, resp *function.RunResponse) {
	var data string

	resp.Error = function.ConcatFuncErrors(req.Arguments.Get(ctx, &data))
	if resp.Error != nil {
		return
	}

	//
	// Function logic goes here
	//

	resp.Error = function.ConcatFuncErrors(resp.Result.Set(ctx, data))
}
```

### Register function to the provider

Once the function is implemented, it must be registered to the provider to be used.
As only Terraform Plugin Framework supports provider-defined functions, registration occurs on the Plugin Framework provider inside `internal/provider/fwprovider/provider.go`.
Add the `New*` factory function in the `Functions` method to register it.

```go
func (p *fwprovider) Functions(_ context.Context) []func() function.Function {
	return []func() function.Function{
            // Append to list of existing functions here
            tffunction.NewExampleFunction,
	}
}
```

### Write passing acceptance tests

All functions should have corresponding acceptance tests.
For functions with variadic arguments, or which can potentially return an error, tests should be written to exercise those conditions.

An example outline is included below:

```go
// Copyright (c) HashiCorp, Inc.
// SPDX-License-Identifier: MPL-2.0

package function_test

import (
	"fmt"
	"testing"

	"github.com/hashicorp/go-version"
	"github.com/hashicorp/terraform-plugin-testing/helper/resource"
	"github.com/hashicorp/terraform-plugin-testing/tfversion"
	"github.com/hashicorp/terraform-provider-aws/internal/acctest"
)

func TestExampleFunction_basic(t *testing.T) {
	t.Parallel()

	resource.UnitTest(t, resource.TestCase{
		ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
		TerraformVersionChecks: []tfversion.TerraformVersionCheck{
			tfversion.SkipBelow(version.Must(version.NewVersion("1.8.0"))),
		},
		Steps: []resource.TestStep{
			{
				Config: testExampleFunctionConfig("foo"),
				Check: resource.ComposeAggregateTestCheckFunc(
					resource.TestCheckOutput("test", "foo"),
				),
			},
		},
	})
}

func testExampleFunctionConfig(arg string) string {
	return fmt.Sprintf(`
output "test" {
  value = provider::aws::example(%[1]q)
}`, arg)
}
```

With Terraform 1.8+ installed, individual tests can be run like:

```console
go test -run='^TestExampleFunction' -v ./internal/function/
```

### Create documentation for the resource

`skaff` will have generated framed out registry documentation in `website/docs/functions/<function name>.html.markdown`.
The `Example Usage`, `Signature`, and `Arguments` sections should all be updated with the appropriate content.
Once released, this documentation will appear on the [Terraform Registry](https://registry.terraform.io/providers/hashicorp/aws/latest).

### Raise a pull request

See [Raising a Pull Request](raising-a-pull-request.md).

### Wait for prioritization

In general, pull requests are triaged within a few days of creation and are prioritized based on community reactions.
Please view our [Prioritization Guide](prioritization.md) for full details of the process.
# Adding a Newly Released AWS Region

New regions can typically be used immediately with the provider, with two important caveats:

- Regions often need to be explicitly enabled via the AWS console. See [ap-east-1 launch blog](https://aws.amazon.com/blogs/aws/now-open-aws-asia-pacific-hong-kong-region/) for an example of how to enable a new region for use.
- Until the provider is aware of the new region, automatic region validation will fail. To use the region before validation support is added to the provider you will need to disable region validation by doing the following:

```terraform
provider "aws" {
  # ... potentially other configuration ...

  region                 = "me-south-1"
  skip_region_validation = true
}
```

## Enabling Region Validation

Support for region validation requires that the provider has an updated [AWS SDK Go Base](aws-sdk-go-base.md) dependency that includes the new region. This also needs to be done in the core Terraform binary itself to enable it for the S3 backend. Many of the authentication and provider-level configuration interactions are also located in the `aws-go-sdk-base` library. As all of these things take direct dependencies and as a result there end up being quite a few places where these dependency updates need to be made.

### Update aws-go-sdk-base

[aws-go-sdk-base](https://github.com/hashicorp/aws-sdk-go-base)

- Update [aws-go-sdk-v2](https://github.com/aws/aws-sdk-go-v2)

### Update Terraform AWS Provider

[provider](https://github.com/hashicorp/terraform-provider-aws)

- Update [aws-go-sdk-v2](https://github.com/aws/aws-sdk-go-v2)
- Update [aws-go-sdk-base](https://github.com/hashicorp/aws-sdk-go-base)

### Update Terraform Core (S3 Backend)

[core](https://github.com/hashicorp/terraform)

- Update [aws-go-sdk-v2](https://github.com/aws/aws-sdk-go-v2)
- Update [aws-go-sdk-base](https://github.com/hashicorp/aws-sdk-go-base)

See the [Changelog Process](changelog-process.md) document for example changelog format.

## Update Region Specific values in static Data Sources

Some data sources include static values specific to regions that are not available via a standard AWS API call. These will need to be manually updated. AWS employees can code search previous region values to find new region values in internal packages like RIPStaticConfig if they are not documented yet.

- Check [Elastic Load Balancing endpoints and quotas](https://docs.aws.amazon.com/general/latest/gr/elb.html#elb_region) and add Route53 Hosted Zone ID if available to [`internal/service/elb/hosted_zone_id_data_source.go`](https://github.com/hashicorp/terraform-provider-aws/tree/main/internal/service/elb/hosted_zone_id_data_source.go) and [`internal/service/elbv2/hosted_zone_id_data_source.go`](https://github.com/hashicorp/terraform-provider-aws/tree/main/internal/service/elbv2/hosted_zone_id_data_source.go)
- Check [Amazon Simple Storage Service endpoints and quotas](https://docs.aws.amazon.com/general/latest/gr/s3.html#s3_website_region_endpoints) and add Route53 Hosted Zone ID if available to [`internal/service/s3/hosted_zones.go`](https://github.com/hashicorp/terraform-provider-aws/tree/main/internal/service/s3/hosted_zones.go)
- Check [AWS Elastic Beanstalk endpoints and quotas](https://docs.aws.amazon.com/general/latest/gr/elasticbeanstalk.html) and add Route53 Hosted Zone ID if available to [`internal/service/elasticbeanstalk/hosted_zone_data_source.go`](https://github.com/hashicorp/terraform-provider-aws/tree/main/internal/service/elasticbeanstalk/hosted_zone_data_source.go)
- Check [SageMaker docs](https://docs.aws.amazon.com/sagemaker/latest/dg/sagemaker-algo-docker-registry-paths.html) and add AWS Account IDs if available to [`internal/service/sagemaker/prebuilt_ecr_image_data_source.go`](https://github.com/hashicorp/terraform-provider-aws/tree/main/internal/service/sagemaker/prebuilt_ecr_image_data_source.go)
- Check [App Runner docs](https://docs.aws.amazon.com/general/latest/gr/apprunner.html#apprunner_region) and add Route53 Hosted Zone ID if available to [`internal/service/apprunner/hosted_zone_id_data_source.go`](https://github.com/hashicorp/terraform-provider-aws/tree/main/internal/service/apprunner/hosted_zone_id_data_source.go)
<!-- markdownlint-configure-file { "code-block-style": false } -->
# Adding a New Resource

New resources are required when AWS adds a new service, or adds new features within an existing service which would require a new resource to manage in Terraform. Typically anything with a new set of CRUD API endpoints is a great candidate for a new resource.

Each resource should be submitted for review in isolation. Pull requests containing multiple resources are harder to review and the maintainers will normally ask for them to be broken apart.

## Prerequisites

If this is the first resource for a new service, please ensure the Service Client for the new service has been added and merged. See [Adding a new Service](add-a-new-service.md) for details.

## Steps to Add a Resource

### Fork the provider and create a feature branch

For new resources use a branch named `f-{resource name}` for example: `f-ec2-vpc`. See [Raising a Pull Request](raising-a-pull-request.md) for more details.

### Create and Name the Resource

See the [Naming Guide](naming.md#resources-and-data-sources) for details on how to name the new resource and the resource file. Not following the naming standards will cause extra delay as maintainers request that you make changes.

Use the [skaff](skaff.md) provider scaffolding tool to generate new resource and test templates using your chosen name. Doing so will ensure that any boilerplate code, structural best practices and repetitive naming are done for you and always represent our most current standards.

### Fill out the Resource Schema

In the `internal/service/<service>/<service>.go` file you will see a `Schema` property which exists as a map of `Schema` objects. This relates the AWS API data model with the Terraform resource itself. For each property you want to make available in Terraform, you will need to add it as an attribute, choose the correct data type and supply the correct [Schema Behaviors](https://www.terraform.io/plugin/sdkv2/schemas/schema-behaviors) to ensure Terraform knows how to correctly handle the value.

Typically you will add arguments to represent the values that are under control by Terraform, and attributes to supply read-only values as references for Terraform. These are distinguished by Schema Behavior.

Attribute names are to be specified in `snake_case` as opposed to the AWS API which is `CamelCase`.

### Implement CRUD handlers

These will map the planned Terraform state to the AWS API call, or an AWS API response to an applied Terraform state. You will also need to handle different response types (including errors correctly). For complex attributes, you will need to implement Flattener or Expander functions. The [Data Handling and Conversion Guide](data-handling-and-conversion.md) covers everything you need to know for mapping AWS API responses to Terraform State and vice-versa. The [Error Handling Guide](error-handling.md) covers everything you need to know about handling AWS API responses consistently.

### Register Resource to the provider

Resources use a self-registration process that adds them to the provider using the `@FrameworkResource()` or `@SDKResource()` annotation in the resource's comments. Run `make gen` to register the resource. This will add an entry to the `service_package_gen.go` file located in the service package folder.

=== "Terraform Plugin Framework (Preferred)"

    ```go
    package something

    import (
        "github.com/hashicorp/terraform-plugin-framework/resource"
        "github.com/hashicorp/terraform-provider-aws/internal/framework"
    )

    // @FrameworkResource("aws_something_example", name="Example")
    func newResourceExample(_ context.Context) (resource.ResourceWithConfigure, error) {
    	return &resourceExample{}, nil
    }

    type resourceExample struct {
    	framework.ResourceWithConfigure
    }

    func (r *resourceExample) Metadata(_ context.Context, request resource.MetadataRequest, response *resource.MetadataResponse) {
    	response.TypeName = "aws_something_example"
    }
    ```

=== "Terraform Plugin SDK V2"

    ```go
    package something

    import "github.com/hashicorp/terraform-plugin-sdk/v2/helper/schema"

    // @SDKResource("aws_something_example", name="Example)
    func ResourceExample() *schema.Resource {
    	return &schema.Resource{
    	    // some configuration
    	}
    }
    ```

### Write passing Acceptance Tests

To adequately test the resource we will need to write a complete set of Acceptance Tests. You will need an AWS account for this which allows the creation of that resource. See [Writing Acceptance Tests](running-and-writing-acceptance-tests.md) for a detailed guide on how to approach these.

You will need at a minimum:

- Basic Test - Tests full lifecycle (CRUD + Import) of a minimal configuration (all required fields, no optional).
- Disappears Test - Tests what Terraform does if a resource it is tracking can no longer be found.
- Argument Tests - All arguments should be tested in a pragmatic way. Ensure that each argument can be initially set, updated, and cleared, as applicable. Depending on the logic and interaction of arguments, this may take one to several separate tests.

### Create documentation for the resource

Add a file covering the use of the new resource in `website/docs/r/<service>_<name>.md`. Add more examples if it is complex or relies on resources in another service. This documentation will appear on the [Terraform Registry](https://registry.terraform.io/providers/hashicorp/aws/latest) when the resource is made available in a provider release. Link to AWS Documentation where appropriate, particularly for values which are likely to change.

### Ensure format and lint checks are passing locally

Format your code and check linters to detect various issues.

```sh
make fmt
make tools     # install linters and dependencies
make lint      # run provider linters
make docs-lint # run documentation linters
```

### Raise a Pull Request

See [Raising a Pull Request](raising-a-pull-request.md).

### Wait for Prioritization

In general, pull requests are triaged within a few days of creation and are prioritized based on community reactions. Please view our [Prioritization Guide](prioritization.md) for full details of the process.
<!-- markdownlint-configure-file { "code-block-style": false } -->
# Adding a New AWS Service

AWS frequently launches new services, and Terraform support is frequently desired by the community shortly after launch. Depending on the API surface area of the new service, this could be a major undertaking. The following steps should be followed to prepare for adding the resources that allow for Terraform management of that service.

## Perform Service Design

Before adding a new service to the provider it's a good idea to familiarize yourself with the primary workflows practitioners are likely to want to accomplish with the provider to ensure the provider design can solve this. It's not always necessary to cover 100% of the AWS service offering to unblock most workflows.

You should have an idea of what resources and data sources should be added, their dependencies and relative importance concerning the workflow. This should give you an idea of the order in which resources are to be added. It's important to note that generally, we like to review and merge resources in isolation, and avoid combining multiple new resources in one Pull Request.

Using the AWS API documentation as a reference, identify the various APIs that correspond to the CRUD operations which consist of the management surface for that resource. These will be the set of APIs called from the new resource. The API's model attributes will correspond to your resource schema.

From there begin to map out the list of resources you would like to implement, and note your plan on the GitHub issue relating to the service (or create one if one does not exist) for the community and maintainers to feedback.

## Add a Service Client

Before new resources are submitted, please raise a separate pull request containing just the new AWS SDK for Go service client.

To add an AWS SDK for Go service client:

1. Check the file `names/data/names_data.hcl` for the service.

1. If the service is there and the `not_implemented` attribute does not exist, you are ready to implement the first [resource](./add-a-new-resource.md) or [data source](./add-a-new-datasource.md).

1. If the service is there and the `not_implemented` attribute is true, remove it and submit the client pull request as described below.

1. Otherwise, determine the service identifier using the rule described in [the Naming Guide](naming.md#service-identifier).

1. In `names/data/names_data.hcl`, add a new hcl block with all the requested information for the service following the guidance in the [`names` README](https://github.com/hashicorp/terraform-provider-aws/blob/main/names/README.md).

    !!! tip
        Be very careful when adding or changing data in `names_data.hcl`!
        The Provider and generators depend on the file being correct.
        We strongly recommend using an editor with HCL support.

Once the names data is ready, create a new service directory with the appropriate service name.

```console
mkdir internal/service/<service>
```

Add a new file `internal/service/<service>/generate.go` with the following content. This will generate the structs required for [resource self-registration](./add-a-new-resource.md#register-resource-to-the-provider).

```go
// Copyright (c) HashiCorp, Inc.
// SPDX-License-Identifier: MPL-2.0

//go:generate go run ../../generate/servicepackage/main.go
// ONLY generate directives and package declaration! Do not add anything else to this file.

package <service>
```

Next, generate the client and ensure all dependencies are fetched.

```console
make gen
```

```console
go mod tidy
```

At this point a pull request with the re-generated files and new service client can be submitted.

Once the service client has been added, implement the first [resource](./add-a-new-resource.md) or [data source](./add-a-new-datasource.md) in a separate PR.

## Adding a Custom Service Client

If an AWS service must be created in a non-standard way, for example, the service API's endpoint must be accessed via a single AWS Region, then:

1. Make the `skip_client_generate` attribute `true` for the service in [`names/data/names_data.hcl`](https://github.com/hashicorp/terraform-provider-aws/blob/main/names/README.md)

1. Run `make gen`

1. Add a file `internal/<service>/service_package.go` that contains an API client factory function, for example:

    ```go
    package costoptimizationhub

    import (
        "context"

        "github.com/aws/aws-sdk-go-v2/aws"
        "github.com/aws/aws-sdk-go-v2/service/costoptimizationhub"
        "github.com/hashicorp/terraform-provider-aws/names"
    )

    // NewClient returns a new AWS SDK for Go v2 client for this service package's AWS API.
    func (p *servicePackage) NewClient(ctx context.Context, config map[string]any) (*costoptimizationhub.Client, error) {
        cfg := *(config["aws_sdkv2_config"].(*aws.Config))

        return costoptimizationhub.NewFromConfig(cfg,
            costoptimizationhub.WithEndpointResolverV2(newEndpointResolverSDKv2()),
            withBaseEndpoint(config[names.AttrEndpoint].(string)),
            func(o *costoptimizationhub.Options) {
                if config["partition"].(string) == names.StandardPartitionID {
                    // Cost Optimization Hub endpoint is available only in us-east-1 Region.
                    if cfg.Region != names.USEast1RegionID {
                        tflog.Info(ctx, "overriding region", map[string]any{
                            "original_region": cfg.Region,
                            "override_region": names.USEast1RegionID,
                        })
                        o.Region = names.USEast1RegionID
                    }
                }
            },
        ), nil
    }
    ```

## Customizing a new Service Client

If an AWS service must be customized after creation, for example, retry handling must be changed, then:

1. Add a file `internal/<service>/service_package.go` that contains an API client customization function, for example:

```go
package shield

import (
	"context"

	"github.com/aws/aws-sdk-go-v2/aws"
	"github.com/aws/aws-sdk-go-v2/service/shield"
	"github.com/hashicorp/aws-sdk-go-base/v2/endpoints"
	"github.com/hashicorp/terraform-plugin-log/tflog"
	"github.com/hashicorp/terraform-provider-aws/names"
)

// NewClient returns a new AWS SDK for Go v2 client for this service package's AWS API.
func (p *servicePackage) NewClient(ctx context.Context, config map[string]any) (*shield.Client, error) {
	cfg := *(config["aws_sdkv2_config"].(*aws.Config))

	return shield.NewFromConfig(cfg,
		shield.WithEndpointResolverV2(newEndpointResolverV2()),
		withBaseEndpoint(config[names.AttrEndpoint].(string)),
		func(o *shield.Options) {
			// Force "global" services to correct Regions.
			if config["partition"].(string) == endpoints.AwsPartitionID {
				if cfg.Region != names.USEast1RegionID {
					tflog.Info(ctx, "overriding region", map[string]any{
						"original_region": cfg.Region,
						"override_region": names.USEast1RegionID,
					})
					o.Region = names.USEast1RegionID
				}
			}
		},
	), nil
}
```
# Adding Resource Import Support

Adding import support for Terraform resources will allow existing infrastructure to be managed within Terraform. This type of enhancement generally requires a small to moderate amount of code changes. Comprehensive code examples and information about resource import support can be found in the [Terraform Plugin Framework documentation](https://developer.hashicorp.com/terraform/plugin/framework/resources/import).

- _Resource Code_: In the resource code (e.g., `internal/service/{service}/{thing}.go`),
    - **Plugin Framework (Preferred)** Implement the `ImportState` method on the resource struct. When possible, prefer using the [`resource.ImportStatePassthroughID` function](https://pkg.go.dev/github.com/hashicorp/terraform-plugin-framework/resource#ImportStatePassthroughID).
    - **Plugin SDK V2**: Implement an `Importer` `State` function. When possible, prefer using [`schema.ImportStatePassthroughContext`](https://www.terraform.io/plugin/sdkv2/resources/import#importer-state-function).
- _Resource Acceptance Tests_: In the resource acceptance tests (e.g., `internal/service/{service}/{thing}_test.go`), implement one or more tests containing a `TestStep` with `ImportState: true`.
- _Resource Documentation_: In the resource documentation (e.g., `website/docs/r/service_thing.html.markdown`), add an `Import` section at the bottom of the page.
# Adding a New Tag Resource

Adding a tag resource, similar to the `aws_ecs_tag` resource, has its own implementation procedure since the resource code and initial acceptance testing functions are automatically generated. The rest of the resource acceptance testing and resource documentation must still be manually created.

- In `internal/generate`: Ensure the service is supported by all generators. Run `make gen` after any modifications.
- In `internal/service/{service}/generate.go`: Add the new `//go:generate` call with the correct generator directives. Run `make gen` after any modifications.
- In `internal/provider/provider.go`: Add the new resource.
- Run `make test` and ensure there are no failures.
- Create `internal/service/{service}/tag_gen_test.go` with initial acceptance testing similar to the following (where the parent resource is simple to provision):

```go
import (
	"fmt"
	"testing"

	"github.com/hashicorp/terraform-plugin-testing/helper/acctest"
	"github.com/hashicorp/terraform-plugin-testing/helper/resource"
	"github.com/hashicorp/terraform-provider-aws/names"
)

func TestAcc{Service}Tag_basic(t *testing.T) {
	ctx := acctest.Context(t)
	rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)
	resourceName := "aws_{service}_tag.test"

	resource.ParallelTest(t, resource.TestCase{
		PreCheck:                 func() { acctest.PreCheck(ctx, t) },
		ErrorCheck:               acctest.ErrorCheck(t, names.{Service}ServiceID),
		ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
		CheckDestroy:             testAccCheck{Service}TagDestroy(ctx),
		Steps: []resource.TestStep{
			{
				Config: testAcc{Service}TagConfig(rName, "key1", "value1"),
				Check: resource.ComposeTestCheckFunc(
					testAccCheck{Service}TagExists(ctx, resourceName),
					resource.TestCheckResourceAttr(resourceName, "key", "key1"),
					resource.TestCheckResourceAttr(resourceName, "value", "value1"),
				),
			},
			{
				ResourceName:      resourceName,
				ImportState:       true,
				ImportStateVerify: true,
			},
		},
	})
}

func TestAcc{Service}Tag_disappears(t *testing.T) {
	ctx := acctest.Context(t)
	rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)
	resourceName := "aws_{service}_tag.test"

	resource.ParallelTest(t, resource.TestCase{
		PreCheck:                 func() { acctest.PreCheck(ctx, t) },
		ErrorCheck:               acctest.ErrorCheck(t, names.{Service}ServiceID),
		ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
		CheckDestroy:             testAccCheck{Service}TagDestroy(ctx),
		Steps: []resource.TestStep{
			{
				Config: testAcc{Service}TagConfig(rName, "key1", "value1"),
				Check: resource.ComposeTestCheckFunc(
					testAccCheck{Service}TagExists(ctx, resourceName),
					acctest.CheckResourceDisappears(ctx, acctest.Provider, resourceAws{Service}Tag(), resourceName),
				),
				ExpectNonEmptyPlan: true,
			},
		},
	})
}

func TestAcc{Service}Tag_Value(t *testing.T) {
	ctx := acctest.Context(t)
	rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)
	resourceName := "aws_{service}_tag.test"

	resource.ParallelTest(t, resource.TestCase{
		PreCheck:                 func() { acctest.PreCheck(ctx, t) },
		ErrorCheck:               acctest.ErrorCheck(t, names.{Service}ServiceID),
		ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
		CheckDestroy:             testAccCheck{Service}TagDestroy(ctx),
		Steps: []resource.TestStep{
			{
				Config: testAcc{Service}TagConfig(rName, "key1", "value1"),
				Check: resource.ComposeTestCheckFunc(
					testAccCheck{Service}TagExists(ctx, resourceName),
					resource.TestCheckResourceAttr(resourceName, "key", "key1"),
					resource.TestCheckResourceAttr(resourceName, "value", "value1"),
				),
			},
			{
				ResourceName:      resourceName,
				ImportState:       true,
				ImportStateVerify: true,
			},
			{
				Config: testAcc{Service}TagConfig(rName, "key1", "value1updated"),
				Check: resource.ComposeTestCheckFunc(
					testAccCheck{Service}TagExists(ctx, resourceName),
					resource.TestCheckResourceAttr(resourceName, "key", "key1"),
					resource.TestCheckResourceAttr(resourceName, "value", "value1updated"),
				),
			},
		},
	})
}

func testAcc{Service}TagConfig(rName string, key string, value string) string {
	return fmt.Sprintf(`
resource "aws_{service}_{thing}" "test" {
  name = %[1]q

  lifecycle {
    ignore_changes = [tags]
  }
}

resource "aws_{service}_tag" "test" {
  resource_arn = aws_{service}_{thing}.test.arn
  key          = %[2]q
  value        = %[3]q
}
`, rName, key, value)
}
```

- Run `make testacc TESTS=TestAcc{Service}Tags_ PKG={Service}` and ensure there are no failures.
- Create `website/docs/r/{service}_tag.html.markdown` with initial documentation similar to the following:

``````markdown
---
subcategory: "{SERVICE}"
layout: "aws"
page_title: "AWS: aws_{service}_tag"
description: |-
  Manages an individual {SERVICE} resource tag
---

# Resource: aws_{service}_tag

Manages an individual {SERVICE} resource tag. This resource should only be used in cases where {SERVICE} resources are created outside Terraform (e.g., {SERVICE} {THING}s implicitly created by {OTHER SERVICE THING}).

~> **NOTE:** This tagging resource should not be combined with the Terraform resource for managing the parent resource. For example, using `aws_{service}_{thing}` and `aws_{service}_tag` to manage tags of the same {SERVICE} {THING} will cause a perpetual difference where the `aws_{service}_{thing}` resource will try to remove the tag being added by the `aws_{service}_tag` resource.

~> **NOTE:** This tagging resource does not use the [provider `ignore_tags` configuration](/docs/providers/aws/index.html#ignore_tags).

## Example Usage

```terraform
resource "aws_{service}_tag" "example" {
  resource_arn = "..."
  key          = "Name"
  value        = "Hello World"
}
```

## Argument Reference

This resource supports the following arguments:

* `resource_arn` - (Required) ARN of the {SERVICE} resource to tag.
* `key` - (Required) Tag name.
* `value` - (Required) Tag value.

## Attribute Reference

This resource exports the following attributes in addition to the arguments above:

* `id` - {SERVICE} resource identifier and key, separated by a comma (`,`)

## Import

Import `aws_{service}_tag` using the {SERVICE} resource identifier and key, separated by a comma (`,`). For example:

```console
$ terraform import aws_{service}_tag.example arn:aws:{service}:us-east-1:123456789012:{thing}/example,Name
```
``````
# AWS SDK Go Base

[AWS SDK Go Base](https://github.com/hashicorp/aws-sdk-go-base) is a shared library used by the [AWS Provider](https://github.com/hashicorp/terraform-provider-aws), [AWSCC Provider](https://github.com/hashicorp/terraform-provider-awscc) and the [Terraform S3 Backend](https://github.com/hashicorp/terraform/tree/main/internal/backend/remote-state/s3) to handle authentication and other non-service level AWS interactions consistently.

Changes are infrequent and normally performed by HashiCorp maintainers.
It should not be necessary to change this library for the majority of provider contributions.
# Making Small Changes to Existing Resources

Most contributions to the provider will take the form of small additions or bug-fixes on existing resources/data sources. In this case the existing resource will give you the best guidance on how the change should be structured, but we require the following to allow the change to be merged:

- __Acceptance test coverage of new behavior__: Existing resources each
   have a set of [acceptance tests](running-and-writing-acceptance-tests.md) covering their functionality.
   These tests should exercise all the behavior of the resource. Whether you are
   adding something or fixing a bug, the idea is to have an acceptance test that
   fails if your code were to be removed. Sometimes it is sufficient to
   "enhance" an existing test by adding an assertion or tweaking the config
   that is used, but it's often better to add a new test. You can copy/paste an
   existing test and follow the conventions you see there, modifying the test
   to exercise the behavior of your code.
- __Documentation updates__: If your code makes any changes that need to
   be documented, you should include those [documentation changes](documentation-changes.md)
   in the same PR. This includes things like new resource attributes or changes in default values.
- __Well-formed Code__: Do your best to follow existing conventions you
   see in the codebase, and ensure your code is formatted with `go fmt`.
   The PR reviewers can help out on this front, and may provide comments with
   suggestions on how to improve the code.
- __Dependency updates__: Create a separate PR if you are updating dependencies.
   This is to avoid conflicts as version updates tend to be fast-
   moving targets. We will plan to merge the PR with this change first.
- __Changelog entry__: Assuming the code change affects Terraform operators,
   the relevant PR ought to include a user-facing [changelog entry](changelog-process.md)
   describing the new behavior.
# Changelog Process

HashiCorp’s open-source projects have always maintained user-friendly, readable `CHANGELOG.md` that allows users to tell at a glance whether a release should have any effect on them, and to gauge the risk of an upgrade.

We use [go-changelog](https://github.com/hashicorp/go-changelog) to generate the changelog from files created in the `.changelog/` directory.
It is important that when you raise your pull request, there is a changelog entry which describes the changes your contribution makes.
Not all changes require an entry in the changelog, guidance follows on what changes do.

## Changelog format

The changelog format requires an entry in the following format, where HEADER corresponds to the changelog category, and the entry is the changelog entry itself. The entry should be included in a file in the `.changelog` directory with the naming convention `{PR-NUMBER}.txt`. For example, to create a changelog entry for pull request 1234, there should be a file named `.changelog/1234.txt`.

``````
```release-note:{HEADER}
{ENTRY}
```
``````

If a pull request should contain multiple changelog entries, then multiple blocks can be added to the same changelog file. For example:

``````
```release-note:note
resource/aws_example_thing: The `broken` attribute has been deprecated. All configurations using `broken` should be updated to use the new `not_broken` attribute instead.
```

```release-note:enhancement
resource/aws_example_thing: Add `not_broken` attribute
```
``````

## Pull request types to CHANGELOG

The CHANGELOG is intended to show operator-impacting changes to the codebase for a particular version. If every change or commit to the code resulted in an entry, the CHANGELOG would become less useful for operators. The lists below are general guidelines and examples for when a decision needs to be made to decide whether a change should have an entry.

### Changes that should have a CHANGELOG entry

#### New resource

A new resource entry should only contain the name of the resource, and use the `release-note:new-resource` header.

``````
```release-note:new-resource
aws_secretsmanager_secret_policy
```
``````

#### New data source

A new data source entry should only contain the name of the data source, and use the `release-note:new-data-source` header.

``````
```release-note:new-data-source
aws_workspaces_workspace
```
``````

#### New full-length documentation guides (e.g., EKS Getting Started Guide, IAM Policy Documents with Terraform)

A new full-length documentation entry gives the title of the documentation added, using the `release-note:new-guide` header.

``````
```release-note:new-guide
Custom Service Endpoint Configuration
```
``````

#### Resource and provider bug fixes

A new bug entry should use the `release-note:bug` header and have a prefix indicating the resource or data source it corresponds to, a colon, then followed by a brief summary. Use a `provider` prefix for provider-level fixes.

``````
```release-note:bug
resource/aws_glue_classifier: Fix quote_symbol being optional
```
``````

#### Resource and provider enhancements

A new enhancement entry should use the `release-note:enhancement` header and have a prefix indicating the resource or data source it corresponds to, a colon, then followed by a brief summary. Use a `provider` prefix for provider-level enhancements.

``````
```release-note:enhancement
resource/aws_eip: Add network_border_group argument
```
``````

#### Deprecations

A deprecation entry should use the `release-note:note` header and have a prefix indicating the resource or data source it corresponds to, a colon, then followed by a brief summary. Use a `provider` prefix for provider-level changes.

``````
```release-note:note
resource/aws_dx_gateway_association: The vpn_gateway_id attribute is being deprecated in favor of the new associated_gateway_id attribute to support transit gateway associations
```
``````

#### Breaking changes and removals

A breaking-change entry should use the `release-note:breaking-change` header and have a prefix indicating the resource or data source it corresponds to, a colon, then followed by a brief summary. Use a `provider` prefix for provider-level changes.

``````
```release-note:breaking-change
resource/aws_lambda_alias: Resource import no longer converts Lambda Function name to ARN
```
``````

#### Region validation support

``````
```release-note:note
provider: Region validation now automatically supports the new `XX-XXXXX-#` (Location) region. For AWS operations to work in the new region, the region must be explicitly enabled as outlined in the [AWS Documentation](https://docs.aws.amazon.com/general/latest/gr/rande-manage.html#rande-manage-enable). When the region is not enabled, the Terraform AWS Provider will return errors during credential validation (e.g., `error validating provider credentials: error calling sts:GetCallerIdentity: InvalidClientTokenId: The security token included in the request is invalid`) or AWS operations will throw their own errors (e.g., `data.aws_availability_zones.available: Error fetching Availability Zones: AuthFailure: AWS was not able to validate the provided access credentials`). [GH-####]
```

```release-note:enhancement
provider: Support automatic region validation for `XX-XXXXX-#` [GH-####]
```
``````

### Changes that may have a CHANGELOG entry

Dependency updates: If the update contains relevant bug fixes or enhancements that affect operators, those should be called out.
Any changes which do not fit into the above categories but warrant highlighting.
Use resource/data source/provider prefixes where appropriate.

``````
```release-note:note
resource/aws_lambda_alias: Resource import no longer converts Lambda Function name to ARN
```
``````

### Changes that should _not_ have a CHANGELOG entry

- Resource and provider documentation updates
- Testing updates
- Code refactoring
# Acceptance Testing Environment Variable Dictionary

Environment variables (beyond standard AWS Go SDK ones) used by acceptance testing. See also the `internal/acctest` package.

| Variable | Description |
|----------|-------------|
| `ACM_CERTIFICATE_RO# Continuous Integration

Continuous integration (CI) includes processes that run when you submit a pull request (PR). These processes can be divided into two broad categories: enrichment and testing.

## CI: Enrichment

The focus of this guide is on CI _testing_, but for completeness, we also mention enrichment processes. These include generating the [changelog](changelog-process.md) when a PR is merged, releasing new versions, labeling a PR based on its size and the AWS service it relates to, and adding automated comments to the PR.

These processes will not usually produce the dreaded red X signifying that a PR has failed CI. For this reason, we shift our focus to CI testing.

## CI: Testing Overview

To help place testing performed as part of CI in context, here is an overview of the Terraform AWS Provider's three types of tests.

1. [**Acceptance tests**](running-and-writing-acceptance-tests.md) are end-to-end evaluations of interactions with AWS. They validate functionalities like creating, reading, and destroying resources within AWS.
2. [**Unit tests**](unit-tests.md) focus on testing isolated units of code within the software, typically at the function level. They assess functionalities solely within the provider itself.
3. **Continuous integration tests** (_You are here!_) encompass a suite of automated tests that are executed on every pull request and include linting, compiling code, running unit tests, and performing static analysis.

## Rationale

Continuous integration (CI) plays a pivotal role in maintaining the health and quality of a large project like the Terraform AWS Provider. CI tests are crucial for automatically assessing code changes for compliance with project standards and functionality expectations, greatly reducing the review burden on maintainers. By executing a battery of tests upon each pull request submission, CI ensures that new contributions integrate seamlessly with the existing codebase, minimizing the risk of regressions and enhancing overall stability.

Additionally, these tests provide rapid feedback to contributors, enabling them to identify and rectify issues early in the development cycle. In essence, CI tests serve as a safeguard, bolstering the reliability and maintainability of the project while fostering a collaborative and iterative development environment.

## Using `make` to Run Specific Tests Locally

**NOTE:** We've made a great effort to ensure that tests running on GitHub have a close-as-possible equivalent in the Makefile. If you notice a difference, please [open an issue](https://github.com/hashicorp/terraform-provider-aws/issues/new/choose) to let us know.

The Makefile included with the Terraform AWS Provider allows you to run many of the CI tests locally before submitting your PR. The file is located in the provider's root directory and is called `GNUmakefile`. You should be able to use `make` with a variety of Linux-type shells that support `bash`, such as a macOS terminal.

**NOTE:** See the [Makefile Cheat Sheet](makefile-cheat-sheet.md) for detailed information about the Makefile.

There are many different tests, and they change often. This guide doesn't cover everything CI does because, as noted above, many of the CI processes enrich the pull request, such as adding labels. If you notice something important that isn't reflected in this documentation, let us know!

**NOTE:** Many tests simply exit without error if passing. "No news is good news."

### Before Running Tests

CI tests run on GitHub when you submit a pull request. However, these tests can take a while to complete. If you prefer, you can run most tests locally. Before running tests locally, you need to clone the repository, which you've likely already done if you're working on a PR, and install the necessary tools.

Use the `tools` target to install a variety of tools used by different CI tests:

```console
make tools
```

### Running All Available CI Tests

Use the `ci` target to run all the tests listed below:

```console
make ci
```

**NOTE:** Depending on your machine, running all the tests can take a long time!

To run most of the tests but exclude the longer-running ones, use the `ci-quick` target. "Quick" may not be _quick_ precisely, but relative to the full `ci` target, it is _quicker_:

```console
make ci-quick
```

Use the `clean-make-tests` target to clean up artifacts left behind by `make` tests, although they should be ignored by Git:

```console
make clean-make-tests
```

### Acceptance Test Linting

Acceptance test linting involves thoroughly testing the Terraform configuration associated with acceptance tests. Currently, this process extracts configuration embedded as strings in Go files. However, as we move testing configurations to `.tf` files, linting will involve testing those files for correctness.

Acceptance test linting has two components: `terrafmt` and `tflint`. The `make` tool provides several targets to help with this.

#### Running All Acceptance Test Linting Checks

Use the `acctest-lint` target to run all the acceptance test linting checks using both `terrafmt` and `tflint`:

```console
make acctest-lint
```

#### Limiting Linting to a Specific Service Package

You can limit the test to a service package by using the `PKG` environment variable:

```console
PKG=rds make acctest-lint
```

The command above is equivalent to using `SVC_DIR` with the full relative path:

```console
SVC_DIR=./internal/service/rds make acctest-lint
```

#### `terrafmt`

Use the `testacc-lint` target to run only the `terrafmt` test. This is useful if you want to skip `tflint`, which takes a long time to run:

```console
make testacc-lint
```

Use the `testacc-lint-fix` target to automatically fix issues found by `terrafmt`:

```console
make testacc-lint-fix
```

#### Validate Acceptance Tests with `tflint`

Use the `testacc-tflint` target to run only the `tflint` test. This is useful if you want to skip `terrafmt`:

```console
make testacc-tflint
```

To run `tflint` only against acceptance test configurations in `.tf` files, use the `testacc-tflint-dir` target:

```console
make testacc-tflint-dir
```

To run `tflint` only against embedded configurations, use the `testacc-tflint-embedded` target:

```console
make testacc-tflint-embedded
```

### Copyright Checks / add headers check

This CI check simply checks to make sure after running the tool, no files have been modified. No modifications signifies that everything already has the proper header.

Use the `copyright` target to add the appropriate copyright headers to all files:

```console
make copyright
```

**NOTE:** Install [tools](#before-running-tests) before running this check.

### Dependency Checks / go_mod

Dependency checks include a variety of tests including who should edit certain types of files. The test that generally trips people up is `go_mod`.

Use the `deps-check` target to make sure that the Go mods files are tidy. This will also install the version of Go defined in the `.go-version` file in the root of the repository.

```console
make deps-check
```

### Documentation Checks

"Documentation" is the context of these checks is the documentation found in the `docs/` directory of the provider. This include contributor and related guides. This is developer-facing unlike the [Examples](#examples-checks) and [Website](#website-checks) checks.

#### markdown-link-check

Use the target `docs-link-check` to check links found in the contributor documentation:

```console
make docs-link-check
```

**NOTE:** Install [Docker](https://docs.docker.com/desktop/install/mac-install/) to run this check.

#### markdown-lint

Use the target `docs-markdown-lint` to lint the contributor documentation:

```console
make docs-markdown-lint
```

**NOTE:** Install [Docker](https://docs.docker.com/desktop/install/mac-install/) to run this check.

#### misspell

Use the target `docs-misspell` to spellcheck the contributor documentation:

```console
make docs-misspell
```

**NOTE:** Install [tools](#before-running-tests) before running this check.

### Examples Checks

These checks help ensure that examples included with the provider are correct.

#### tflint

Use the target `examples-tflint` to lint the examples:

```console
make examples-tflint
```

**NOTE:** Install [tools](#before-running-tests) before running this check.

#### validate-terraform (0.12.31)

This check is not currently available in the Makefile.

#### validate-terraform (1.0.6)

This check is not currently available in the Makefile.

### golangci-lint Checks

golangci-lint checks runs a variety of linters on the provider's code. This is done in two stages with the first stage acting as a gatekeeper since the second stage takes considerably longer to run.

Before running these checks locally, you need to install golangci-lint locally. This can be done in [several ways](https://golangci-lint.run/welcome/install/#local-installation) including using Homebrew on macOS:

```console
brew install golangci-lint
```

Use the target `golangci-lint` to run both checks sequentially:

```console
make golangci-lint
```

You can limit the checks to a specific service package. For example:

```console
PKG=rds make golangci-lint
```

#### 1 of 2

Use the `golangci-lint1` target to run only the first step of these checks:

```console
make golangci-lint1
```

#### 2 of 2

Use the `golangci-lint2` target to run only the second step of these checks:

```console
make golangci-lint2
```

**Tip:** Running the second step against the entire codebase often takes the longest of all CI tests. If you're only working in one service package, you can save a lot of time limiting the scan to that service:

```console
PKG=rds make golangci-lint2
```

### GoReleaser CI / build-32-bit

GoReleaser CI build-32-bit ensures that GoReleaser can build a 32-bit binary. This check catches rare but important edge cases. Currently, we do not offer a `make` target to run this check locally.

### Provider Checks

Provider checks are a suite of tests that ensure Go code functions and markdown is correct.

#### go-build

This check determines if the code compiles correctly, there are syntax errors, or there are any unresolved references.

There are two ways to run this check that are basically equivalent.

Use the `go-build` target to build the provider using `go build`, installing the provider in the `terraform-plugin-dir` directory:

```console
make go-build
```

Similarly, use the `build` target to install the provider binary locally using `go install`:

```console
make build
```

#### go_generate

`go_generate` checks to make sure nothing changes after you run the code generators. In other words, generated code and committed code should be in sync or we'll say, "bye bye bye."

Use the `gen-check` target to run the check:

```console
make gen-check
```

Use the `gen` target to run all the generators associated with the provider. Unless you're working on the generators or have inadvertently edited generated code, there should be no changes to the codebase after the generators finish:

```console
make gen
```

**NOTE:** While running the generators, you may see hundreds or thousands of code changes as `make` and the generators delete and recreate files.

#### go_test

`go_test` compiles the code and runs all tests except the [acceptance tests](running-and-writing-acceptance-tests.md). This check may also find higher level code errors than building alone finds.

Use the `test` target to run this test:

```console
make test
```

You can limit `test` to a single service package with the `PKG` environment variable:

```console
PKG=rds make test
```

**NOTE:** `test` and `golangci-lint2` are generally the longest running checks and, depending on your computer, may take considerable time to finish.

#### import-lint

`import-lint` uses [impi](https://github.com/pavius/impi) to make sure that imports in Go files follow the order of _standard_, _third party_, and then _local_. Besides neatness, enforcing the order helps avoid meaningless Git differences. In earlier days of Go, it was possible to order imports more freely. This check may no longer be needed but we need additional verification.

To run this check locally, you will need to install `impi`, which is done as part of `make tools`.

Use the `import-lint` target to run `impi` with the appropriate parameters:

```console
make import-lint
```

#### markdown-lint

`markdown-lint` can be a little confusing since it shows up in CI in three different contexts, each performing slightly different checks:

1. Provider Check / markdown-lint (this check)
2. Documentation Checks / markdown-lint
3. Website Checks / markdown-lint

This particular check uses [markdownlint](https://github.com/DavidAnson/markdownlint) to check all Markdown files in the provider except those in `docs` and `website/docs`, the CHANGELOG, and an example.

Use the `provider-markdown-lint` target to run this test:

```console
make provider-markdown-lint
```

**NOTE:** Install [Docker](https://docs.docker.com/desktop/install/mac-install/) to run this check.

#### misspell

Use `go-misspell` to check the provider code for misspellings:

```console
make go-misspell
```

**NOTE:** Install [tools](#before-running-tests) before running this check.

#### terraform providers schema

This process generates the Terraform AWS Provider schema for use by the `tfproviderdocs` check. In the `make` file, this is done as part of the `tfproviderdocs` target test.

#### tfproviderdocs

**NOTE:** To run this test, you need Terraform installed locally. On macOS, you can use Homebrew to install Terraform:

```console
brew install terraform
```

This test builds the provider binary, loads the provider with Terraform, generates the provider schema, and then uses the tfproviderdocs tool to ensure the provider (via the schema) and documentation are consistent with each other.

Use the `tfproviderdocs` target to run this test:

```console
make tfproviderdocs
```

#### Sweeper Functions Not Linked

This check builds the Terraform AWS Provider in two different configurations, with sweepers and without, to make sure sweepers are properly included or excluded from the builds. The normal build you would receive from the Terraform Registry does not include sweepers and this ensures they aren't accidentally included.

Use the `sweeper-check` target to run both tests:

```console
make sweeper-check
```

You can also run the checks separately.

Use the `sweeper-linked` target to ensure sweeper are included in a sweeper build:

```console
make sweeper-linked
```

Use the `sweeper-unlinked` target to ensure sweeper are not included in a normal build:

```console
make sweeper-unlinked
```

### ProviderLint Checks / providerlint

ProviderLint checks for a variety of best practices. For more details on specific checks and errors, see [providerlint](https://github.com/hashicorp/terraform-provider-aws/tree/main/.ci/providerlint).

Use the `provider-lint` target to run the check just as it runs in CI:

```console
make provider-lint
```

### Semgrep Checks

We use [Semgrep](https://github.com/semgrep/semgrep) for many types of checks and cannot describe all of them here. They are broken into rough groupings for parallel CI processing, as described below.

To locally run Semgrep checks using `make`, you'll need to install Semgrep locally. On macOS, you can do this easily using Homebrew:

```console
brew install semgrep
```

#### Code Quality Scan

This scan looks for a hodgepodge of issues, best practices, and problems we've found over the years.

Use the `semgrep-code-quality` target to run the same check CI runs:

```console
make semgrep-code-quality
```

You can limit the scan to a service package by using the `PKG` environment variable:

```console
PKG=rds make semgrep-code-quality
```

#### Naming Scan Caps/AWS/EC2

Idiomatic Go uses [_mixed caps_](naming.md#mixed-caps) for multiword names, not camel case. In camel case, a name with the words "SMTP thing" would be `SmtpThing`. This is wrong in Go. In mixed caps, and therefore idiomatic Go, `SMTPThing` is correct. This scan ensures that many acronyms and initialisms are capitalized correctly in code.

Use the `semgrep-naming-cae` target to run the same check CI runs:

```console
make semgrep-naming-cae
```

You can limit the scan to a service package by using the `PKG` environment variable:

```console
PKG=rds make semgrep-naming-cae
```

#### Service Name Scan A-Z

This scan ensures that AWS service names are used fairly consistently from one service package to the next.

Use the `semgrep-service-naming` target to run the same check CI runs:

```console
make semgrep-service-naming
```

You can limit the scan to a service package by using the `PKG` environment variable:

```console
PKG=rds make semgrep-service-naming
```

#### Test Configs Scan

This scan checks for consistency in naming of test-related functions.

Use the `semgrep-naming` target to run the same check CI runs:

```console
make semgrep-naming
```

You can limit the scan to a service package by using the `PKG` environment variable:

```console
PKG=rds make semgrep-naming
```

### Skaff Checks / Compile skaff

Use the `skaff-check-compile` target to test building Skaff:

```console
make skaff-check-compile
```

### Website Checks

These checks help ensure that user-facing documentation on the website is correct.

#### markdown-link-check-a-h-markdown

Use the target `website-link-check-markdown` to check links found in the website:

```console
make website-link-check-markdown
```

**NOTE:** Install [Docker](https://docs.docker.com/desktop/install/mac-install/) to run this check.

#### markdown-link-check-i-z-markdown

This range is also checked as part of the "a-h" check above.

#### markdown-link-check-md

Use the target `website-link-check-md` to check links found in the website:

```console
make website-link-check-md
```

**NOTE:** Install [Docker](https://docs.docker.com/desktop/install/mac-install/) to run this check.

#### markdown-lint

Use the target `website-markdown-lint` to lint the website documentation:

```console
make website-markdown-lint
```

**NOTE:** Install [Docker](https://docs.docker.com/desktop/install/mac-install/) to run this check.

#### misspell

Use the target `website-misspell` to spellcheck the documentation:

```console
make website-misspell
```

**NOTE:** Install [tools](#before-running-tests) before running this check.

#### terrafmt

Use the target `website-terrafmt` to check formatting of Terraform configuration in documentation:

```console
make website-terrafmt
```

**NOTE:** Install [tools](#before-running-tests) before running this check.

#### tflint

Use the target `website-tflint` to check formatting of Terraform configuration in documentation:

```console
make website-tflint
```

**NOTE:** Install [tools](#before-running-tests) before running this check.

### Workflow Linting / actionlint

Use the `gh-workflow-lint` target to perform the check:

```console
make gh-workflow-lint
```

**NOTE:** Install [tools](#before-running-tests) before running this check.

### YAML Linting / yamllint

YAMLlint checks the validity of YAML files.

To run YAMLlint locally using `make`, you'll need to install it locally. On macOS, you can install it using Homebrew:

```console
brew install yamllint
```

Use the `yamllint` target to perform the check:

```console
make yamllint
```
# Terraform AWS Provider Core Services

Core Services are AWS services we have identified as critical for a large majority of our users. Our goal is to continually increase the depth of coverage for these services. We will work to prioritize features and enhancements to these services in each weekly release, even if they are not necessarily highlighted in our quarterly roadmap.

The core services we have identified are:

* EC2

* Lambda

* EKS

* ECS

* VPC

* S3

* RDS

* DynamoDB

* IAM

* Autoscaling (ASG)

* ElastiCache

We'll continue to evaluate the selected services as our user base grows and changes.
<!-- markdownlint-configure-file { "code-block-style": false } -->
# Data Handling and Conversion

The Terraform AWS Provider codebase bridges the implementation of a [Terraform Plugin](https://www.terraform.io/plugin/how-terraform-works) and an AWS API client to support AWS operations and data types as Terraform Resources. Data handling and conversion is a large portion of resource implementation given the domain-specific implementations of each side of the provider. The first is where Terraform is a generic infrastructure as code tool with a generic data model and the other is where the details are driven by AWS API data modeling concepts. This guide is intended to explain and show preferred Terraform AWS Provider code implementations required to successfully translate data between these two systems.

At the bottom of this documentation is a [Glossary section](#glossary), which may be a helpful reference while reading the other sections.

## Data Conversions in Terraform Providers

Before getting into highly specific documentation about the Terraform AWS Provider handling of data, it may be helpful to briefly highlight how Terraform Plugins (Terraform Providers in this case) interact with Terraform CLI and the Terraform State in general and where this documentation fits into the whole process.

There are two primary data flows that are typically handled by resources within a Terraform Provider.
Data is either converted from a planned new Terraform State into making a remote system request, referred to as "Expanding",
or a remote system response is converted into an applied new Terraform State, referred to as "Flattening".
The semantics of how the data of the planned new Terraform State is surfaced to the resource implementation is determined by where a resource is in its lifecycle and is mainly handled by Terraform CLI.
This concept can be explored further in the [Terraform Resource Instance Change Lifecycle documentation](https://github.com/hashicorp/terraform/blob/main/docs/resource-instance-change-lifecycle.md), with the caveat that some additional behaviors occur within the Terraform Plugin SDK as well (if the Terraform Plugin uses that implementation detail).

As a generic walkthrough, the following data handling occurs when creating a Terraform Resource:

- An operator creates a Terraform configuration with a new resource defined and runs `terraform apply`
- Terraform CLI merges an empty prior state for the resource, along with the given configuration state, to create a planned new state for the resource
- Terraform CLI sends a Terraform Plugin Protocol request to create the new resource with its planned new state data
- If the Terraform Plugin is using a higher-level library, such as the Terraform Plugin Framework, that library receives the request and translates the Terraform Plugin Protocol data types into the expected library types
- Terraform Plugin invokes the resource creation function with the planned new state data
    - **The planned new state data is converted into a remote system request (e.g., API creation request) that is invoked**
    - **The remote system response is received and the data is converted into an applied new state**
- If the Terraform Plugin is using a higher-level library, such as the Terraform Plugin Framework, that library translates the library types back into Terraform Plugin Protocol data types
- Terraform Plugin responds to Terraform Plugin Protocol request with the new state data
- Terraform CLI verifies and stores the new state

The lines in bold above are the focus of this page.

### Implicit State Passthrough

An important behavior to note with Terraform State handling is if the value of a particular root attribute or block is not refreshed during plan or apply operations, then the prior Terraform State is implicitly deep copied to the new Terraform State for that attribute or block.

Given a resource with a writeable root attribute named `not_set_attr` that never explicitly writes a value, the following happens:

- If the Terraform configuration contains `not_set_attr = "anything"` on resource creation, the Terraform State contains `not_set_attr` equal to `"anything"` after apply.
- If the Terraform configuration is updated to `not_set_attr = "updated"`, the Terraform State contains `not_set_attr` equal to `"updated"` after apply.
- If the attribute was meant to be associated with a remote system value, it will never update the Terraform State on plan or apply with the remote value. Effectively, it cannot perform drift detection with the remote value.

This however does _not_ apply to nested attributes and blocks if the parent block is refreshed.
Given a resource with a root block named `parent`, with nested child attributes `set_attr` and `not_set_attr`, a read operation which updates the value of `parent` (and the nested `set_attr` attribute) will not copy the Terraform State for the nested `not_set_attr` attribute.

There are valid use cases for passthrough attribute values such as these (see the [Virtual Attributes section](#virtual-attributes)), however the behavior can be confusing or incorrect for operators if the drift detection is expected.
Typically these types of drift detection issues can be discovered by implementing resource import testing with state verification.

## Terraform Plugin Framework versus Plugin SDK V2

Perhaps the most distinct difference between [Terraform Plugin Framework](https://developer.hashicorp.com/terraform/plugin/framework) and [Terraform Plugin SDKv2](https://developer.hashicorp.com/terraform/plugin/sdkv2) is data handling.
With Terraform Plugin Framework state data is strongly typed, while Plugin SDK V2 based resources represent state data generically (each attribute is an `interface{}`) and types must be asserted at runtime.
Strongly typed data eliminates an entire class of runtime bugs and crashes, but does require compile type declarations and a slightly different approach to reading and writing data.
The sections below contain examples for both plugin libraries, but Terraform Plugin Framework is **required for all net-new resources**.

## Data Conversions in the Terraform AWS Provider

To expand on the data handling that occurs specifically within the Terraform AWS Provider resource implementations, the above resource creation items become the below in practice given our current usage of the Terraform Plugin SDK:

=== "Terraform Plugin Framework (Preferred)"
    - The `Create` method of a resource is invoked with `resource.CreateRequest` containing the planned new state data (`req.Plan`) and an AWS API client (stored in the `Meta()` method of the resource struct).
        - Before reaching this point, the `Plan` data was already translated from the Terraform Plugin Protocol data types by the Terraform Plugin Framework so values can be read by invoking `req.Plan.Get(ctx, &plan)`, where `plan` is an instance of the struct representing the resources data.
    - An AWS Go SDK operation input type (e.g., `ec2.CreateVpcInput`) is initialized
    - For each necessary field to configure in the operation input type, the data is read from the `plan` struct and converted into the AWS Go SDK type for the field (e.g., `*string`)
    - The AWS Go SDK operation is invoked and the output type (e.g., `*ec2.CreateVpcOutput`) is initialized
    - For each necessary Attribute, Block, or resource identifier to be saved in the state, the data is read from the AWS Go SDK type for the field (`*string`), if necessary converted into the equivalent Plugin Framework compatible type, and saved into a mutated data struct
    - Function is returned

=== "Terraform Plugin SDK V2"
    - The `CreateWithoutTimeout` function of a `schema.Resource` is invoked with `*schema.ResourceData` containing the planned new state data (conventionally named `d`) and an AWS API client (conventionally named `meta`).
        - Before reaching this point, the `ResourceData` was already translated from the Terraform Plugin Protocol data types by the Terraform Plugin SDK so values can be read by invoking `d.Get()` and `d.GetOk()` receiver methods with Attribute and Block names from the `Schema` of the `schema.Resource`.
    - An AWS Go SDK operation input type (e.g., `ec2.CreateVpcInput`) is initialized
    - For each necessary field to configure in the operation input type, the data is read from the `ResourceData` (e.g., `d.Get()`, `d.GetOk()`) and converted into the AWS Go SDK type for the field (e.g., `*string`)
    - The AWS Go SDK operation is invoked and the output type (e.g., `*ec2.CreateVpcOutput`) is initialized
    - For each necessary Attribute, Block, or resource identifier to be saved in the state, the data is read from the AWS Go SDK type for the field (`*string`), if necessary converted into a `ResourceData` compatible type, and saved into a mutated `ResourceData` (e.g., `d.Set()`, `d.SetId()`)
    - Function is returned

### Type Mapping

To further understand the necessary data conversions used throughout the Terraform AWS Provider codebase between AWS Go SDK types and the Terraform Plugin SDK, the following table can be referenced for most scenarios:

=== "Terraform Plugin Framework (Preferred)"
    <!-- markdownlint-disable no-inline-html --->

    | AWS API Model | AWS Go SDK V2 | Terraform Plugin Framework | Terraform Language/State |
    |---------------|---------------|----------------------------|--------------------------|
    | `boolean` | `bool` | `types.Bool` | `bool` |
    | `float` | `*float64` | `types.Float64` | `number` |
    | `integer` | `*int64` | `types.Int64` | `number` |
    | `list` | `[]*T` | `types.List` <br/>`types.Set` | `list(any)`<br/>`set(any)` |
    | `map` | `map[T1]*T2` | `types.Map` | `map(any)` |
    | `string` | `*string` | `types.String` | `string` |
    | `structure` | `struct` | `types.List` with `MaxItems: 1` | `list(object(any))` |
    | `timestamp` | `*time.Time` | `types.String` (typically RFC3339 formatted) | `string` |

    <!-- markdownlint-enable no-inline-html --->

    [Types](https://developer.hashicorp.com/terraform/plugin/framework/handling-data/types) are built into the Terraform Plugin Framework library and handle null and unknown values in accordance with the [Terraform type system](https://developer.hashicorp.com/terraform/plugin/framework/handling-data/terraform-concepts#type-system).
    This eliminates the need for any special handling of zero values and provides better change detection on unset values.

=== "Terraform Plugin SDK V2"
    <!-- markdownlint-disable no-inline-html --->

    | AWS API Model | AWS Go SDK | Terraform Plugin SDK | Terraform Language/State |
    |---------------|------------|----------------------|--------------------------|
    | `boolean` | `*bool` | `TypeBool` (`bool`) | `bool` |
    | `float` | `*float64` | `TypeFloat` (`float64`) | `number` |
    | `integer` | `*int64` | `TypeInt` (`int`) | `number` |
    | `list` | `[]*T` | `TypeList` (`[]interface{}` of `T`)<br/>`TypeSet` (`*schema.Set` of `T`) | `list(any)`<br/>`set(any)` |
    | `map` | `map[T1]*T2` | `TypeMap` (`map[string]interface{}`) | `map(any)` |
    | `string` | `*string` | `TypeString` (`string`) | `string` |
    | `structure` | `struct` | `TypeList` (`[]interface{}` of `map[string]interface{}`) with `MaxItems: 1` | `list(object(any))` |
    | `timestamp` | `*time.Time` | `TypeString` (typically RFC3339 formatted) | `string` |

    <!-- markdownlint-enable no-inline-html --->

    You may notice there are type encoding differences between the AWS Go SDK and Terraform Plugin SDK:

    - AWS Go SDK types are all Go pointer types, while Terraform Plugin SDK types are not.
    - AWS Go SDK structures are the Go `struct` type, while there is no semantically equivalent Terraform Plugin SDK type. Instead they are represented as a slice of interfaces with an underlying map of interfaces.
    - AWS Go SDK types are all Go concrete types, while the Terraform Plugin SDK types for collections and maps are interfaces.
    - AWS Go SDK whole numeric type is always 64-bit, while the Terraform Plugin SDK type is implementation-specific.

    Conceptually, the first and second items above are the most problematic in the Terraform AWS Provider codebase. The first item because non-pointer types in Go cannot implement the concept of no value (`nil`). The [Zero Value Mapping section](#zero-value-mapping) will go into more detail about the implications of this limitation. The second item because it can be confusing to always handle a structure ("object") type as a list.

### Zero Value Mapping

!!! note
    This section only applies to Plugin SDK V2 based resources. Terraform Plugin Framework based resources will handle null and unknown values distinctly from zero values.

As mentioned in the [Type Mapping section](#type-mapping) for Terraform Plugin SDK V2, there is a discrepancy between how the Terraform Plugin SDK represents values and the reality that a Terraform State may not configure an Attribute.
These values will default to the matching underlying Go type "zero value" if not set:

| Terraform Plugin SDK | Go Type | Zero Value |
|----------------------|---------|------------|
| `TypeBool` | `bool` | `false` |
| `TypeFloat` | `float64` | `0.0` |
| `TypeInt` | `int` | `0` |
| `TypeString` | `string` | `""` |

For Terraform resource logic this means that these special values must always be accounted for in implementation.
The semantics of the API and its meaning of the zero value will determine whether:

- If it is not used/needed, then generally the zero value can safely be used to store an "unset" value and should be ignored when sending to the API.
- If it is used/needed, whether:
    - A value can always be set and it is safe to always send to the API. Generally, boolean values fall into this category.
    - A different default/sentinel value must be used as the "unset" value so it can either match the default of the API or be ignored when sending to the API.
    - A special type implementation is required within the schema to work around the limitation.

The maintainers can provide guidance on appropriate solutions for cases not mentioned in the [Recommended Implementation section](#recommended-implementations).

### Root Attributes Versus Block Attributes

=== "Terraform Plugin Framework (Preferred)"
    All Attributes and Blocks at the top level of a resource structs `Schema` method are considered "root" attributes.
    These will always be handled with the `Plan` and `State` fields from the request and response pointers passed in as arguments the the CRUD methods on the resource struct.
    Values are read from and written to the underlying data structure during CRUD operations, and finally written to state in the response object with a call like `resp.Diagnostics.Append(resp.State.Set(ctx, &plan)...)`.

=== "Terraform Plugin SDK V2"
    All Attributes and Blocks at the top level of `schema.Resource` `Schema` are considered "root" attributes.
    These will always be handled with receiver methods on `ResourceData`, such as reading with `d.Get()`, `d.GetOk()`, etc. and writing with `d.Set()`.
    Any nested Attributes and Blocks inside those root Blocks will then be handled with standard Go types according to the table in the [Type Mapping section](#type-mapping).

    !!! warning
        While it is possible in certain type scenarios to deeply read and write ResourceData information for a Block Attribute, this practice is discouraged in preference of only handling root Attributes and Blocks.

## Recommended Implementations

Given the complexities around conversions between AWS and Terraform Plugin type systems, this section contains recommended implementations for Terraform AWS Provider resources.

!!! tip
    Some of these coding patterns may not be well represented in the codebase, as refactoring the many older styles over years of community development is a large task.
    However this is meant to represent the preferred implementations today.
    These will continue to evolve as this codebase and the Terraform Plugin ecosystem changes.

When using the Terraform Plugin Framework, there are two approaches for flattening and expanding Terraform data.
The preferred is AutoFlex, which automatically converts between provider and AWS API structures by analyzing type information.
Alternatively, provider developers can define flattening and expanding functions manually.

When using the Terraform Plugin SDK v2, flattening and expanding functions must be defined manually.

### AutoFlex for Terraform Plugin Framework (Preferred)

AutoFlex provides two entry-point functions, `Flatten` and `Expand` defined in the package `github.com/hashicorp/terraform-provider-aws/internal/framework/flex`.
Without configuration, these two functions should be able to convert most provider and AWS API structures.

AutoFlex uses field names to map between the source and target structures:

1. An exact, case-sensitive match
1. An exact, case-insensitive match
1. Comparing plural and singular field names
1. Adding a field name prefix set using the AutoFlex options function `flex.WithFieldNamePrefix`, e.g. Lex v2 Intents in `internal/service/lexv2models/intent.go`

By default, AutoFlex ignores fields with the name `Tags`, as AWS resource tags are [handled separately](./resource-tagging.md).
Additional fields can be ignored and the `Tags` field can be included by passing optional `flex.AutoFlexOptionsFunc`s to `Flatten` or `Expand`.
For example, to add an additional ignored field, use

```go
diags := flex.Expand(ctx, source, &target, flex.WithIgnoredFieldNamesAppend("OtherField"))
```

This will ignore both `Tags` and `OtherField`.
To empty the list of ignored fields, use `flex.WithNoIgoredFieldNames`.
For example, to include `Tags`, call

```go
diags := flex.Expand(ctx, source, &target, flex.WithNoIgnoredFieldNames())
```

AutoFlex is able to convert single-element lists from Terraform blocks into single struct or pointer values in AWS API structs.

#### Customizing Struct Field Flexing

The flexing of individual struct fields can be customized by using Go struct tags, with the namespace `autoflex`.

Tag values are comma-separated lists of options, with a leading comma.

The option `legacy` can be used when migrating a resource or data source from the Terraform Plugin SDK to the Terraform Plugin Framework.
This will preserve certain behaviors from the Plugin SDK, such as treating zero-values, i.e. the empty string or a numeric zero, equivalently to `null` values.
This is equivalent to calling the `fwflex.<Type><To/From>FrameworkLegacy` functions.

For example, from the struct `resourceManagedUserPoolClientModel` for the Cognito IDP Managed User Pool Client:

```go
type resourceManagedUserPoolClientModel struct {
	AccessTokenValidity                      types.Int64  `tfsdk:"access_token_validity" autoflex:",legacy"`
	AllowedOauthFlows                        types.Set    `tfsdk:"allowed_oauth_flows"`
	...
	ClientSecret                             types.String `tfsdk:"client_secret"`
	DefaultRedirectUri                       types.String `tfsdk:"default_redirect_uri" autoflex:",legacy"`
	...
	ID                                       types.String `tfsdk:"id"`
	IdTokenValidity                          types.Int64  `tfsdk:"id_token_validity" autoflex:",legacy"`
	LogoutUrls                               types.Set    `tfsdk:"logout_urls"`
	...
}
```

The option `omitempty` can be used with `string` values to store a `null` value when an empty string is returned.

For example, from the struct `refreshOnDayModel` for the QuickSight Refresh Schedule:

```go
type refreshOnDayModel struct {
	DayOfMonth types.String `tfsdk:"day_of_month"`
	DayOfWeek  types.String `tfsdk:"day_of_week" autoflex:",omitempty"`
}
```

To completely ignore a field, use the tag value `-`.

For example, from the struct `scheduleModel` for the QuickSight Refresh Schedule:

```go
type scheduleModel struct {
	RefreshType        types.String                                           `tfsdk:"refresh_type"`
	ScheduleFrequency  fwtypes.ListNestedObjectValueOf[refreshFrequencyModel] `tfsdk:"schedule_frequency"`
	StartAfterDateTime types.String                                           `tfsdk:"start_after_date_time" autoflex:"-"`
}
```

To ignore a field when flattening, but include it when expanding, use the option `noflatten`.

For example, from the struct `dataSourceReservedCacheNodeOfferingModel` for the ElastiCache Reserved Cache Node Offering:

```go
type dataSourceReservedCacheNodeOfferingModel struct {
	CacheNodeType      types.String            `tfsdk:"cache_node_type"`
	Duration           fwtypes.RFC3339Duration `tfsdk:"duration" autoflex:",noflatten"`
	FixedPrice         types.Float64           `tfsdk:"fixed_price"`
	OfferingID         types.String            `tfsdk:"offering_id"`
	OfferingType       types.String            `tfsdk:"offering_type"`
	ProductDescription types.String            `tfsdk:"product_description"`
}
```

#### Overriding Default Behavior

In some cases, flattening and expanding need conditional handling.
One important case is new AWS API implementations where the input or output structs make use of [union types](https://smithy.io/2.0/spec/aggregate-types.html#union).
The AWS implementation uses an interface as the common type, along with various concrete implementations.
Because the Terraform schema does not support union types (see https://github.com/hashicorp/terraform/issues/32587 for discussion), the provider defines nested schemas for each type with a restriction to allow only one.

To override flattening behavior, implement the interface `flex.Flattener` on the model.
The function should have a pointer receiver, as it will modify the struct in-place.
From the Mainframe Modernization (M2) environment (`internal/service/m2/environment.go`):

```go
type storageConfigurationModel struct {
	EFS fwtypes.ListNestedObjectValueOf[efsStorageConfigurationModel] `tfsdk:"efs"`
	FSX fwtypes.ListNestedObjectValueOf[fsxStorageConfigurationModel] `tfsdk:"fsx"`
}

func (m *storageConfigurationModel) Flatten(ctx context.Context, v any) (diags diag.Diagnostics) {
	switch t := v.(type) {
	case awstypes.StorageConfigurationMemberEfs:
		var model efsStorageConfigurationModel
		d := fwflex.Flatten(ctx, t.Value, &model)
		diags.Append(d...)
		if diags.HasError() {
			return diags
		}

		m.EFS = fwtypes.NewListNestedObjectValueOfPtrMust(ctx, &model)

		return diags

	case awstypes.StorageConfigurationMemberFsx:
		var model fsxStorageConfigurationModel
		d := fwflex.Flatten(ctx, t.Value, &model)
		diags.Append(d...)
		if diags.HasError() {
			return diags
		}

		m.FSX = fwtypes.NewListNestedObjectValueOfPtrMust(ctx, &model)

		return diags

	default:
		return diags
	}
}
```

To override expanding behavior, implement the interface `flex.Expander` on the model.
As the function should not modify the struct in-place, it should not have a pointer receiver.
From the Mainframe Modernization (M2) environment (`internal/service/m2/environment.go`):

```go
type storageConfigurationModel struct {
	EFS fwtypes.ListNestedObjectValueOf[efsStorageConfigurationModel] `tfsdk:"efs"`
	FSX fwtypes.ListNestedObjectValueOf[fsxStorageConfigurationModel] `tfsdk:"fsx"`
}

func (m storageConfigurationModel) Expand(ctx context.Context) (result any, diags diag.Diagnostics) {
	switch {
	case !m.EFS.IsNull():
		efsStorageConfigurationData, d := m.EFS.ToPtr(ctx)
		diags.Append(d...)
		if diags.HasError() {
			return nil, diags
		}

		var r awstypes.StorageConfigurationMemberEfs
		diags.Append(fwflex.Expand(ctx, efsStorageConfigurationData, &r.Value)...)
		if diags.HasError() {
			return nil, diags
		}

		return &r, diags

	case !m.FSX.IsNull():
		fsxStorageConfigurationData, d := m.FSX.ToPtr(ctx)
		diags.Append(d...)
		if diags.HasError() {
			return nil, diags
		}

		var r awstypes.StorageConfigurationMemberFsx
		diags.Append(fwflex.Expand(ctx, fsxStorageConfigurationData, &r.Value)...)
		if diags.HasError() {
			return nil, diags
		}

		return &r, diags
	}

	return nil, diags
}
```

In some cases, the result types for expanding will be different when creating or updating a resource.
For example, for the Verified Permissions identity source, the create operation takes a `Configuration` struct while the update operation takes an `UpdateConfiguration`, even though the contents are identical.
In this case, implement the interface `flex.TypedExpander` on the model.
From the Verified Permissions identity source (`internal/service/verifiedpermissions/identity_source.go`):

```go
type configuration struct {
	CognitoUserPoolConfiguration fwtypes.ListNestedObjectValueOf[cognitoUserPoolConfiguration] `tfsdk:"cognito_user_pool_configuration"`
	OpenIDConnectConfiguration   fwtypes.ListNestedObjectValueOf[openIDConnectConfiguration]   `tfsdk:"open_id_connect_configuration"`
}


func (m configuration) ExpandTo(ctx context.Context, targetType reflect.Type) (result any, diags diag.Diagnostics) {
	switch targetType {
	case reflect.TypeFor[awstypes.Configuration]():
		return m.expandToConfiguration(ctx)

	case reflect.TypeFor[awstypes.UpdateConfiguration]():
		return m.expandToUpdateConfiguration(ctx)
	}
	return nil, diags
}

func (m configuration) expandToConfiguration(ctx context.Context) (result awstypes.Configuration, diags diag.Diagnostics) {
	switch {
	case !m.CognitoUserPoolConfiguration.IsNull():
		var result awstypes.ConfigurationMemberCognitoUserPoolConfiguration
		diags.Append(flex.Expand(ctx, m.CognitoUserPoolConfiguration, &result.Value)...)
		if diags.HasError() {
			return nil, diags
		}
		return &result, diags

	case !m.OpenIDConnectConfiguration.IsNull():
		var result awstypes.ConfigurationMemberOpenIdConnectConfiguration
		diags.Append(flex.Expand(ctx, m.OpenIDConnectConfiguration, &result.Value)...)
		if diags.HasError() {
			return nil, diags
		}
		return &result, diags
	}

	return nil, diags
}

func (m configuration) expandToUpdateConfiguration(ctx context.Context) (result awstypes.UpdateConfiguration, diags diag.Diagnostics) {
	switch {
	case !m.CognitoUserPoolConfiguration.IsNull():
		var result awstypes.UpdateConfigurationMemberCognitoUserPoolConfiguration
		diags.Append(flex.Expand(ctx, m.CognitoUserPoolConfiguration, &result.Value)...)
		if diags.HasError() {
			return nil, diags
		}
		return &result, diags

	case !m.OpenIDConnectConfiguration.IsNull():
		var result awstypes.UpdateConfigurationMemberOpenIdConnectConfiguration
		diags.Append(flex.Expand(ctx, m.OpenIDConnectConfiguration, &result.Value)...)
		if diags.HasError() {
			return nil, diags
		}
		return &result, diags
	}

	return nil, diags
}
```

#### Troubleshooting

AutoFlex can output detailed logging as it flattens or expands a value.
To turn on logging for AutoFlex, use the environment variable `TF_LOG_AWS_AUTOFLEX` to set the logging level.
Valid values are `ERROR`, `WARN`, `INFO`, `DEBUG`, and `TRACE`.
By default, AutoFlex logging is set to `ERROR`.

### Manually Defined Flattening and Expanding Functions

By convention in the codebase, each level of Block handling beyond root attributes should be separated into "expand" functions that convert Terraform Plugin SDK data into the equivalent AWS Go SDK type (typically named `expand{Service}{Type}`) and "flatten" functions that convert an AWS Go SDK type into the equivalent Terraform Plugin SDK data (typically named `flatten{Service}{Type}`).

Define FLatten and EXpand (i.e., flex) functions at the _most local level_ possible. This table provides guidance on the preferred place to define flex functions based on usage.

| Where Used | Where to Define | Include Service in Name |
|---------------|------------|--------|
| One resource (e.g., `aws_instance`) | Resource file (e.g., `internal/service/ec2/instance.go`) | No |
| Few resources in one service (e.g., `EC2`) | Resource file or service flex file (e.g., `internal/service/ec2/flex.go`) | No |
| Widely used in one service (e.g., `EC2`) | Service flex file (e.g., `internal/service/ec2/flex.go`) | No |
| Two services (e.g., `EC2` and `EKS`) | Define a copy in each service | If helpful |
| 3+ services | `internal/flex/flex.go` | Yes |

### Expand Functions for Blocks

=== "Terraform Plugin Framework (Preferred)"
    ```go
    func expandStructure(tfList []structureData) *service.Structure {
        if len(tfList) == 0 {
            return nil
        }

        tfObj := tfList[0]
        apiObject := &service.Structure{}

        // ... nested attribute handling ...
        
        return apiObject
    }

    func expandStructures(tfList []structureData) []*service.Structure {
        if len(tfList) == 0 {
            return nil
        }

        var apiObjects []*service.Structure
        for _, tfObj := range tfList {
            apiObject := &service.Structure{}

            // ... nested attribute handling ...

            apiObjects = append(apiObjects, apiObject)
        }

        return apiObjects
    }
    ```

=== "Terraform Plugin SDK V2"
    ```go
    func expandStructure(tfMap map[string]interface{}) *service.Structure {
        if tfMap == nil {
            return nil
        }

        apiObject := &service.Structure{}

        // ... nested attribute handling ...

        return apiObject
    }

    func expandStructures(tfList []interface{}) []*service.Structure {
        if len(tfList) == 0 {
            return nil
        }

        var apiObjects []*service.Structure

        for _, tfMapRaw := range tfList {
            tfMap, ok := tfMapRaw.(map[string]interface{})

            if !ok {
                continue
            }

            apiObject := expandStructure(tfMap)

            if apiObject == nil {
                continue
            }

            apiObjects = append(apiObjects, apiObject)
        }

        return apiObjects
    }
    ```

### Flatten Functions for Blocks

=== "Terraform Plugin Framework (Preferred)"
    ```go
    func flattenStructure(ctx context.Context, apiObject *service.Structure) (types.List, diag.Diagnostics) {
        var diags diag.Diagnostics
        elemType := types.ObjectType{AttrTypes: structureAttrTypes}

        if apiObject == nil {
            return types.ListNull(elemType), diags
        }
        
        obj := map[string]attr.Value{
            // ... nested attribute handling ...
        }
        objVal, d := types.ObjectValue(structureAttrTypes, obj)
        diags.Append(d...)
        
        listVal, d := types.ListValue(elemType, []attr.Value{objVal})
        diags.Append(d...)
        
        return listVal, diags
    }
    
    func flattenStructures(ctx context.Context, apiObjects []*service.Structure) (types.List, diag.Diagnostics) {
        var diags diag.Diagnostics
        elemType := types.ObjectType{AttrTypes: structureAttrTypes}
        
        if len(apiObjects) == 0 {
            return types.ListNull(elemType), diags
        }
        
        elems := []attr.Value{}
        for _, apiObject := range apiObjects {
            if apiObject == nil {
                continue
            }

            obj := map[string]attr.Value{
                // ... nested attribute handling ...
            }
            objVal, d := types.ObjectValue(structureAttrTypes, obj)
            diags.Append(d...)

            elems = append(elems, objVal)
        }
        
        listVal, d := types.ListValue(elemType, elems)
        diags.Append(d...)
        
        return listVal, diags
    }
    ```

=== "Terraform Plugin SDK V2"
    ```go
    func flattenStructure(apiObject *service.Structure) map[string]interface{} {
        if apiObject == nil {
            return nil
        }

        tfMap := map[string]interface{}{}
    
        // ... nested attribute handling ...
    
        return tfMap
    }
    
    func flattenStructures(apiObjects []*service.Structure) []interface{} {
        if len(apiObjects) == 0 {
            return nil
        }
    
        var tfList []interface{}
    
        for _, apiObject := range apiObjects {
            if apiObject == nil {
                continue
            }
    
            tfList = append(tfList, flattenStructure(apiObject))
        }
    
        return tfList
    }
    ```

### Root Bool and AWS Boolean

=== "Terraform Plugin Framework (Preferred)"
    To read, if always sending the attribute value is correct:

    ```go
    input := service.ExampleOperationInput{
        AttributeName: plan.AttributeName.ValueBoolPointer()
    }
    ```
    
    Alternatively, if only sending the attribute value when `true`:
    
    ```go
    input := service.ExampleOperationInput{}
    
    if v := plan.AttributeName.ValueBool(); v {
        input.AttributeName = aws.Bool(v)
    }
    ```

    Or, if only sending the attribute value when it is known and not null:
    
    ```go
    input := service.ExampleOperationInput{}
    
    if !plan.AttributeName.IsUnknown() && !plan.AttributeName.IsNull() {
        input.AttributeName = plan.AttributeName.ValueBoolPointer()
    }
    ```
    
    To write:
    
    ```go
    plan.AttributeName = flex.BoolToFramework(output.Thing.AttributeName)
    ```

=== "Terraform Plugin SDK V2"
    To read, if always sending the attribute value is correct:

    ```go
    input := service.ExampleOperationInput{
        AttributeName: aws.String(d.Get("attribute_name").(bool))
    }
    ```
    
    Otherwise to read, if only sending the attribute value when `true` is preferred (`!ok` for opposite):
    
    ```go
    input := service.ExampleOperationInput{}
    
    if v, ok := d.GetOk("attribute_name"); ok {
        input.AttributeName = aws.Bool(v.(bool))
    }
    ```
    
    To write:
    
    ```go
    d.Set("attribute_name", output.Thing.AttributeName)
    ```

### Root Float and AWS Float

=== "Terraform Plugin Framework (Preferred)"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if !plan.AttributeName.IsNull() {
        input.AttributeName = plan.AttributeName.ValueFloat64Pointer()
    }
    ```
    
    To write:
    
    ```go
    plan.AttributeName = flex.Float64ToFramework(output.Thing.AttributeName)
    ```

=== "Terraform Plugin SDK V2"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if v, ok := d.GetOk("attribute_name"); ok {
        input.AttributeName = aws.Float64(v.(float64))
    }
    ```
    
    To write:
    
    ```go
    d.Set("attribute_name", output.Thing.AttributeName)
    ```

### Root Int and AWS Integer

=== "Terraform Plugin Framework (Preferred)"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if !plan.AttributeName.IsNull() {
        input.AttributeName = plan.AttributeName.ValueInt64Pointer()
    }
    ```
    
    To write:
    
    ```go
    plan.AttributeName = flex.Int64ToFramework(output.Thing.AttributeName)
    ```

=== "Terraform Plugin SDK V2"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if v, ok := d.GetOk("attribute_name"); ok {
        input.AttributeName = aws.Int64(int64(v.(int)))
    }
    ```
    
    To write:
    
    ```go
    d.Set("attribute_name", output.Thing.AttributeName)
    ```

### Root List of Resource and AWS List of Structure

=== "Terraform Plugin Framework (Preferred)"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if !plan.AttributeName.IsNull() {
        var tfList []attributeNameData
        resp.Diagnostics.Append(plan.AttributeName.ElementsAs(ctx, &tfList, false)...)
        if resp.Diagnostics.HasError() {
            return
        }

        input.AttributeName = expandStructures(tfList)
    }
    ```
    
    To write:
    
    ```go
    attributeName, d := flattenStructures(ctx, output.Thing.AttributeName))
    resp.Diagnostics.Append(d...)
    state.AttributeName = attributeName
    ```

=== "Terraform Plugin SDK V2"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if v, ok := d.GetOk("attribute_name"); ok && len(v.([]interface{})) > 0 {
        input.AttributeName = expandStructures(v.([]interface{}))
    }
    ```
    
    To write:
    
    ```go
    if err := d.Set("attribute_name", flattenStructures(output.Thing.AttributeName)); err != nil {
        return sdkdiag.AppendErrorf(diags, "setting attribute_name: %s", err)
    }
    ```

### Root List of Resource and AWS Structure

=== "Terraform Plugin Framework (Preferred)"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if !plan.AttributeName.IsNull() {
        var tfList []attributeNameData
        resp.Diagnostics.Append(plan.AttributeName.ElementsAs(ctx, &tfList, false)...)
        if resp.Diagnostics.HasError() {
            return
        }

        // expander handles translating list with 1 item to a single AWS object
        input.AttributeName = expandStructure(tfList)
    }
    ```
    
    To write:
    
    ```go
    // flattener handles nil output, returning the equivalent null Terraform type
    attributeName, d := flattenStructures(ctx, output.Thing.AttributeName))
    resp.Diagnostics.Append(d...)
    state.AttributeName = attributeName
    ```

=== "Terraform Plugin SDK V2"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if v, ok := d.GetOk("attribute_name"); ok && len(v.([]interface{})) > 0 && v.([]interface{})[0] != nil {
        input.AttributeName = expandStructure(v.([]interface{})[0].(map[string]interface{}))
    }
    ```
    
    To write (_likely to have helper function introduced soon_):
    
    ```go
    if output.Thing.AttributeName != nil {
        if err := d.Set("attribute_name", []interface{}{flattenStructure(output.Thing.AttributeName)}); err != nil {
            return sdkdiag.AppendErrorf(diags, "setting attribute_name: %s", err)
        }
    } else {
        d.Set("attribute_name", nil)
    }
    ```

### Root List of String and AWS List of String

=== "Terraform Plugin Framework (Preferred)"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if !plan.AttributeName.IsNull() {
        input.AttributeName = flex.ExpandFrameworkStringValueList(ctx, plan.AttributeName)
    }
    ```
    
    To write:
    
    ```go
    plan.AttributeName = flex.FlattenFrameworkStringValueList(output.Thing.AttributeName)
    ```

=== "Terraform Plugin SDK V2"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if v, ok := d.GetOk("attribute_name"); ok && len(v.([]interface{})) > 0 {
        input.AttributeName = flex.ExpandStringList(v.([]interface{}))
    }
    ```
    
    To write:
    
    ```go
    d.Set("attribute_name", aws.StringValueSlice(output.Thing.AttributeName))
    ```

### Root Map of String and AWS Map of String

=== "Terraform Plugin Framework (Preferred)"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if !plan.AttributeName.IsNull() {
        input.AttributeName = flex.ExpandFrameworkStringValueMap(ctx, plan.AttributeName)
    }
    ```
    
    To write:
    
    ```go
    plan.AttributeName = flex.FlattenFrameworkStringValueMap(output.Thing.AttributeName)
    ```

=== "Terraform Plugin SDK V2"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if v, ok := d.GetOk("attribute_name"); ok && len(v.(map[string]interface{})) > 0 {
        input.AttributeName = flex.ExpandStringMap(v.(map[string]interface{}))
    }
    ```

    To write:

    ```go
    d.Set("attribute_name", aws.StringValueMap(output.Thing.AttributeName))
    ```

### Root Set of Resource and AWS List of Structure

=== "Terraform Plugin Framework (Preferred)"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if !plan.AttributeName.IsNull() {
        var tfList []attributeNameData
        resp.Diagnostics.Append(plan.AttributeName.ElementsAs(ctx, &tfList, false)...)
        if resp.Diagnostics.HasError() {
            return
        }

        input.AttributeName = expandStructure(tfList)
    }
    ```
    
    To write:
    
    ```go
    // flattener handles nil output, returning the equivalent null Terraform type
    attributeName, d := flattenStructures(ctx, output.Thing.AttributeName))
    resp.Diagnostics.Append(d...)
    state.AttributeName = attributeName
    ```

=== "Terraform Plugin SDK V2"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if v, ok := d.GetOk("attribute_name"); ok && v.(*schema.Set).Len() > 0 {
        input.AttributeName = expandStructures(v.(*schema.Set).List())
    }
    ```

    To write:

    ```go
    if err := d.Set("attribute_name", flattenStructures(output.Thing.AttributeNames)); err != nil {
        return sdkdiag.AppendErrorf(diags, "setting attribute_name: %s", err)
    }
    ```

### Root Set of String and AWS List of String

=== "Terraform Plugin Framework (Preferred)"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if !plan.AttributeName.IsNull() {
        input.AttributeName = flex.ExpandFrameworkStringValueSet(ctx, plan.AttributeName)
    }
    ```
    
    To write:
    
    ```go
    plan.AttributeName = flex.FlattenFrameworkStringValueSet(output.Thing.AttributeName)
    ```

=== "Terraform Plugin SDK V2"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if v, ok := d.GetOk("attribute_name"); ok && v.(*schema.Set).Len() > 0 {
        input.AttributeName = flex.ExpandStringSet(v.(*schema.Set))
    }
    ```

    To write:

    ```go
    d.Set("attribute_name", aws.StringValueSlice(output.Thing.AttributeName))
    ```

### Root String and AWS String

=== "Terraform Plugin Framework (Preferred)"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if !plan.AttributeName.IsNull() {
        input.AttributeName = plan.AttributeName.ValueStringPointer()
    }
    ```
    
    To write:
    
    ```go
    plan.AttributeName = flex.StringToFramework(output.Thing.AttributeName)
    ```

=== "Terraform Plugin SDK V2"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if v, ok := d.GetOk("attribute_name"); ok {
        input.AttributeName = aws.String(v.(string))
    }
    ```

    To write:

    ```go
    d.Set("attribute_name", output.Thing.AttributeName)
    ```

### Root String and AWS Timestamp

=== "Terraform Plugin Framework (Preferred)"
    To ensure that parsing the read string value does not fail, use the [RFC3339 timetype](https://pkg.go.dev/github.com/hashicorp/terraform-plugin-framework-timetypes@v0.3.0/timetypes#RFC3339).

    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if !plan.AttributeName.IsNull() {
        attributeName, d := plan.AttributeName.ValueRFC3339Time()
        resp.Diagnostics.Append(d...)
        input.AttributeName = aws.Time(attributeName)
    }
    ```
    
    To write:
    
    ```go
    plan.AttributeName = timetypes.NewRFC3339ValueMust(aws.ToTime(output.Thing.AttributeName).Format(time.RFC3339))
    ```

=== "Terraform Plugin SDK V2"
    To ensure that parsing the read string value does not fail, define `attribute_name`'s `schema.Schema` with an appropriate [`ValidateFunc`](https://www.terraform.io/plugin/sdkv2/schemas/schema-behaviors#validatefunc):

    ```go
    "attribute_name": {
        Type:         schema.TypeString,
        // ...
        ValidateFunc: validation.IsRFC3339Time,
    },
    ```

    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if v, ok := d.GetOk("attribute_name"); ok {
        v, _ := time.Parse(time.RFC3339, v.(string))
    
        input.AttributeName = aws.Time(v)
    }
    ```

    To write:

    ```go
    if output.Thing.AttributeName != nil {
        d.Set("attribute_name", aws.TimeValue(output.Thing.AttributeName).Format(time.RFC3339))
    } else {
        d.Set("attribute_name", nil)
    }
    ```

### Nested Bool and AWS Boolean

=== "Terraform Plugin Framework (Preferred)"
    To read, if always sending the attribute value is correct:

    ```go
    func expandStructure(tfList []structureData) *service.Structure {
        // ...

        apiObject.NestedAttributeName = tfObj.NestedAttributeName.ValueBoolPointer()

        // ...
    }
    ```

    To read, if only sending the attribute value when known and not nil:

    ```go
    func expandStructure(tfList []structureData) *service.Structure {
        // ...

        if !tfObj.NestedAttributeName.IsUnknown() && !tfObj.NestedAttributeName.IsNull() {
            apiObject.NestedAttributeName = tfObj.NestedAttributeName.ValueBoolPointer()
        }

        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(ctx context.Context, apiObject *service.Structure) (types.List, diag.Diagnostics) {
        // ...
    
        // flex will handle setting null when appropriate
        obj["nested_attribute_name"] = flex.BoolToFramework(ctx, apiObject.NestedAttributeName)
    
        // ...
    }
    ```

=== "Terraform Plugin SDK V2"
    To read, if always sending the attribute value is correct:

    ```go
    func expandStructure(tfMap map[string]interface{}) *service.Structure {
        // ...
    
        if v, ok := tfMap["nested_attribute_name"].(bool); ok {
            apiObject.NestedAttributeName = aws.Bool(v)
        }
    
        // ...
    }
    ```

    To read, if only sending the attribute value when `true` is preferred (`!v` for opposite):

    ```go
    func expandStructure(tfMap map[string]interface{}) *service.Structure {
        // ...
    
        if v, ok := tfMap["nested_attribute_name"].(bool); ok && v {
            apiObject.NestedAttributeName = aws.Bool(v)
        }
    
        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(apiObject *service.Structure) map[string]interface{} {
        // ...
    
        if v := apiObject.NestedAttributeName; v != nil {
            tfMap["nested_attribute_name"] = aws.ToBool(v)
        }
    
        // ...
    }
    ```

### Nested Float and AWS Float

=== "Terraform Plugin Framework (Preferred)"
    To read:

    ```go
    func expandStructure(tfList []structureData) *service.Structure {
        // ...

        if !tfObj.NestedAttributeName.IsUnknown() && !tfObj.NestedAttributeName.IsNull() {
            apiObject.NestedAttributeName = tfObj.NestedAttributeName.ValueFloat64Pointer()
        }

        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(ctx context.Context, apiObject *service.Structure) (types.List, diag.Diagnostics) {
        // ...
    
        // flex will handle setting null when appropriate
        obj["nested_attribute_name"] = flex.Float64ToFramework(ctx, apiObject.NestedAttributeName)
    
        // ...
    }
    ```

=== "Terraform Plugin SDK V2"
    To read:

    ```go
    func expandStructure(tfMap map[string]interface{}) *service.Structure {
        // ...
    
        if v, ok := tfMap["nested_attribute_name"].(float64); ok && v != 0.0 {
            apiObject.NestedAttributeName = aws.Float64(v)
        }
    
        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(apiObject *service.Structure) map[string]interface{} {
        // ...
    
        if v := apiObject.NestedAttributeName; v != nil {
            tfMap["nested_attribute_name"] = aws.ToFloat64(v)
        }
    
        // ...
    }
    ```

### Nested Int and AWS Integer

=== "Terraform Plugin Framework (Preferred)"
    To read:

    ```go
    func expandStructure(tfList []structureData) *service.Structure {
        // ...

        if !tfObj.NestedAttributeName.IsUnknown() && !tfObj.NestedAttributeName.IsNull() {
            apiObject.NestedAttributeName = tfObj.NestedAttributeName.ValueInt64Pointer()
        }

        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(ctx context.Context, apiObject *service.Structure) (types.List, diag.Diagnostics) {
        // ...
    
        // flex will handle setting null when appropriate
        obj["nested_attribute_name"] = flex.Int64ToFramework(ctx, apiObject.NestedAttributeName)
    
        // ...
    }
    ```

=== "Terraform Plugin SDK V2"
    To read:

    ```go
    func expandStructure(tfMap map[string]interface{}) *service.Structure {
        // ...
    
        if v, ok := tfMap["nested_attribute_name"].(int); ok && v != 0 {
            apiObject.NestedAttributeName = aws.Int64(int64(v))
        }
    
        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(apiObject *service.Structure) map[string]interface{} {
        // ...
    
        if v := apiObject.NestedAttributeName; v != nil {
            tfMap["nested_attribute_name"] = aws.ToInt64(v)
        }
    
        // ...
    }
    ```

### Nested List of Resource and AWS List of Structure

=== "Terraform Plugin Framework (Preferred)"
    To read:

    ```go
    func expandStructure(ctx context.Context, tfList []structureData) (*service.Structure, diag.Diagnostics) {
        // ...

        var nested []nestedAttributeNameData
        diags.Append(tfObj.NestedAttributeName.ElementsAs(ctx, &nested, false)...)

        // expand will handle null when appropriate
        apiObject.NestedAttributeName = expandNestedAttributeName(nested)

        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(ctx context.Context, apiObject *service.Structure) (types.List, diag.Diagnostics) {
        // ...
    
        // flatten will handle setting null when appropriate
        obj["nested_attribute_name"] = flattenNestedAttributeName(ctx, v)
    
        // ...
    }
    ```

=== "Terraform Plugin SDK V2"
    To read:

    ```go
    func expandStructure(tfMap map[string]interface{}) *service.Structure {
        // ...
    
        if v, ok := tfMap["nested_attribute_name"].([]interface{}); ok && len(v) > 0 {
            apiObject.NestedAttributeName = expandStructures(v)
        }
    
        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(apiObject *service.Structure) map[string]interface{} {
        // ...
    
        if v := apiObject.NestedAttributeName; v != nil {
            tfMap["nested_attribute_name"] = flattenNestedStructures(v)
        }
    
        // ...
    }
    ```

### Nested List of Resource and AWS Structure

=== "Terraform Plugin Framework (Preferred)"
    To read:

    ```go
    func expandStructure(ctx context.Context, tfList []structureData) (*service.Structure, diag.Diagnostics) {
        // ...

        var nested []nestedAttributeNameData
        diags.Append(tfObj.NestedAttributeName.ElementsAs(ctx, &nested, false)...)

        // expand will handle null when appropriate
        apiObject.NestedAttributeName = expandNestedAttributeName(nested)

        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(ctx context.Context, apiObject *service.Structure) (types.List, diag.Diagnostics) {
        // ...
    
        // flatten will handle setting null when appropriate
        obj["nested_attribute_name"] = flattenNestedAttributeName(ctx, v)
    
        // ...
    }
    ```

=== "Terraform Plugin SDK V2"
    To read:

    ```go
    func expandStructure(tfMap map[string]interface{}) *service.Structure {
        // ...
    
        if v, ok := tfMap["nested_attribute_name"].([]interface{}); ok && len(v) > 0 && v[0] != nil {
            apiObject.NestedAttributeName = expandStructure(v[0].(map[string]interface{}))
        }
    
        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(apiObject *service.Structure) map[string]interface{} {
        // ...
    
        if v := apiObject.NestedAttributeName; v != nil {
            tfMap["nested_attribute_name"] = []interface{}{flattenNestedStructure(v)}
        }
    
        // ...
    }
    ```

### Nested List of TypeString and AWS List of String

=== "Terraform Plugin Framework (Preferred)"
    To read:

    ```go
    func expandStructure(ctx context.Context, tfList []structureData) (*service.Structure, diag.Diagnostics) {
        // ...

        if !tfObj.NestedAttributeName.IsUnknown() && !tfObj.NestedAttributeName.IsNull() {
            apiObject.NestedAttributeName = flex.ExpandFrameworkStringList(ctx, tfObj.NestedAttributeName)
        }

        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(ctx context.Context, apiObject *service.Structure) (types.List, diag.Diagnostics) {
        // ...
    
        // flex will handle setting null when appropriate
        obj["nested_attribute_name"] = flex.FlattenFrameworkStringList(ctx, v)
    
        // ...
    }
    ```

=== "Terraform Plugin SDK V2"
    To read:

    ```go
    func expandStructure(tfMap map[string]interface{}) *service.Structure {
        // ...
    
        if v, ok := tfMap["nested_attribute_name"].([]interface{}); ok && len(v) > 0 {
            apiObject.NestedAttributeName = flex.ExpandStringList(v)
        }
    
        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(apiObject *service.Structure) map[string]interface{} {
        // ...
    
        if v := apiObject.NestedAttributeName; v != nil {
            tfMap["nested_attribute_name"] = aws.StringValueSlice(v)
        }
    
        // ...
    }
    ```

### Nested Map of String and AWS Map of String

=== "Terraform Plugin Framework (Preferred)"
    To read:

    ```go
    func expandStructure(ctx context.Context, tfList []structureData) (*service.Structure, diag.Diagnostics) {
        // ...

        if !tfObj.NestedAttributeName.IsUnknown() && !tfObj.NestedAttributeName.IsNull() {
            apiObject.NestedAttributeName = flex.ExpandFrameworkStringMap(ctx, tfObj.NestedAttributeName)
        }

        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(ctx context.Context, apiObject *service.Structure) (types.List, diag.Diagnostics) {
        // ...
    
        // flex will handle setting null when appropriate
        obj["nested_attribute_name"] = flex.FlattenFrameworkStringMap(ctx, v)
    
        // ...
    }
    ```

=== "Terraform Plugin SDK V2"
    To read:

    ```go
    input := service.ExampleOperationInput{}
    
    if v, ok := tfMap["nested_attribute_name"].(map[string]interface{}); ok && len(v) > 0 {
        apiObject.NestedAttributeName = flex.ExpandStringMap(v)
    }
    ```

    To write:

    ```go
    func flattenStructure(apiObject *service.Structure) map[string]interface{} {
        // ...
    
        if v := apiObject.NestedAttributeName; v != nil {
            tfMap["nested_attribute_name"] = aws.StringValueMap(v)
        }
    
        // ...
    }
    ```

### Nested Set of Resource and AWS List of Structure

=== "Terraform Plugin Framework (Preferred)"
    To read:

    ```go
    func expandStructure(ctx context.Context, tfList []structureData) (*service.Structure, diag.Diagnostics) {
        // ...

        var nested []nestedAttributeNameData
        diags.Append(tfObj.NestedAttributeName.ElementsAs(ctx, &nested, false)...)

        // expand will handle null when appropriate
        apiObject.NestedAttributeName = expandNestedAttributeName(nested)

        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(ctx context.Context, apiObject *service.Structure) (types.List, diag.Diagnostics) {
        // ...
    
        // flatten will handle setting null when appropriate
        obj["nested_attribute_name"] = flattenNestedAttributeName(ctx, v)
    
        // ...
    }
    ```

=== "Terraform Plugin SDK V2"
    To read:

    ```go
    func expandStructure(tfMap map[string]interface{}) *service.Structure {
        // ...
    
        if v, ok := tfMap["nested_attribute_name"].(*schema.Set); ok && v.Len() > 0 {
            apiObject.NestedAttributeName = expandStructures(v.List())
        }
    
        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(apiObject *service.Structure) map[string]interface{} {
        // ...
    
        if v := apiObject.NestedAttributeName; v != nil {
            tfMap["nested_attribute_name"] = flattenNestedStructures(v)
        }
    
        // ...
    }
    ```

### Nested Set of TypeString and AWS List of String

=== "Terraform Plugin Framework (Preferred)"
    To read:

    ```go
    func expandStructure(ctx context.Context, tfList []structureData) (*service.Structure, diag.Diagnostics) {
        // ...

        if !tfObj.NestedAttributeName.IsUnknown() && !tfObj.NestedAttributeName.IsNull() {
            apiObject.NestedAttributeName = flex.ExpandFrameworkStringSet(ctx, tfObj.NestedAttributeName)
        }

        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(ctx context.Context, apiObject *service.Structure) (types.List, diag.Diagnostics) {
        // ...
    
        // flex will handle setting null when appropriate
        obj["nested_attribute_name"] = flex.FlattenFrameworkStringSet(ctx, v)
    
        // ...
    }
    ```

=== "Terraform Plugin SDK V2"
    To read:

    ```go
    func expandStructure(tfMap map[string]interface{}) *service.Structure {
        // ...
    
        if v, ok := tfMap["nested_attribute_name"].(*schema.Set); ok && v.Len() > 0 {
            apiObject.NestedAttributeName = flex.ExpandStringSet(v)
        }
    
        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(apiObject *service.Structure) map[string]interface{} {
        // ...
    
        if v := apiObject.NestedAttributeName; v != nil {
            tfMap["nested_attribute_name"] = aws.StringValueSlice(v)
        }
    
        // ...
    }
    ```

### Nested TypeString and AWS String

=== "Terraform Plugin Framework (Preferred)"
    To read:

    ```go
    func expandStructure(tfList []structureData) *service.Structure {
        // ...

        if !tfObj.NestedAttributeName.IsUnknown() && !tfObj.NestedAttributeName.IsNull() {
            apiObject.NestedAttributeName = tfObj.NestedAttributeName.ValueStringPointer()
        }

        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(ctx context.Context, apiObject *service.Structure) (types.List, diag.Diagnostics) {
        // ...
    
        // flex will handle setting null when appropriate
        obj["nested_attribute_name"] = flex.StringToFramework(ctx, apiObject.NestedAttributeName)
    
        // ...
    }
    ```

=== "Terraform Plugin SDK V2"
    To read:

    ```go
    func expandStructure(tfMap map[string]interface{}) *service.Structure {
        // ...
    
        if v, ok := tfMap["nested_attribute_name"].(string); ok && v != "" {
            apiObject.NestedAttributeName = aws.String(v)
        }
    
        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(apiObject *service.Structure) map[string]interface{} {
        // ...
    
        if v := apiObject.NestedAttributeName; v != nil {
            tfMap["nested_attribute_name"] = aws.ToString(v)
        }
    
        // ...
    }
    ```

### Nested String and AWS Timestamp

=== "Terraform Plugin Framework (Preferred)"
    To ensure that parsing the read string value does not fail, use the [RFC3339 timetype](https://pkg.go.dev/github.com/hashicorp/terraform-plugin-framework-timetypes@v0.3.0/timetypes#RFC3339).

    To read:

    ```go
    func expandStructure(tfList []structureData) (*service.Structure, diag.Diagnostics) {
        // ...

        if !tfObj.NestedAttributeName.IsUnknown() && !tfObj.NestedAttributeName.IsNull() {
            nested := tfObj.NestedAttributeName.ValueRFC3339Time()
            diags.Append(tfObj.NestedAttributeName.ElementsAs(ctx, &nested, false)...)

            apiObject.NestedAttributeName = aws.Time(nested)
        }

        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(ctx context.Context, apiObject *service.Structure) (types.List, diag.Diagnostics) {
        // ...
    
        obj["nested_attribute_name"] = timetypes.NewRFC3339ValueMust(aws.ToTime(apiObject.NestedAttributeName).Format(time.RFC3339))

    
        // ...
    }
    ```

=== "Terraform Plugin SDK V2"
    To ensure that parsing the read string value does not fail, define `nested_attribute_name`'s `schema.Schema` with an appropriate [`ValidateFunc`](https://www.terraform.io/plugin/sdkv2/schemas/schema-behaviors#validatefunc):

    ```go
    "nested_attribute_name": {
        Type:         schema.TypeString,
        // ...
        ValidateFunc: validation.IsRFC3339Time,
    },
    ```

    To read:

    ```go
    func expandStructure(tfMap map[string]interface{}) *service.Structure {
        // ...
    
        if v, ok := tfMap["nested_attribute_name"].(string); ok && v != "" {
            v, _ := time.Parse(time.RFC3339, v)
    
            apiObject.NestedAttributeName = aws.Time(v)
        }
    
        // ...
    }
    ```

    To write:

    ```go
    func flattenStructure(apiObject *service.Structure) map[string]interface{} {
        // ...
    
        if v := apiObject.NestedAttributeName; v != nil {
            tfMap["nested_attribute_name"] = aws.ToTime(v).Format(time.RFC3339)
        }
    
        // ...
    }
    ```

## Further Guidelines

This section includes additional topics related to data design and decision making from the Terraform AWS Provider maintainers.

### Binary Values

Certain resources may need to interact with binary (non UTF-8) data while the Terraform State only supports UTF-8 data. Configurations attempting to pass binary data to an attribute will receive an error from Terraform CLI. These attributes should expect and store the value as a Base64 string while performing any necessary encoding or decoding in the resource logic.

### Destroy State Values

During resource destroy operations, _only_ previously applied Terraform State values are available to resource logic. Even if the configuration is updated in a manner where both the resource destroy is triggered (e.g., setting the resource meta-argument `count = 0`) and an attribute value is updated, the resource logic will only have the previously applied data values.

Any usage of attribute values during destroy should explicitly note in the resource documentation that the desired value must be applied into the Terraform State before any apply to destroy the resource.

### Hashed Values

Attribute values may be very lengthy or potentially contain [Sensitive Values](#sensitive-values). A potential solution might be to use a hashing algorithm, such as MD5 or SHA256, to convert the value before saving in the Terraform State to reduce its relative size or attempt to obfuscate the value. However, there are a few reasons not to do so:

- Terraform expects any planned values to match applied values. Ensuring proper handling during the various Terraform operations such as difference planning and Terraform State storage can be a burden.
- Hashed values are generally unusable in downstream attribute references. If a value is hashed, it cannot be successfully used in another resource or provider configuration that expects the real value.
- Terraform plan differences are meant to be human-readable. If a value is hashed, operators will only see the relatively unhelpful hash differences `abc123 -> def456` in plans.

Any value hashing implementation will not be accepted. An exception to this guidance is if the remote system explicitly provides a separate hash value in responses, in which a resource can provide a separate attribute with that hashed value.

### Sensitive Values

Marking an Attribute in the Terraform Plugin Framework Schema with `Sensitive` has the following real-world implications:

- All occurrences of the Attribute will have the value hidden in plan difference output. In the context of an Attribute within a Block, all Blocks will hide all values of the Attribute.
- In Terraform CLI 0.14 (with the `provider_sensitive_attrs` experiment enabled) and later, any downstream references to the value in other configurations will hide the value in plan difference output.

The value is either always hidden or not as the Terraform Plugin Framework does not currently implement conditional support for this functionality. Since Terraform Configurations have no control over the behavior, hiding values from the plan difference can incur a potentially undesirable user experience cost for operators.

Given that and especially with the improvements in Terraform CLI 0.14, the Terraform AWS Provider maintainers guiding principles for determining whether an Attribute should be marked as `Sensitive` is if an Attribute value:

- Objectively will always contain a credential, password, or other secret material. Operators can have differing opinions on what constitutes secret material and the maintainers will make best-effort determinations, if necessary consulting with the HashiCorp Security team.
- If the Attribute is within a Block, all occurrences of the Attribute value will objectively contain secret material. Some APIs (and therefore the Terraform AWS Provider resources) implement generic "setting" and "value" structures which likely will contain a mixture of secret and non-secret material. These will generally not be accepted for marking as `Sensitive`.

If you are unsatisfied with sensitive value handling, the maintainers can recommend ensuring there is a covering issue in the Terraform CLI and/or Terraform Plugin Framework projects explaining the use case. Ultimately, Terraform Plugins including the Terraform AWS Provider cannot implement their own sensitive value abilities if the upstream projects do not implement the appropriate functionality.

### Virtual Attributes

Attributes which only exist within Terraform and not the remote system are typically referred to as virtual attributes. Especially in the case of [Destroy State Values](#destroy-state-values), these attributes rely on the [Implicit State Passthrough](#implicit-state-passthrough) behavior of values in Terraform to be available in resource logic. A fictitious example of one of these may be a resource attribute such as a `skip_waiting` flag, which is used only in the resource logic to skip the typical behavior of waiting for operations to complete.

If a virtual attribute has a default value that does not match the [Zero Value Mapping](#zero-value-mapping) for the type, it is recommended to explicitly call `d.Set()` with the default value in the `schema.Resource` `Importer` `State` function, for example:

=== "Teraform Plugin Framework (Preferred)"
    <!-- markdownlint-disable no-space-in-emphasis -->
    ```go
    (r *ThingResource) ImportState(ctx context.Context, req resource.ImportStateRequest, resp *resource.ImportStateResponse) {
        // ... Other import activity

        resp.Diagnostics.Append(resp.State.SetAttribute(ctx, path.Root("skip_waiting"), true)...)
    }
    ```
    <!-- markdownlint-enable no-space-in-emphasis -->

=== "Teraform Plugin SDK V2"
    ```go
    &schema.Resource{
        // ... other fields ...
        Importer: &schema.ResourceImporter{
            State: func(d *schema.ResourceData, meta interface{}) ([]*schema.ResourceData, error) {
                d.Set("skip_waiting", true)

    			return []*schema.ResourceData{d}, nil
    		},
    	},
    }
    ```

This helps prevent an immediate plan difference after resource import unless the configuration has a non-default value.

## Glossary

Below is a listing of relevant terms and descriptions for data handling and conversion in the Terraform AWS Provider to establish common conventions throughout this documentation.
This list is not exhaustive of all concepts of Terraform Plugins, the Terraform AWS Provider, or the data handling that occurs during Terraform runs, but these should generally provide enough context about the topics discussed here.

- **AWS Go SDK**: Library that converts Go code into AWS Service API compatible operations and data types.
- **AWS Go SDK Model**: AWS Go SDK compatible format of AWS Service API Model.
- **AWS Go SDK Service**: AWS Service API Go code generated from the AWS Go SDK Model. Generated by the AWS Go SDK code.
- **AWS Service API**: Logical boundary of an AWS service by API endpoint. Some large AWS services may be marketed with many different product names under the same service API (e.g., VPC functionality is part of the EC2 API) and vice-versa where some services may be marketed with one product name but are split into multiple service APIs (e.g., Single Sign-On functionality is split into the Identity Store and SSO Admin APIs).
- **AWS Service API Model**: Declarative description of the AWS Service API operations and data types. Generated by the AWS service teams. Used to operate the API and generate API clients such as the various AWS Software Development Kits (SDKs).
- **Terraform Language** ("Configuration"): Configuration syntax interpreted by the Terraform CLI. An implementation of [HCL](https://github.com/hashicorp/hcl). [Full Documentation](https://www.terraform.io/language).
- **Terraform Plugin Protocol**: Description of Terraform Plugin operations and data types. Currently based on the Remote Procedure Call (RPC) library [`gRPC`](https://grpc.io/).
- **Terraform Plugin Go**: Low-level library that converts Go code into Terraform Plugin Protocol compatible operations and data types. Not currently implemented in the Terraform AWS Provider. [Project](https://github.com/hashicorp/terraform-plugin-go).
- **Terraform Plugin Framework**: High-level library that converts Go code into Terraform Plugin Protocol compatible operations and data types. This library replaces Plugin SDK V2. See [Terraform Plugin Development Packages](terraform-plugin-development-packages.md) for more information. [Project](https://github.com/hashicorp/terraform-plugin-framework).
- **Terraform Plugin SDK V2**: High-level library that converts Go code into Terraform Plugin Protocol compatible operations and data types. This library is replaced by Plugin Framework. See [Terraform Plugin Development Packages](terraform-plugin-development-packages.md) for more information. [Project](https://github.com/hashicorp/terraform-plugin-sdk).
- **Terraform Plugin Schema**: Declarative description of types and domain-specific behaviors for a Terraform provider, including resources and attributes. [Framework Documentation](https://developer.hashicorp.com/terraform/plugin/framework/handling-data/schemas). [SDK V2 Documentation](https://www.terraform.io/plugin/sdkv2/schemas).
- **Terraform State**: Bindings between objects in a remote system (e.g., an EC2 VPC) and a Terraform configuration (e.g., an `aws_vpc` resource configuration). [Full Documentation](https://www.terraform.io/language/state).

AWS Service API Models use specific terminology to describe data and types:

- **Enumeration**: Collection of valid values for a Shape.
- **Operation**: An API call. Includes information about input, output, and error Shapes.
- **Shape**: Type description.
    - **boolean**: Boolean value.
    - **float**: Fractional numeric value. May contain value validation such as maximum or minimum.
    - **integer**: Whole numeric value. May contain value validation such as maximum or minimum.
    - **list**: Collection that contains member Shapes. May contain value validation such as maximum or minimum keys.
    - **map**: Grouping of key Shape to value Shape. May contain value validation such as maximum or minimum keys.
    - **string**: Sequence of characters. May contain value validation such as an enumeration, regular expression pattern, maximum length, or minimum length.
    - **structure**: Object that contains member Shapes. May represent an error.
    - **timestamp**: Date and time value.

The Terraform Language uses the following terminology to describe data and types:

- **Attribute** ("Argument"): Assigns a name to a data value.
- **Block** ("Configuration Block"): Container type for Attributes or Blocks.
- **null**: Virtual value equivalent to the Attribute not being set.
- **Types**: [Full Documentation](https://www.terraform.io/language/expressions/types).
    - **any**: Virtual type representing any concrete type in type declarations.
    - **bool**: Boolean value.
    - **list** ("tuple"): Ordered collection of values.
    - **map** ("object"): Grouping of string keys to values.
    - **number**: Numeric value. Can be either whole or fractional numbers.
    - **set**: Unordered collection of values.
    - **string**: Sequence of characters.

Terraform Plugin Framework Schemas use the following terminology to describe data and types:

- **Resource Schema**: Grouping of Schema that represents a Terraform Resource.
- **Schema**: Represents an Attribute or Block. Has a Type and Behavior(s).
- **Types**: [Full Documentation](https://developer.hashicorp.com/terraform/plugin/framework/handling-data/types).
    - **Bool**: Boolean value.
    - **Float64**: Fractional numeric value.
    - **Int64**: Whole numeric value.
    - **List**: An ordered collection of values or Blocks.
    - **Map**: Grouping of key Type to value Type.
    - **Set**: Unordered collection of values or Blocks.
    - **String**: Sequence of characters value.

Terraform Plugin SDK Schemas use the following terminology to describe data and types:

- **Behaviors**: [Full Documentation](https://www.terraform.io/plugin/sdkv2/schemas/schema-behaviors).
    - **Sensitive**: Whether the value should be hidden from user interface output.
    - **StateFunc**: Conversion function between the value set by the Terraform Plugin and the value seen by Terraform Plugin SDK (and ultimately the Terraform State).
- **Element**: Underlying value type for a collection or grouping Schema.
- **Resource Data**: Data representation of a Resource Schema. Translation layer between the Schema and Go code of a Terraform Plugin. In the Terraform Plugin SDK, the `ResourceData` Go type.
- **Resource Schema**: Grouping of Schema that represents a Terraform Resource.
- **Schema**: Represents an Attribute or Block. Has a Type and Behavior(s).
- **Types**: [Full Documentation](https://www.terraform.io/plugin/sdkv2/schemas/schema-types).
    - **TypeBool**: Boolean value.
    - **TypeFloat**: Fractional numeric value.
    - **TypeInt**: Whole numeric value.
    - **TypeList**: Ordered collection of values or Blocks.
    - **TypeMap**: Grouping of key Type to value Type.
    - **TypeSet**: Unordered collection of values or Blocks.
    - **TypeString**: Sequence of characters value.

Some other terms that may be used:

- **Block Attribute** ("Child Attribute", "Nested Attribute"): Block level Attribute.
- **Expand Function**: Function that converts Terraform Plugin SDK data into the equivalent AWS Go SDK type.
- **Flatten Function**: Function that converts an AWS Go SDK type into the equivalent Terraform Plugin SDK data.
- **NullableTypeBool**: (SDK V2 Only) Workaround "schema type" created to accept a boolean value that is not configured in addition to true and false. Not implemented in the Terraform Plugin SDK, but uses `TypeString` (where `""` represents not configured) and additional validation.
- **NullableTypeFloat**: (SDK V2 Only) Workaround "schema type" created to accept a fractional numeric value that is not configured in addition to `0.0`. Not implemented in the Terraform Plugin SDK, but uses `TypeString` (where `""` represents not configured) and additional validation.
- **NullableTypeInt**: (SDK V2 Only) Workaround "schema type" created to accept a whole numeric value that is not configured in addition to `0`. Not implemented in the Terraform Plugin SDK, but uses `TypeString` (where `""` represents not configured) and additional validation.
- **Root Attribute: Resource top-level Attribute or Block.

For additional reference, the Terraform documentation also includes a [full glossary of terminology](https://www.terraform.io/docs/glossary.html).
# Debugging

This guide covers strategies we have found useful in finding runtime and logic errors in the AWS Provider. We do not cover syntax or compiler errors as these are well addressed by [Go documentation](https://go.dev/ref/spec) and IDEs, such as Visual Studio Code ("VS Code").

If you have your own debugging tricks for the provider, open a pull request to add them here!

## 1. Reproduce

One of the most crucial steps in the process of bug fixing is to reproduce the bug and create a minimal reproduction of it. In this section, we will discuss why it is so important to reproduce bugs.

**TL;DR:** for Repro

Perhaps the most important step in debugging is reproducing the bug.

### What is a bug?

Before we dive into the details, let's first define what a bug is. A bug is an error or flaw that produces an incorrect or unexpected result, or causes the AWS Provider to behave in an unintended manner. For the Provider, "bugs" generally refer to errors that happen at runtime due to logic problems or unexpected interactions with AWS.

### Why is it important to reproduce bugs?

Reproducing a bug is the process of intentionally triggering the error or unexpected behavior that occurs when the bug is present. It is important to reproduce bugs because it allows us to:

1. **Verify that the bug exists**: By reproducing the bug, we can confirm that the error or unexpected behavior is real and either _always_ happens or happens _intermittently_ and not just a one-time occurrence. This is important because if we can't reproduce the bug, we may end up wasting time trying to fix a non-existent issue.
2. **Understand the cause of the bug**: Reproducing the bug can help us understand what is causing the error or unexpected behavior. This is important because without understanding the root cause of the bug, we may end up fixing _the symptoms_ of the bug rather than the underlying problem.
3. **Test the fix:** If we know how to reproduce the bug, we also know how to verify we've fixed it.

## 2. Create a _minimal_ reproduction

**TL;DR:** A complete 10-line configuration that reproduces a bug is _far more_ (perhaps 100× more) useful than a 1000-line configuration that reproduces the same bug.

Creating a minimal reproduction of a bug is the process of isolating the bug to its simplest form. It is _very important_ to create a minimal reproduction of bugs, especially with Terraform configurations, because it allows us to:

1. **Focus on the root cause of the bug**: By eliminating any extraneous configuration or dependencies, we can focus on the specific configuration that is causing the bug. This makes it easier to understand and fix the root cause of the bug.
2. **Save time**: By creating a minimal reproduction of the bug, we can reduce the amount of time it takes to reproduce the bug and test the fix. This is because we don't have to navigate through a large configuration or deal with unnecessary dependencies. _The minimal configuration becomes the basis of a [new acceptance test](#3-create-a-new-acceptance-test) that verifies the bug is fixed (and stays fixed in the future)._
3. **Make it easier for others to reproduce the bug**: If we are working on a team, creating a minimal reproduction of the bug makes it easier for other team members to reproduce the bug and understand the root cause.

### How to create a minimal reproduction of a bug

Creating a minimal reproduction of a bug can be a time-consuming process, but it is well worth the effort. Here are some tips for creating a minimal reproduction of a bug:

1. **Start with a simple test case**: Start with a simple configuration that causes the bug.
2. **Remove any extraneous configuration**: Remove as many resources, dependencies, and arguments as possible to simplify, while still maintaining [test independence](running-and-writing-acceptance-tests.md#test-configuration-independence).
3. **Verify that the configuration still reproduces the bug**: After removing the configuration, make sure that the configuration still causes the bug. If the bug no longer occurs, you may have removed too much. In this case, add back configuration until the bug reappears.

_A minimal configuration is worth its weight in gold._ If you're only able to make it this far in the debugging process, create a new issue with your minimal configuration or add it to an existing issue. A minimal configuration is a great way to give someone else a jump start in looking at the problem.

## 3. Create A New Acceptance Test

Sometimes, we tend to immediately jump into the code without creating a test. However, [creating an acceptance test](running-and-writing-acceptance-tests.md#writing-an-acceptance-test) is something we'll need to do eventually anyway but doing it _first_ has the added benefit of allowing us to easily trigger the bug. That makes debugging easier and allows us to use debugging tools.

### Use the Minimal Configuration as the Basis for the Test

Adding a problematic minimal configuration test is just like [creating an acceptance test](running-and-writing-acceptance-tests.md#writing-an-acceptance-test) except that when we run it, it has a problem. Starting with the end in mind focuses our efforts and gives great satisfaction when the code is fixed!

#### Erroring tests example

For example, if we're looking at an error in the VPC flow log resource, this is how we might add a test with a minimal configuration to trigger the error.

```go
func TestAccVPCFlowLog_destinationError(t *testing.T) {
	ctx := acctest.Context(t)
	rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)

	resource.ParallelTest(t, resource.TestCase{
		PreCheck:                 func() { acctest.PreCheck(ctx, t) },
		ErrorCheck:               acctest.ErrorCheck(t, names.EC2ServiceID),
		ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
		CheckDestroy:             testAccCheckFlowLogDestroy(ctx),
		Steps: []resource.TestStep{
			{
				Config:      testAccVPCFlowLogConfig_destinationError(rName),
			},
		},
	})
}

// ...

func testAccVPCFlowLogConfig_destinationError(rName string) string {
	return fmt.Sprintf(`
resource "aws_flow_log" "test" {
  # minimal configuration causing a bug
}
`, rName)
}
```

If we were to [run the test](running-and-writing-acceptance-tests.md#running-an-acceptance-test) on the command line, this is how the erroring output might look:

```console
make testacc TESTS=TestAccVPCFlowLog_destinationError PKG=vpc
```

```
==> Checking that code complies with gofmt requirements...
TF_ACC=1 go test ./internal/service/ec2/... -v -count 1 -parallel 20 -run='TestAccVPCFlowLog_destinationError'  -timeout 180m
=== RUN   TestAccVPCFlowLog_destinationError
=== PAUSE TestAccVPCFlowLog_destinationError
=== CONT  TestAccVPCFlowLog_destinationError
    vpc_flow_log_test.go:297: Step 1/1 error: Error running apply: exit status 1
        
        Error: creating Flow Log (vpc-0c2635533cef2be79): 1 error occurred:
        	* vpc-0c2635533cef2be79: 400: Access Denied for LogDestination: does-not-exist. Please check LogDestination permission

          with aws_flow_log.test,
          on terraform_plugin_test.tf line 34, in resource "aws_flow_log" "test":
          34: resource "aws_flow_log" "test" {
        
--- FAIL: TestAccVPCFlowLog_destinationError (13.79s)
FAIL
FAIL	github.com/hashicorp/terraform-provider-aws/internal/service/ec2	15.373s
FAIL
make: *** [testacc] Error 1
```

#### Wrong results example

Of course, not all bugs throw errors. For example, perhaps the bug you are looking at involves a wrong value in the `log_group_name` attribute. This is an example of adding a test that will error because the value is wrong.

```go
func TestAccVPCFlowLog_destinationError(t *testing.T) {
	ctx := acctest.Context(t)
	rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)

	resource.ParallelTest(t, resource.TestCase{
		PreCheck:                 func() { acctest.PreCheck(ctx, t) },
		ErrorCheck:               acctest.ErrorCheck(t, names.EC2ServiceID),
		ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
		CheckDestroy:             testAccCheckFlowLogDestroy(ctx),
		Steps: []resource.TestStep{
			{
				Config:      testAccVPCFlowLogConfig_destinationError(rName),
                Check: resource.ComposeTestCheckFunc(
					testAccCheckFlowLogExists(ctx, resourceName, &flowLog),
					resource.TestCheckResourceAttr(resourceName, "log_group_name", ""), // this should not be empty
				),
			},
		},
	})
}

// ...

func testAccVPCFlowLogConfig_destinationError(rName string) string {
	return fmt.Sprintf(`
resource "aws_flow_log" "test" {
  # minimal configuration causing a bug
}
`, rName)
}
```

If we were to [run the test](running-and-writing-acceptance-tests.md#running-an-acceptance-test) on the command line, this is how the erroring output might look:

```console
make testacc TESTS=TestAccVPCFlowLog_LogDestinationType_s3 PKG=vpc
```

```
==> Checking that code complies with gofmt requirements...
TF_ACC=1 go test ./internal/service/ec2/... -v -count 1 -parallel 20 -run='TestAccVPCFlowLog_LogDestinationType_s3'  -timeout 180m
=== RUN   TestAccVPCFlowLog_LogDestinationType_s3
=== PAUSE TestAccVPCFlowLog_LogDestinationType_s3
=== CONT  TestAccVPCFlowLog_LogDestinationType_s3
    vpc_flow_log_test.go:269: Step 1/2 error: Check failed: Check 3/4 error: aws_flow_log.test: Attribute 'log_group_name' expected "abc-123", got ""
--- FAIL: TestAccVPCFlowLog_LogDestinationType_s3 (15.49s)
FAIL
FAIL	github.com/hashicorp/terraform-provider-aws/internal/service/ec2	17.358s
FAIL
make: *** [testacc] Error 1
```

### Take Stock

It may seem like we haven't accomplished much of anything at this point. However, we have! We've:

1. Reproduced the error
2. Created a minimal reproduction
3. Created a test to trigger the error

This will make the rest of debugging a lot more straightforward.

### Contributing a Failing Test

If you aren't able to figure out a bug or delving into code is not your thing, open a pull request to [contribute just the test](running-and-writing-acceptance-tests.md#writing-an-acceptance-test) that highlights the bug. This is a valuable starting point for future work!

We ask that you make the test "PASS," but use code comments and a GitHub issue to explain what is wrong. With nearly 7,000 acceptance tests, there is always a certain percentage that inexplicably fails. Since we know that the new test we're adding highlights a known bug, we don't want the failure to be lost in the tally of inexplicable failures.

#### Failing Test Contribution Example: Errors

For example, if you want to contribute just a failing test, the example below shows how to use `ExpectError` and a code comment to reference an open GitHub issue addressing the bug. Here we're using `ExpectError` to allow the test to "pass," even though it should not. When the next person comes along to debug, they can simply remove `ExpectError`.

```go
func TestAccVPCFlowLog_destinationError(t *testing.T) {
	ctx := acctest.Context(t)
	rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)

	resource.ParallelTest(t, resource.TestCase{
		PreCheck:                 func() { acctest.PreCheck(ctx, t) },
		ErrorCheck:               acctest.ErrorCheck(t, names.EC2ServiceID),
		ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
		CheckDestroy:             testAccCheckFlowLogDestroy(ctx),
		Steps: []resource.TestStep{
			{
				Config:      testAccVPCFlowLogConfig_destinationError(rName),
                // This error should not happen!
                // See https://github.com/hashicorp/terraform-provider-aws/issues/45912
				ExpectError: regexache.MustCompile(`invalid destination`),
			},
		},
	})
}

// ...

func testAccVPCFlowLogConfig_destinationError(rName string) string {
	return fmt.Sprintf(`
resource "aws_flow_log" "test" {
  # minimal configuration causing a bug
}
`, rName)
}
```

#### Failing Test Contribution Example: Wrong Results

There are other types of bugs besides the error thrown in the previous example. For example, with a wrong results test, you would have `resource.TestCheckResourceAttr()` highlighting what is wrong, along with a link to the GitHub issue to explain why the attribute value is wrong.

```go
func TestAccVPCFlowLog_destinationError(t *testing.T) {
	ctx := acctest.Context(t)
	rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)

	resource.ParallelTest(t, resource.TestCase{
		PreCheck:                 func() { acctest.PreCheck(ctx, t) },
		ErrorCheck:               acctest.ErrorCheck(t, names.EC2ServiceID),
		ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
		CheckDestroy:             testAccCheckFlowLogDestroy(ctx),
		Steps: []resource.TestStep{
			{
				Config:      testAccVPCFlowLogConfig_destinationError(rName),
				Check: resource.ComposeTestCheckFunc(
					testAccCheckFlowLogExists(ctx, resourceName, &flowLog),
                     // log_group_name should be "xyz-123"
                     // See https://github.com/hashicorp/terraform-provider-aws/issues/45912
					resource.TestCheckResourceAttr(resourceName, "log_group_name", ""),
				),
			},
		},
	})
}

// ...

func testAccVPCFlowLogConfig_destinationError(rName string) string {
	return fmt.Sprintf(`
resource "aws_flow_log" "test" {
  # minimal configuration causing a bug
}
`, rName)
}
```

## 4. Find Out Why a Bug Happens

Now that we can easily reproduce a bug with a test and we have a minimal configuration, we can look more closely at why the bug is happening.

There are several approaches to looking at what is happening in the AWS provider. You might find that some bugs lend themselves to one approach while others are more easily evaluated with another. Also, you might start with one approach and then find you need to move to another, _e.g._, starting by adding a few `fmt.Printf()` statements and then move to an IDE debugger.

### Use `fmt.Printf()`

One quick and dirty approach that works for simple bugs is to have Go output information to the console (_i.e._, terminal). This approach is especially helpful if you've reviewed the code, found an error, and have a strong suspicion about what is going on. You can use `fmt.Printf()` to confirm what you think is happening.

The approach is also helpful to see if the code reaches a certain point or for seeing the value of a variable or two.

This approach does not work well for complex logic, examining many lines of code, or for looking at many different variables. Use more advanced debugging, as described below, for these situations.

This example shows using `fmt.Printf()` to output information to the console:

```go
func resourceLogFlowCreate(ctx context.Context, d *schema.ResourceData, meta interface{}) diag.Diagnostics {
    // other code ...

	outputRaw, err := tfresource.RetryWhenAWSErrMessageContains(ctx, propagationTimeout, func() (interface{}, error) {
		return conn.CreateFlowLogsWithContext(ctx, input)
	}, errCodeInvalidParameter, "Unable to assume given IAM role")

    fmt.Printf("reached point %d, with input: %+v\n", 3, input)

	if err == nil && outputRaw != nil {
        fmt.Printf("reached point %d, with output: %+v\n", 4, outputRaw)
		err = UnsuccessfulItemsError(outputRaw.(*ec2.CreateFlowLogsOutput).Unsuccessful)
	}

    // other code ...
}
```

[Running the test](running-and-writing-acceptance-tests.md#running-an-acceptance-test) from the command line, we might see the following output:

```console
make testacc TESTS=TestAccVPCFlowLog_LogDestinationType_s3 PKG=vpc
```

```
==> Checking that code complies with gofmt requirements...
TF_ACC=1 go test ./internal/service/ec2/... -v -count 1 -parallel 20 -run='TestAccVPCFlowLog_LogDestinationType_s3'  -timeout 180m
=== RUN   TestAccVPCFlowLog_LogDestinationType_s3
=== PAUSE TestAccVPCFlowLog_LogDestinationType_s3
=== CONT  TestAccVPCFlowLog_LogDestinationType_s3
reached point 3, with input: {
  ClientToken: "terraform-20230403170214312900000001",
  LogDestination: "arn:aws:s3:::tf-acc-test-4802362269206133111",
  LogDestinationType: "s3",
  MaxAggregationInterval: 600,
  ResourceIds: ["vpc-093265898e824c24e"],
  ResourceType: "VPC",
  TagSpecifications: [{
      ResourceType: "vpc-flow-log",
      Tags: [{
          Key: "Name",
          Value: "tf-acc-test-4802362269206133111"
        }]
    }],
  TrafficType: "ALL"
}
reached point 4, with output: {
  ClientToken: "terraform-20230403170214312900000001",
  FlowLogIds: ["fl-09861862b9f8bb3a3"]
}
--- PASS: TestAccVPCFlowLog_LogDestinationType_s3 (26.45s)
```

### Use Visual Studio Code Debugging

Using debugging from within VS Code provides extra benefits but also an extra challenge. The extra benefits include the ability to set breakpoints, step over and into code, and see the values of variables. The extra challenge is getting your debug environment properly set up to include access to your AWS credentials and environment variables used for testing.

Special thanks to Drew Mullen for [his work on debugging the AWS provider in VS Code](https://dev.to/drewmullen/vscode-terraform-provider-development-setup-debugging-6bn).

#### Set up `launch.json`

VS Code uses a hidden directory called `.vscode` in the root of your project for configuration files. This directory and the files it contains are ignored by Git using the `.gitignore` file included with the AWS provider. This allows you to have your own local configuration without concerns that it will be uploaded to or overwritten by the AWS provider repository.

As shown below, use VS Code to create two files in the `.vscode` directory: `launch.json` and `private.env`.

![Using launch.json in VS Code](images/launch-json.png "Using launch.json in VS Code")

In `launch.json`, add this configuration:

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Debug Selected Test",
      "request": "launch",
      "type": "go",
      "args": [
        "-test.v",
        "-test.run",
        "^${selectedText}$"
      ],
      "mode": "auto",
      "program": "${fileDirname}",
      "env": {"PKG_NAME": "${relativeFileDirname}"},
      "envFile": "${workspaceFolder}/.vscode/private.env",
      "showLog": true
    }
  ]
}
```

In `private.env`, add environment variables to represent your AWS provider testing configuration, including replacing `aws_provider_profile` and `aws_alternate_profile` below with the names of profiles defined in your `~/.aws/config` file:

```env
TF_ACC=1
TF_LOG=info
GOFLAGS='-mod=readonly'
AWS_PROFILE=aws_provider_profile
AWS_DEFAULT_REGION=us-west-2
AWS_ALTERNATE_PROFILE=aws_alternate_profile
AWS_ALTERNATE_REGION=us-east-1
AWS_THIRD_REGION=us-east-2
ACM_CERTIFICATE_ROOT_DOMAIN=terraform-provider-aws-acctest-acm.com
```

Note that you _can_ set `TF_LOG` to `debug` but, if you do, you can receive thousands of lines of additional information that can make it difficult to find useful information.

#### Viewing Run and Debug

Open the Run and Debug panel in VS Code by pressing `Shift-⌘-D` or by clicking on the debug button icon:

![Debug Button](images/debug-button.png "Debug Button")

To debug, you'll also want to open the debug console by pressing `Shift-⌘-Y` or selecting "Debug Console" from the View top menu.

#### Run and Debug

With the environment and VS Code GUI set up, you are ready to run and debug.

1. As shown below, select the name of a test function from a `*_test.go` file by double-clicking on the name or click-dragging over the name to highlight the entire name. (Do not include the `func` at the beginning or `(t *testing.T) {` at the end.)
2. Make sure that "Debug Selected Test" is shown next to the debug play button.
3. Click on the play button in the Run and Debug panel. Depending on your configuration, there may also be a "Debug Selected Test" option at the bottom of the VS Code window. Clicking on that is equivalent to clicking the play button in the Run and Debug panel.

![Debug GUI](images/debug-gui.png "Debug GUI")

#### Breakpoints

Depending on where you suspect the problems are occurring, you can set breakpoints on the resource's Create, Read, Update, Delete, or other functions. The debugger will stop at the first breakpoint it encounters.

Setting breakpoints is built into VS Code and is easy. Hover to the left of a line number and you'll see a faded red dot. Click on the faded red dot to turn it into a breakpoint, as shown below.

You can see a list of breakpoints throughout the codebase at the bottom of the Run and Debug panel, as shown below.

![Breakpoints](images/breakpoints.png "Breakpoints")

#### Stepping Out

Once the debugger has stopped at a breakpoint, you can control how it continues from there. VS Code will display the debugger controls, which you can reposition using the grip (_i.e._, six dots), at the left of the controls.

![Debug Controls](images/debug-controls.png "Debug Controls")

From left to right, the controls are as follows:

1. Pause (_i.e._, two vertical lines) pauses execution wherever it happens to be when you click pause
2. Step over (_i.e._, dot with a curved arrow above it) goes to the next statement but will not follow execution inside functions
3. Step into (_i.e._, dot with an arrow pointing down) goes to the next statement, following execution inside functions
4. Step out (_i.e._, dot with an arrow pointing up) goes to the next statement in the calling function skipping the rest of the execution in the current function
5. Restart (_i.e._, the circular arrow) stops the current run and starts at the beginning again
6. Stop (_i.e._, the square) stops the current run

### Use Delve

Behind the scenes, VS Code and other IDEs use Delve to debug. You can also use Delve without an IDE if you prefer to work on the command line.

Here are some resources to get you started using Delve:

* [Delve on GitHub](https://github.com/go-delve/delve)
* [Golang Debugging With Delve (Step-by-Step)](https://golang.cafe/blog/golang-debugging-with-delve.html)
* [Using the Go Delve Debugger from the command line](https://www.jamessturtevant.com/posts/Using-the-Go-Delve-Debugger-from-the-command-line/)
* [Stop debugging Go with Println and use Delve instead](https://opensource.com/article/20/6/debug-go-delve)

## 5. Verify the Fix with a Test

Verify that bugs are fixed with one or more tests. The tests used to help debug, described above, verify that the bug is fixed after debugging. In addition, the tests ensure that future changes don't undo the fix.
# Dependency Updates

Generally, dependency updates are handled by maintainers.

## Go Default Version Update

This project typically upgrades its Go version for development and testing shortly after release to get the latest and greatest Go functionality. Before beginning the update process, ensure that you review the new version release notes to look for any areas of possible friction when updating.

Create an issue to cover the update noting down any areas of particular interest or friction.

Ensure that the following steps are tracked within the issue and completed within the resulting pull request.

- Update go version in `go.mod`
- Verify `make test lint` works as expected
- Verify `goreleaser build --snapshot` succeeds for all currently supported architectures
- Verify `goenv` support for the new version
- Update `docs/development-environment.md`
- Update `.go-version`
- Update `CHANGELOG.md` detailing the update and mention any notes practitioners need to be aware of.

See [#9992](https://github.com/hashicorp/terraform-provider-aws/issues/9992) / [#10206](https://github.com/hashicorp/terraform-provider-aws/pull/10206)  for a recent example.

## AWS Go SDK Updates

Almost exclusively, `github.com/aws/aws-sdk-go` and `github.com/aws/aws-sdk-go-v2` updates are additive in nature. It is generally safe to only scan through them before approving and merging. If you have any concerns about any of the service client updates such as suspicious code removals in the update, or deprecations introduced, run the acceptance testing for potentially affected resources before merging.

### Authentication changes

Occasionally, there will be changes listed in the authentication pieces of the AWS Go SDK codebase, e.g., changes to `aws/session`. The AWS Go SDK `CHANGELOG` should include a relevant description of these changes under a heading such as `SDK Enhancements` or `SDK Bug Fixes`. If they seem worthy of a callout in the Terraform AWS Provider `CHANGELOG`, then upon merging we should include a similar message prefixed with the `provider` subsystem, e.g., `* provider: ...`.

Additionally, if a `CHANGELOG` addition seemed appropriate, this dependency and version should also be updated in the Terraform S3 Backend, which currently lives in Terraform Core. An example of this can be found at https://github.com/hashicorp/terraform-provider-aws/pull/9305 and https://github.com/hashicorp/terraform/pull/22055.

### CloudFront changes

CloudFront service client updates have previously caused an issue when a new field introduced in the SDK was not included with Terraform and caused all requests to error (https://github.com/hashicorp/terraform-provider-aws/issues/4091). As a precaution, if you see CloudFront updates, run all the CloudFront resource acceptance testing before merging (`TestAccCloudFront`).

## golangci-lint Updates

Merge if CI passes.

## Terraform Plugin Development Package Updates (SDK V2 or Framework)

Except for trivial changes, run the full acceptance testing suite against the pull request and verify there are no new or unexpected failures.

## tfproviderdocs Updates

Merge if CI passes.

## tfproviderlint Updates

Merge if CI passes.

## yaml.v2 Updates

Run the acceptance testing pattern, `TestAccCloudFormationStack(_dataSource)?_yaml`, and merge if passing.
# Design Decision Log

This serves as an index over the various decisions we make as a maintainer team over what is considered best practice, and
what we should encourage/require as a design standard. These are not necessarily fixed, and are likely to evolve and be
replaced as new decisions are made. This is an evolution of an internal process and will pivot to take place in public
as much as possible to allow for external feedback from the community and core contributors.

| Decision                                                                                                 | Description                                                                                                                     | Issue Link                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Relationship Resource Design Standards](./design-decisions/relationship-resource-design-standards.md)   | Align on design standards for relationship management resources in the Terraform AWS Provider.                                  | [#9901](https://github.com/hashicorp/terraform-provider-aws/issues/9901)   |
| [SecretsManager Secret Target Attachment](./design-decisions/secretsmanager-secret-target-attachment.md) | Assess the feasibility of replicating the `AWS::SecretsManager::SecretTargetAttachment` CloudFormation function with Terraform. | [#9183](https://github.com/hashicorp/terraform-provider-aws/issues/9183)   |
| [RDS Blue Green Deployments](./design-decisions/rds-bluegreen-deployments.md)                            | Assess the feasibility extending blue green deployment functionality found in `aws_rds_instance` to `aws_rds_cluster`.          | [#28956](https://github.com/hashicorp/terraform-provider-aws/issues/28956) |
| [Exclusive Relationship Management Resources](./design-decisions/exclusive-relationship-management-resources.md)| A proposal describing the use case for "exclusive relationship management" resources and their function within the Terraform AWS provider.                                 | [#39203](https://github.com/hashicorp/terraform-provider-aws/pull/39203)   |
# Development Environment Setup

## Requirements

- [Terraform](https://www.terraform.io/downloads.html) 0.12.26+ (to run acceptance tests)
- [Go](https://golang.org/doc/install) 1.23+ (to build the provider plugin)
- Mac, Linux or WSL (to build the provider plugin)

## Quick Start

If you wish to work on the provider, you'll first need [Go](http://www.golang.org) installed on your machine (please check the [requirements](#requirements) before proceeding).

!!! note
    This project uses [Go Modules](https://blog.golang.org/using-go-modules) making it safe to work with it outside of your existing [GOPATH](http://golang.org/doc/code.html#GOPATH). The instructions that follow assume a directory in your home directory outside of the standard GOPATH (i.e `$HOME/development/hashicorp/`).

Begin by creating a new development directory and cloning the repository.

```console
mkdir -p $HOME/development/hashicorp/; cd $HOME/development/hashicorp/
```

```console
 git clone git@github.com:hashicorp/terraform-provider-aws
```

Enter the provider directory and run `make tools`. This will install the tools for provider development.

```console
make tools
```

### Building the Provider

To compile the provider, run `make build`.

```console
make build
```

This will build the provider and put the provider binary in the `$GOPATH/bin` directory.

```console
ls -la $GOPATH/bin/terraform-provider-aws
```

### Testing the Provider

In order to test the provider, you can run `make test`.

!!! tip
    Make sure no `AWS_ACCESS_KEY_ID` or `AWS_SECRET_ACCESS_KEY` variables are set, and there's no `[default]` section in the AWS credentials file `~/.aws/credentials`.

```console
make test
```

In order to run the full suite of acceptance tests, run `make testacc`.

!!! warning
    Acceptance tests create real resources, and often cost money to run. Please read [Running and Writing Acceptance Tests](running-and-writing-acceptance-tests.md) before running these tests.

```console
make testacc
```

### Using the Provider

With Terraform v0.14 and later, [development overrides for provider developers](https://www.terraform.io/cli/config/config-file#development-overrides-for-provider-developers) can be leveraged in order to use the provider built from source.

To do this, populate a Terraform CLI configuration file (`~/.terraformrc` for all platforms other than Windows; `terraform.rc` in the `%APPDATA%` directory when using Windows) with at least the following options:

```terraform
provider_installation {
  dev_overrides {
    "hashicorp/aws" = "[REPLACE WITH GOPATH]/bin"
  }
  direct {}
}
```
# End User Documentation Changes

All practitioner-focused documentation is found in the `/website` folder of the repository.

```
├── website/docs
    ├── r/                     # Documentation for resources
    ├── d/                     # Documentation for data sources
    ├── guides/                # Long format guides for provider level configuration or provider upgrades.
    ├── cdktf/                 # Documentation for CDKTF generated in other programming languages
    └── index.html.markdown    # Home page and all provider level documentation.
└── examples/                  # Large example configurations
```

!!!note
    The CDKTF documentation is generated based on resource and data source documentation. Files in the `cdktf/` folder should not be edited directly.

For any documentation change please raise a pull request including and adhering to the following:

- __Reasoning for Change__: Documentation updates should include an explanation for why the update is needed. If the change is a correction that aligns with AWS behavior, please include a link to the AWS Documentation in the PR.
- __Prefer AWS Documentation__: Documentation about AWS service features and valid argument values that are likely to update over time should link to AWS service user guides and API references where possible.
- __Large Example Configurations__: Example Terraform configuration that includes multiple resource definitions should be added to the repository `examples` directory instead of an individual resource documentation page. Each directory under `examples` should be self-contained to call `terraform apply` without special configuration.
- __Avoid Terraform Configuration Language Features__: Individual resource documentation pages and examples should refrain from highlighting particular Terraform configuration language syntax workarounds or features such as `variable`, `local`, `count`, and built-in functions.
<!-- markdownlint-configure-file { "code-block-style": false } -->
# Error Handling

The Terraform AWS Provider codebase bridges the implementation of a [Terraform Plugin](https://www.terraform.io/plugin/how-terraform-works) and an AWS API client to support AWS operations as Terraform Resources.
An important aspect of performing remote actions is properly handling operations which are not guaranteed to succeed.
Some common examples include unstable network connections, missing permissions, incorrect Terraform configurations, or unexpected responses from the remote system.
All of these situations lead to an unexpected workflow action that must be surfaced to Terraform for operators to troubleshoot.
This guide is intended to document best practices for surfacing these issues properly.

For further details about how the AWS SDK for Go and the Terraform AWS Provider handle retryable errors, see the [Retries and Waiters documentation](retries-and-waiters.md).

## General Guidelines and Helpers

### Naming and Check Style

Following typical Go conventions, error variables in the Terraform AWS Provider codebase should be named `err`, e.g.

```go
result, err := strconv.Itoa("oh no!")
```

The code that then checks these errors should prefer `if` conditionals that usually `return` (or in the case of looping constructs, `break`/`continue`) early, especially in the case of multiple error checks, e.g.

```go
if /* ... something checking err first ... */ {
    // ... return, break, continue, etc. ...
}

if err != nil {
    // ... return, break, continue, etc. ...
}

// all good!
```

This is in preference to some other styles of error checking, such as `switch` conditionals without a condition.

### Wrap Errors

Go implements error wrapping, which means that a deeply nested function call can return a particular error type, while each function up the stack can provide additional error message context without losing the ability to determine the original error.
Additional information about this concept can be found in the [Go blog entry titled Working with Errors in Go 1.13](https://blog.golang.org/go1.13-errors).

For most use cases in this codebase, this means if code is receiving an error and needs to return it, it should implement [`fmt.Errorf()`](https://pkg.go.dev/fmt#Errorf) and the `%w` verb, e.g.

```go
return fmt.Errorf("adding some additional message: %w", err)
```

This type of error wrapping should be applied to all Terraform resource logic where errors (not diagnostics) are returned.

### AWS SDK for Go Errors

The [AWS SDK for Go v2 documentation](https://aws.github.io/aws-sdk-go-v2/docs/) includes a [section on handling errors](https://aws.github.io/aws-sdk-go-v2/docs/handling-errors/), which is recommended reading.

For the purposes of this documentation, the most important concepts in handling these errors are:

- The SDK wraps all errors returned by service clients with the [`smithy.OperationError`](https://pkg.go.dev/github.com/aws/smithy-go/#OperationError) type.
- [`errors.As`](https://golang.org/pkg/errors#As) should be used to unwrap errors when inspecting for a specific error type (e.g, a `BucketAlreadyExists` error from the S3 API).

#### AWS SDK for Go Error Helpers

To simplify operations with AWS SDK for Go error types, the following helpers are available via the `github.com/hashicorp/aws-sdk-go-base/v2/tfawserr` Go package:

- `tfawserr.ErrCodeEquals` - Preferred when the error code is specific enough for the check condition. For example, a `ResourceNotFoundError` code provides enough information that the requested resource does not exist.
- `tfawserr.ErrMessageContains`: Preferred when an error code can cover multiple failure modes, and additional parsing of the error message is required to determine if it matches a specific condition.

The recommendation for error message checking is to be just specific enough to capture the anticipated issue, but not include _too_ much matching as the AWS API can change over time without notice.
The maintainers have observed changes in wording and capitalization cause unexpected issues in the past.

For example, given this error code and message:

```
InvalidParameterValueException: IAM Role arn:aws:iam::123456789012:role/XXX cannot be assumed by AWS Backup
```

An error check for this might be:

```go
if tfawserr.ErrMessageContains(err, backup.ErrCodeInvalidParameterValueException, "cannot be assumed") {
    // Special handling here
}
```

The Amazon Resource Name in the error message will be different for every environment and does not add value to the check.
The AWS Backup suffix is also extraneous and could change should the service ever rename.

#### AWS SDK for Go Error Constants

Each AWS SDK for Go v2 service API typically implements common error codes, which get exported as public structs in the SDK. In the [AWS SDK for Go v2 API Reference](https://pkg.go.dev/github.com/aws/aws-sdk-go-v2), these can be found in each of the service packages `types` subpackage (typically named `{ErrorType}Exception`).

If an AWS SDK for Go service API is missing an error code constant, an AWS Support case should be submitted and a new constant can be added to `internal/service/{SERVICE}/errors.go` file (created if not present), e.g.

```go
const(
    ErrCodeInvalidParameterException = "InvalidParameterException"
)
```

Then referencing code can use it via:

```go
// imports
tf{SERVICE} "github.com/hashicorp/terraform-provider-aws/internal/service/{SERVICE}"

// logic
tfawserr.ErrCodeEquals(err, tf{SERVICE}.ErrCodeInvalidParameterException)
```

### Terraform Plugin Types and Helpers

The Terraform Plugin SDK includes some error types which are used in certain operations and typically preferred over implementing new types:

* [`retry.NotFoundError`](https://pkg.go.dev/github.com/hashicorp/terraform-plugin-sdk/v2/helper/retry#NotFoundError)
* [`retry.TimeoutError`](https://pkg.go.dev/github.com/hashicorp/terraform-plugin-sdk/v2/helper/retry#TimeoutError)
    * Returned from [`retry.RetryContext()`](https://pkg.go.dev/github.com/hashicorp/terraform-plugin-sdk/v2/helper/retry#RetryContext) and
    [`(retry.StateChangeConf).WaitForStateContext()`](https://pkg.go.dev/github.com/hashicorp/terraform-plugin-sdk/v2/helper/retry#StateChangeConf.WaitForStateContext)

!!! note
    While these helpers currently reside in the Terraform Plugin SDK V2 package, they can be used with Plugin Framework based resources. In the future these functions will likely be migrated into the provider itself, or a standalone library as there is no direct dependency on Plugin SDK functionality.

The Terraform AWS Provider codebase implements some additional helpers for working with these in the `internal/tfresource` package:

- `tfresource.NotFound(err)`: Returns true if the error is a `retry.NotFoundError`.
- `tfresource.TimedOut(err)`: Returns true if the error is a `retry.TimeoutError` and contains no `LastError`. This typically signifies that the retry logic was never signaled for a retry, which can happen when AWS API operations are automatically retrying before returning.

## Resource Lifecycle Guidelines

Terraform CLI and the Terraform Plugin libraries have certain expectations and automatic behaviors depending on the lifecycle operation of a resource.
This section highlights some common issues that can occur and their expected resolution.

### Resource Creation

For Terraform Plugin Framework based resources, creation is implemented on the `Create` method of the resource struct.
For Terraform Plugin SDK V2 based resources, creation is implemented on the `CreateWithoutTimeout` function of the resource schema definition.

#### Creation Error Message Context

=== "Terraform Plugin Framework (Preferred)"
    Errors encountered during creation should include additional messaging about the location or cause of the error for operators and code maintainers.
    Plugin Framework based resources will append error [diagnostics](https://developer.hashicorp.com/terraform/plugin/framework/diagnostics) to the `resource.CreateResponse` `Diagnostics` field.
    The `create.ProblemStandardMessage` helper function can be used for constructing the appropriate context to accompany the error.

    ```go
    if err != nil {
        resp.Diagnostics.AddError(
            create.ProblemStandardMessage(names.{{ .Service }}, create.ErrActionCreating, ResName{{ .Resource }}, plan.Name.String(), err),
            err.Error(),
        )
        return
    }
    ```

    e.g.

    ```go
    if err != nil {
        resp.Diagnostics.AddError(
            create.ProblemStandardMessage(names.QuickSight, create.ErrActionCreating, ResNameVPCConnection, plan.Name.String(), err),
            err.Error(),
        )
        return
    }
    ```

    Resources that use other operations that return errors (e.g. waiters) should follow a similar pattern, including the resource identifier since it has typically been set before this execution:

    ```go
    createTimeout := r.CreateTimeout(ctx, plan.Timeouts)
    waitOut, err := waitVPCConnectionCreated(ctx, conn, plan.ID.ValueString(), createTimeout)
    if err != nil {
        resp.Diagnostics.AddError(
            create.ProblemStandardMessage(names.QuickSight, create.ErrActionWaitingForCreation, ResNameVPCConnection, plan.ID.String(), err),
            err.Error(),
        )
        return
    }
    ```

=== "Terraform Plugin SDK V2"
    Errors encountered during creation should include additional messaging about the location or cause of the error for operators and code maintainers.
    The `create.AppendDiagError` helper function can be used to convert a native error into a [diagnostic](https://developer.hashicorp.com/terraform/plugin/framework/diagnostics), which is the method for surfacing warnings and errors in Terraform providers.

    ```go
    if err != nil {
        return create.AppendDiagError(diags, names.{{ .Service }}, create.ErrActionCreating, ResName{{ .Resource }}, d.Get("name").(string), err)...)
    }
    ```

    e.g.

    ```go
    if err != nil {
        return create.AppendDiagError(diags, names.IVS, create.ErrActionCreating, ResNameRecordingConfiguration, d.Id(), err)
    }
    ```

    Resources that use other operations that return errors (e.g. waiters) should follow a similar pattern, including the resource identifier since it has typically been set before this execution:

    ```go
    if _, err := waitRecordingConfigurationCreated(ctx, conn, d.Id(), d.Timeout(schema.TimeoutCreate)); err != nil {
        return create.AppendDiagError(diags, names.IVS, create.ErrActionWaitingForCreation, ResNameRecordingConfiguration, d.Id(), err)
    }
    ```

#### d.IsNewResource() Checks

!!! note
    This type of check only applies to Plugin SDK V2 based resources. Plugin Framework based resources rely solely on [retries and waiters](retries-and-waiters.md) to handle eventually consistent resources.

During resource creation, Terraform CLI expects either a properly applied state for the new resource or an error. To signal proper resource existence, the Terraform Plugin SDK uses an underlying resource identifier (set via `d.SetId(/* some value */)`). If for some reason the resource creation is returned without an error, but also without the resource identifier being set, Terraform CLI will return an error such as:

```sh
Error: Provider produced inconsistent result after apply

When applying changes to aws_sns_topic_subscription.sqs,
provider "registry.terraform.io/hashicorp/aws" produced an unexpected new
value: Root resource was present, but now absent.

This is a bug in the provider, which should be reported in the provider's own
issue tracker.
```

A typical pattern in resource implementations in the `CreateWithoutTimeout` function is to `return` the `ReadWithoutTimeout` function at the end to fill in the Terraform State for all attributes. Another typical pattern in resource implementations in the `ReadWithoutTimeout` function is to remove the resource from the Terraform State if the remote system returns an error or status that indicates the remote resource no longer exists by explicitly calling `d.SetId("")` and returning no error. If the remote system is not strongly read-after-write consistent (eventually consistent), this means the resource creation can return no error and also return no resource state.

To prevent this type of Terraform CLI error, the resource implementation should also check against `d.IsNewResource()` before removing from the Terraform State and returning no error. If that check is `true`, then remote operation error (or one synthesized from the non-existent status) should be returned instead. While adding this check will not fix the resource implementation to handle the eventually consistent nature of the remote system, the error being returned will be less opaque for operators and code maintainers to troubleshoot.

In the Terraform AWS Provider, an initial fix for the Terraform CLI error will typically look like:

```go
func resourceServiceThingCreate(ctx context.Context, d *schema.ResourceData, meta interface{}) diag.Diagnostics {
 	var diags diag.Diagnostics

   /* ... */

    return append(diags, resourceServiceThingRead(ctx, d, meta)...)
}

func resourceServiceThingRead(ctx context.Context, d *schema.ResourceData, meta interface{}) diag.Diagnostics {
  	var diags diag.Diagnostics

   /* ... */

    output, err := conn.DescribeServiceThing(input)

    if !d.IsNewResource() && tfawserr.ErrCodeEquals(err, "ResourceNotFoundException") {
        log.Printf("[WARN] {Service} {Thing} (%s) not found, removing from state", d.Id())
        d.SetId("")
        return diags
    }

    if err != nil {
        return create.AppendDiagError(diags, names.{{ .Service }}, create.ErrActionReading, ResName{{ .Resource }}, d.Id(), err)
    }

    /* ... */
}
```

If the remote system is eventually consistent, see the [Retries and Waiters documentation on Resource Lifecycle Retries](retries-and-waiters.md#resource-lifecycle-retries) for how to prevent consistency-type errors.

### Resource Read

For Terraform Plugin Framework based resources, read is implemented on the `Read` method of the resource struct.
For Terraform Plugin SDK V2 based resources, read is implemented on the `ReadWithoutTimeout` function of the resource schema definition.

#### Read Error Message Context

=== "Terraform Plugin Framework (Preferred)"
    Errors encountered during read should include the resource identifier (for managed resources) and additional messaging about the location or cause of the error for operators and code maintainers.
    Plugin Framework based resources will append error [diagnostics](https://developer.hashicorp.com/terraform/plugin/framework/diagnostics) to the `resource.ReadResponse` `Diagnostics` field.
    The `create.ProblemStandardMessage` helper function can be used for constructing the appropriate context to accompany the error.

    ```go
    if err != nil {
        resp.Diagnostics.AddError(
            create.ProblemStandardMessage(names.{{ .Service }}, create.ErrActionReading, ResName{{ .Resource }}, state.ID.String(), err),
            err.Error(),
        )
        return
    }
    ```

    e.g.

    ```go
    if err != nil {
        resp.Diagnostics.AddError(
            create.ProblemStandardMessage(names.QuickSight, create.ErrActionReading, ResNameVPCConnection, state.ID.String(), err),
            err.Error(),
        )
        return
    }
    ```

=== "Terraform Plugin SDK V2"
    Errors encountered during read should include the resource identifier (for managed resources) and additional messaging about the location or cause of the error for operators and code maintainers.
    The `create.AppendDiagError` helper function can be used to convert a native error into a [diagnostic](https://developer.hashicorp.com/terraform/plugin/framework/diagnostics), which is the method for surfacing warnings and errors in Terraform providers.

    ```go
    if err != nil {
        return create.AppendDiagError(diags, names.{{ .Service }}, create.ErrActionReading, ResName{{ .Resource }}, d.Id(), err)
    }
    ```

    e.g.

    ```go
    if err != nil {
        return create.AppendDiagError(diags, names.IVS, create.ErrActionReading, ResNameRecordingConfiguration, d.Id(), err)
    }
    ```

#### Singular Data Source Errors

A data source which is expected to return Terraform State about a single remote resource is commonly referred to as a "singular" data source.
Implementation-wise, it may use any available describe or list functionality from the remote system to retrieve the information.
In addition to remote operation and data handling errors, errors should also be returned if:

- Zero results are found.
- Multiple results are found.

For remote operations that are designed to return an error when the remote resource is not found, this error is typically just passed through similar to other remote operation errors.
For remote operations that are designed to return a successful result whether there are zero, one, or multiple results, the error must be generated.

For example in pseudo-code:

```go
output, err := conn.ListServiceThings(input)

if err != nil {
    // Return error diagnostic wrapping remote error
}

if output == nil || len(output.Results) == 0 {
    // Return custom error diagnostic indicating empty results
}

if len(output.Results) > 1 {
    // Return custom error diagnostic indicating multiple results
}
```

#### Plural Data Source Errors

An emergent concept is a data source that returns multiple results, acting similarly to listing functionality from the remote system.
These types of data sources should return _not_ return errors if:

- Zero results are found.
- Multiple results are found.

Remote operation and other data handling errors should still be returned.

### Resource Update

For Terraform Plugin Framework based resources, update is implemented on the `Update` method of the resource struct.
For Terraform Plugin SDK V2 based resources, update is implemented on the `UpdateWithoutTimeout` function of the resource schema definition.

#### Update Error Message Context

=== "Terraform Plugin Framework (Preferred)"
    Errors ecnountered during update should include the resource identifier and additional messaging about the location or cause of the error for operators and code maintainers.
    Plugin Framework based resources will append error [diagnostics](https://developer.hashicorp.com/terraform/plugin/framework/diagnostics) to the `resource.UpdateResponse` `Diagnostics` field.
    The `create.ProblemStandardMessage` helper function can be used for constructing the appropriate context to accompany the error.

    ```go
    if err != nil {
        resp.Diagnostics.AddError(
            create.ProblemStandardMessage(names.{{ .Service }}, create.ErrActionUpdating, ResName{{ .Resource }}, plan.ID.String(), err),
            err.Error(),
        )
        return
    }
    ```

    e.g.

    ```go
    if err != nil {
        resp.Diagnostics.AddError(
            create.ProblemStandardMessage(names.QuickSight, create.ErrActionUpdating, ResNameVPCConnection, plan.ID.String(), err),
            err.Error(),
        )
        return
    }
    ```

    Resources that use other operations that return errors (e.g. waiters) should follow a similar pattern:

    ```go
    updateTimeout := r.UpdateTimeout(ctx, plan.Timeouts)
    waitOut, err := waitVPCConnectionUpdated(ctx, conn, plan.ID.ValueString(), updateTimeout)
    if err != nil {
        resp.Diagnostics.AddError(
            create.ProblemStandardMessage(names.QuickSight, create.ErrActionWaitingForUpdate, ResNameVPCConnection, plan.ID.String(), err),
            err.Error(),
        )
        return
    }
    ```

=== "Terraform Plugin SDK V2"
    Errors encountered during update should include the resource identifier and additional messaging about the location or cause of the error for operators and code maintainers.
    The `create.AppendDiagError` helper function can be used to convert a native error into a [diagnostic](https://developer.hashicorp.com/terraform/plugin/framework/diagnostics), which is the method for surfacing warnings and errors in Terraform providers.

    ```go
    if err != nil {
        return create.AppendDiagError(diags, names.{{ .Service }}, create.ErrActionUpdating, ResName{{ .Resource }}, d.Id(), err)
    }
    ```

    e.g.

    ```go
    if err != nil {
         return create.AppendDiagError(diags, names.IVS, create.ErrActionUpdating, ResNameRecordingConfiguration, d.Id(), err)
    }
    ```

    Resources that use other operations that return errors (e.g. waiters) should follow a similar pattern:

    ```go
    if _, err := waitRecordingConfigurationUpdated(ctx, conn, d.Id(), d.Timeout(schema.TimeoutUpdate)); err != nil {
         return create.AppendDiagError(diags, names.IVS, create.ErrActionWaitingForUpdate, ResNameRecordingConfiguration, d.Id(), err)
    }
    ```

### Resource Deletion

For Terraform Plugin Framework based resources, deletion is implemented on the `Delete` method of the resource struct.
For Terraform Plugin SDK V2 based resources, deletion is implemented on the `DeleteWithoutTimeout` function of the resource schema definition.

#### Deletion Error Message Context

=== "Terraform Plugin Framework (Preferred)"
    Errors encountered during deletion should include the resource identifier and additional messaging about the location or cause of the error for operators and code maintainers.
    Plugin Framework based resources will append error [diagnostics](https://developer.hashicorp.com/terraform/plugin/framework/diagnostics) to the `resource.DeleteResponse` `Diagnostics` field.
    The `create.ProblemStandardMessage` helper function can be used for constructing the appropriate context to accompany the error.

    ```go
    if err != nil {
        resp.Diagnostics.AddError(
            create.ProblemStandardMessage(names.{{ .Service }}, create.ErrActionDeleting, ResName{{ .Resource }}, state.ID.String(), err),
            err.Error(),
        )
        return
    }
    ```

    e.g.

    ```go
    if err != nil {
        resp.Diagnostics.AddError(
            create.ProblemStandardMessage(names.QuickSight, create.ErrActionDeleting, ResNameVPCConnection, state.ID.String(), err),
            err.Error(),
        )
        return
    }
    ```

    Resources that use other operations that return errors (e.g. waiters) should follow a similar pattern:

    ```go
    deleteTimeout := r.DeleteTimeout(ctx, plan.Timeouts)
    waitOut, err := waitVPCConnectionDeleted(ctx, conn, state.ID.ValueString(), deleteTimeout)
    if err != nil {
        resp.Diagnostics.AddError(
            create.ProblemStandardMessage(names.QuickSight, create.ErrActionWaitingForDeletion, ResNameVPCConnection, state.ID.String(), err),
            err.Error(),
        )
        return
    }
    ```

=== "Terraform Plugin SDK V2"
    Errors encountered during deletion should include the resource identifier and additional messaging about the location or cause of the error for operators and code maintainers.
    The `create.AppendDiagError` helper function can be used to convert a native error into a [diagnostic](https://developer.hashicorp.com/terraform/plugin/framework/diagnostics), which is the method for surfacing warnings and errors in Terraform providers.

    ```go
    if err != nil {
        return create.AppendDiagError(diags, names.{{ .Service }}, create.ErrActionDeleting, ResName{{ .Resource }}, d.Id(), err)
    }
    ```

    e.g.

    ```go
    if err != nil {
        return create.AppendDiagError(diags, names.IVS, create.ErrActionDeleting, ResNameRecordingConfiguration, d.Id(), err)
    }
    ```

    Resources that use other operations that return errors (e.g. waiters) should follow a similar pattern:

    ```go
    if _, err := waitRecordingConfigurationDeleted(ctx, conn, d.Id(), d.Timeout(schema.TimeoutDelete)); err != nil {
        return create.AppendDiagError(diags, names.IVS, create.ErrActionWaitingForDeletion, ResNameRecordingConfiguration, d.Id(), err)
    }
    ```

#### Resource Already Deleted

A typical pattern for resource deletion is to immediately perform the remote system deletion operation without checking existence.
This is generally acceptable as operators are encouraged to always refresh their Terraform State prior to performing changes.
However, in certain scenarios, such as external systems modifying the remote system prior to the Terraform execution, it is still possible that the remote system will return an error signifying that the resource does not exist.
In these cases, resources should implement logic that skips returning the error.

=== "Terraform Plugin Framework (Preferred)"
    !!! note
        The Terraform Plugin Framework automatically handles the equivalent of `resp.State.RemoveResource()` on deletion, so it is not necessary to include it.

    ```go
    output, err := conn.DeleteServiceThing(input)

    if tfawserr.ErrCodeEquals(err, "ResourceNotFoundException") {
        return
    }

    if err != nil {
        resp.Diagnostics.AddError(
            create.ProblemStandardMessage(names.{{ .Service }}, create.ErrActionDeleting, ResName{{ .Resource }}, state.ID.String(), err),
            err.Error(),
        )
        return
    }
    ```

=== "Terraform Plugin SDK V2"
    !!! note
        The Terraform Plugin SDK V2 automatically handles the equivalent of `d.SetId("")` on deletion, so it is not necessary to include it.

    ```go
    output, err := conn.DeleteServiceThing(input)

    if tfawserr.ErrCodeEquals(err, "ResourceNotFoundException") {
        return diags
    }

    if err != nil {
        return create.AppendDiagError(diags, names.{{ .Service }}, create.ErrActionDeleting, ResName{{ .Resource }}, d.Id(), err)
    }
    ```
# Frequently Asked Questions

<!-- markdownlint-disable no-trailing-punctuation -->

## Who are the maintainers?

The HashiCorp Terraform AWS provider team is :

* Marc Cosentino, Product Manager - GitHub [@marcosentino](https://github.com/marcosentino)
* Simon Davis, Engineering Manager - GitHub [@breathingdust](https://github.com/breathingdust)
* Justin Retzolk, Technical Community Manager - GitHub [@justinretzolk](https://github.com/justinretzolk)
* Adrian Johnson, Engineer - GitHub [@johnsonaj](https://github.com/johnsonaj)
* Dirk Avery, Engineer - GitHub [@YakDriver](https://github.com/yakdriver)
* Graham Davison, Engineer - GitHub [@gdavison](https://github.com/gdavison)
* Jared Baker, Engineer - GitHub [@jar-b](https://github.com/jar-b)
* Kerim Satirli, Developer Advocate - GitHub [@ksatirli](https://github.com/ksatirli)
* Kit Ewbank, Engineer - GitHub [@ewbankkit](https://github.com/ewbankkit)
* Sharon Nam, Engineer - GitHub [@nam054](https://github.com/nam054)

## Why isn’t my PR merged yet?

Unfortunately, due to the volume of issues and new pull requests we receive, we are unable to give each one the full attention that we would like. We always focus on the contributions that provide the greatest value to the most community members. For more information on how we prioritize pull requests, see the [prioritization guide](prioritization.md).

## How do you decide what gets merged for each release?

We have a large backlog of pull requests to get through and the team is moving through them as quickly as we can. All pull requests must be reviewed by a HashiCorp engineer before inclusion. This is to ensure that the design of the addition fits with what provider users have come to expect, and to ensure that testing and best practices are adhered to. This is particularly important for such a large codebase, to ensure that we sustain its maintainability as it grows.

The number one factor we look at when deciding what issues to look at are your 👍 [reactions](https://blog.github.com/2016-03-10-add-reactions-to-pull-requests-issues-and-comments/) to the original issue/PR description as these can be [easily discovered](https://github.com/hashicorp/terraform-provider-aws/issues?q=is%3Aopen+sort%3Areactions-%2B1-desc). Comments that further explain desired use cases or poor user experience are also heavily factored in. The items with the most support are always on our radar, and we commit to keeping the community updated on their status and potential timelines.

We publish a [roadmap](https://github.com/hashicorp/terraform-provider-aws/blob/main/ROADMAP.md) every quarter which describes major themes or specific product areas of focus. What is excluded from the public roadmap is work performed under NDA with AWS on new services, and any ad-hoc work we pick up during the quarter. This ad-hoc work can be responding to bugs, gardening day activity, customer prioritization, and technical debt items.

We also are investing time to improve the contributing experience by improving documentation, adding more linter coverage to ensure that incoming PRs can be in as good shape as possible. This will allow us to get through them quicker.

## My PR hasn't been merged and it now has merge conflicts/failed checks, should I keep it up to date?

We realize that sometimes pull requests sit for a considerable amount of time without being addressed. During this time period they may accumulate merge conflicts and failed linter checks as the provider codebase moves forward. As maintainers we have no expectation that you keep your PR up to date, these issues will be addressed at review time most often by the maintainers themselves. Obviously we would hope that your PR is mergeable when first raised! The mergeability of the PR does not affect its prioritization for review.

## How often do you release?

We release weekly on Thursday. We release often to ensure we can bring value to the community at a frequent cadence and to ensure we are in a good place to react to AWS region launches and service announcements.

## Backward Compatibility Promise

Our policy is described on the Terraform website [here](https://www.terraform.io/plugin/sdkv2/best-practices/versioning). While we do our best to prevent breaking changes until major version releases of the provider, it is generally recommended to [pin the provider version in your configuration](https://www.terraform.io/language/providers/configuration#provider-versions).

Due to the constant release pace of AWS and the relatively infrequent major version releases of the provider, there can be cases where a minor version update may contain unexpected changes depending on your configuration or environment. These may include items such as a resource requiring additional IAM permissions to support newer functionality. We typically base these decisions on a pragmatic compromise between introducing a relatively minor one-time inconvenience for a subset of the community versus a better overall user experience for the entire community.

## Once a major release is published, will new features and fixes be backported to previous versions?

Generally, new features and fixes will only be added to the most recent major version. Due to the high-touch nature of provider development and the extensive regression testing required to ensure stability, maintaining multiple versions of the provider is not sustainable at this time. An exception to this could be a discovered security vulnerability for which backporting may be the most reasonable course of action. These would be reviewed on a case-by-case basis.

## AWS just announced a new region, when will I see it in the provider?

Normally pretty quickly. We usually see the region appear within the `aws-go-sdk` within a couple of days of the announcement. Depending on when it lands, we can often get it out within the current or following weekly release. Comparatively, adding support for a new region in the S3 backend can take a little longer, as it is shipped as part of Terraform Core and not via the AWS Provider.

Please note that this new region requires a manual process to enable in your account. Once enabled in the console, it takes a few minutes for everything to work properly.

If the region is not enabled properly, or the enablement process is still in progress, you may receive errors like these:

```console
$ terraform apply

Error: error validating provider credentials: error calling sts:GetCallerIdentity: InvalidClientTokenId: The security token included in the request is invalid.
    status code: 403, request id: 142f947b-b2c3-11e9-9959-c11ab17bcc63

  on main.tf line 1, in provider "aws":
   1: provider "aws" {
```

To use this new region before support has been added to the Terraform AWS Provider, you can disable the provider's automatic region validation via:

```terraform
provider "aws" {
  # ... potentially other configuration ...

  region                 = "af-south-1"
  skip_region_validation = true
}

```

## How can I help?

Great question, if you have contributed before check out issues with the `help-wanted` label. These are normally enhancement issues that will have a great impact, but the maintainers are unable to develop them in the near future. If you are just getting started, take a look at issues with the `good-first-issue` label. Items with these labels will always be given priority for response.

Check out the [Contributing Guide](https://hashicorp.github.io/terraform-provider-aws/) for additional information.

## How can I become a maintainer?

This is an area under active research. Stay tuned!
# Welcome

The Terraform AWS Provider is the work of thousands of contributors, and is maintained by a small team within HashiCorp. This site contains extensive instructions about how to contribute and how the AWS provider works.

!!! tip
    This documentation is intended for Terraform AWS Provider code developers. Typical operators writing and applying Terraform configurations do not need to read or understand this material.

## Contribute

Please follow the following steps to ensure your contribution goes smoothly.

### 1. Configure Development Environment

Install Terraform and Go. Clone the repository, compile the provider, and set up testing. Refer to [Configure Development Environment](development-environment.md).

### 2. Debug Code

If you are looking to _create or enhance code_, such as a new resource or adding an argument to an existing resource, skip to the next step.

Finding and fixing errors in the AWS Provider can be difficult. We have a [debugging guide](debugging.md) to help you get started.

### 3. Change Code

Follow the guide for your contribution type and refer to the Development Reference materials as needed for additional details about [provider design](provider-design.md), expected [naming conventions](naming.md), guidance for [error handling](error-handling.md), etc.

| Contribution Guide | Description |
|--------------------|-------------|
| [Small Changes](bugs-and-enhancements.md) | Requirements for small additions or bug-fixes on existing resources/data sources |
| [Resources](add-a-new-resource.md) | Allow the management of a logical resource within AWS by adding a new resource to the Terraform AWS Provider. |
| [Data Source](add-a-new-datasource.md) | Let your Terraform configurations use data from resources not under local management by creating ready only data sources. |
| [Services](add-a-new-service.md) | Allow Terraform (via the AWS Provider) to manage an entirely new AWS service by introducing the resources and data sources required to manage configuration of the service. |
| [AWS Region](add-a-new-region.md) | New regions are immediately usable with the provider with the caveat that a configuration workaround is required to skip validation of the region during cli operations. A small set of changes are required to make this workaround necessary. |
| [Resource Name Generation](resource-name-generation.md) | Allow a resource to either fully, or partially, generate its own resource names. This can be useful in cases where the resource name uniquely identifies the resource and it needs to be recreated. It can also be used when a name is required, but the specific name is not important. |
| [Tagging Support](resource-tagging.md) | Many AWS resources allow assigning metadata via tags. However, frequently AWS services are launched without tagging support so this will often need to be added later. |
| [Import Support](add-import-support.md) | Adding import support allows `terraform import` to be run targeting an existing unmanaged resource and pulling its configuration into Terraform state. Typically import support is added during initial resource implementation but in some cases this will need to be added later. |
| [Documentation Changes](documentation-changes.md)| The provider documentation is displayed on the [Terraform Registry](https://registry.terraform.io/providers/hashicorp/aws/latest) and is sourced and refreshed from the provider repository during the release process. |

### 4. Write Tests

We require all changes to be covered by [acceptance tests](running-and-writing-acceptance-tests.md) and/or [unit tests](unit-tests.md), depending on the situation. In the context of the Terraform AWS Provider, _acceptance tests_ are tests of interactions with AWS, such as creating, reading information about, and destroying AWS resources. In contrast, _unit tests_ test functionality wholly within the provider itself, such as function tests.

If you are unable to pay for acceptance tests for your contributions, mention this in your pull request. We will happily accept "best effort" acceptance tests implementations and run them for you on our side. Your PR may take longer to merge, but this is not a blocker for contributions.

### 5. Continuous Integration

When submitting a pull request, you'll notice that we run several automated processes on your proposed change.Some of these processes are tests to ensure your contribution aligns with our standards. While we strive for accuracy, some users may find these tests confusing. Check out [Continuous Integration](continuous-integration.md) for additional clarity.

### 6. Update the Changelog

HashiCorp's open-source projects have always maintained a user-friendly, readable CHANGELOG.md that allows users to tell at a glance whether a release should have any effect on them, and to gauge the risk of an upgrade. Not all changes require an entry in the changelog, refer to our [Changelog Process](changelog-process.md) for details about when and how to create a changelog.

### 7. Create a Pull Request

When your contribution is ready, Create a [Pull Request](raising-a-pull-request.md) in the AWS provider repository.

Pull requests are usually triaged within a few days of creation and are prioritized based on community reactions. Our [Prioritization Guides](prioritization.md) provide more details about the process.

## Submit an Issue

In addition to contributions, we welcome [bug reports](https://github.com/hashicorp/terraform-provider-aws/issues/new?assignees=&labels=&template=Bug_Report.md) and [feature requests](https://github.com/hashicorp/terraform-provider-aws/issues/new?assignees=&labels=enhancement&template=Feature_Request.md).

## Join the Contributors Slack

For frequent contributors, it's useful to join the contributors Slack channel hosted within the HashiCorp Slack workspace. This Slack channel is used to discuss topics such as general contribution questions, suggestions for improving the contribution process, coordinating on pair programming sessions, etc. The channel is not intended as a place to request status updates on open issues or pull requests. For prioritization questions, instead refer to the [prioritization guide](prioritization.md).

To request to join, fill out the [request form](https://forms.gle/Gf9ZAmUYXuzafkct6) and allow time for the request to be reviewed and processed.
# Issue Reporting and Lifecycle

## Issue Reporting Checklists

We welcome issues of all kinds including feature requests, bug reports, and
general questions. Below you'll find checklists with guidelines for well-formed
issues of each type.

We encourage opening new issues rather than commenting on closed issues if a problem has not been completely solved or causes a regression. This ensures we are able to triage it effectively.

### [Bug Reports](https://github.com/hashicorp/terraform-provider-aws/issues/new?template=Bug_Report.md)

- __Test against the latest release__: Make sure you test against the latest
   released version. It is possible we already fixed the bug you're experiencing.

- __Search for possible duplicate reports__: It's helpful to keep bug
   reports consolidated to one thread, so do a quick search on existing bug
   reports to check if anybody else has reported the same thing. You can [scope
      searches by the label "bug"](https://github.com/hashicorp/terraform-provider-aws/issues?q=is%3Aopen+is%3Aissue+label%3Abug) to help narrow things down.

- __Include steps to reproduce__: Provide steps to reproduce the issue,
   along with your `.tf` files, with secrets removed, so we can try to
   reproduce it. Without this, it makes it much harder to fix the issue.

- __For panics, include `crash.log`__: If you experienced a panic, please
   create a [gist](https://gist.github.com) of the *entire* generated crash log
   for us to look at. Double-check check no sensitive items were in the log.

### [Feature Requests](https://github.com/hashicorp/terraform-provider-aws/issues/new?labels=enhancement&template=Feature_Request.md)

- __Search for possible duplicate requests__: It's helpful to keep requests
   consolidated to one thread, so do a quick search on existing requests to
   check if anybody else has reported the same thing. You can [scope searches by
      the label "enhancement"](https://github.com/hashicorp/terraform-provider-aws/issues?q=is%3Aopen+is%3Aissue+label%3Aenhancement) to help narrow things down.

- __Include a use case description__: In addition to describing the
   behavior of the feature you'd like to see added, it's helpful to also lay
   out the reason why the feature would be important and how it would benefit
   Terraform users.

### Questions

- __Search for answers in Terraform documentation__: We're happy to answer
   questions in GitHub Issues, but it helps reduce issue churn and maintainer
   workload if you work to [find answers to common questions in the
   documentation](https://registry.terraform.io/providers/hashicorp/aws/latest/docs). Oftentimes Question issues result in documentation updates
   to help future users, so if you don't find an answer, you can give us
   pointers for where you'd expect to see it in the docs.

## Issue Lifecycle

!!! tip
    For detailed information on how issues are prioritized, see the [prioritization guide](prioritization.md).

1. The issue is reported.

2. The issue is verified and categorized by a Terraform collaborator.
   Categorization is done via GitHub labels. We generally use a two-label
   system of (1) issue/PR type, and (2) section of the codebase. Type is
   one of "bug", "enhancement", "documentation", or "question", and section
   is usually the AWS service name.

3. An initial triage process determines whether the issue is critical and must
   be addressed immediately, or can be left open for community discussion.

4. The issue is addressed in a pull request or commit. The issue number will be
   referenced in the commit message so that the code that fixes it is clearly
   linked.

5. The issue is closed. Sometimes, valid issues will be closed because they are
   tracked elsewhere or non-actionable. The issue is still indexed and
   available for future viewers, or can be re-opened if necessary.

6. 30 days after the issue has been closed it is locked, preventing further comments.
# Makefile Cheat Sheet

The Terraform AWS Provider Makefile includes a lot of functionality to make working on the provider easier and more efficient. Many contributors are familiar with using the Makefile for running acceptance tests, but there is a lot more functionality hidden in this humble file.

!!! tip
    See [Continuous Integration](continuous-integration.md) for more information about the CI-focused parts of the Makefile.

## Basics

If you're new to our Makefile, this section will bring you up to speed.

### Location

The Makefile is located in the root of the provider repository and is called [GNUmakefile](https://github.com/hashicorp/terraform-provider-aws/blob/main/GNUmakefile).

### Phony Targets

Historically, Makefiles were used to help with the complexities of compiling and linking software projects, managing dependencies, and enabling the creation of various _target_ files. `make` would create a "target" file as determined by the command line:

```console
% make <target>
```

Today, we use _phony_ targets in the Makefile to automate many tasks. "Phony" simply means that the target doesn't define the file we're trying to make but rather the recipe we want to perform, such as running tests.

For example, `testacc` is a phony target to simplify the command for running acceptance tests:

```console
make testacc TESTS=TestAccIAMRole_basic PKG=iam
```

### Meta Targets and Dependent Targets

_Meta_ targets are `make` targets that only run other targets. They aggregate the functionality of other targets for convenience. In the [Cheat Sheet](#cheat-sheet), meta targets are marked with <sup>M</sup>.

_Dependent_ targets also run other targets but, in addition, have their own functionality. A dependent target generally runs the other targets first before executing its own functionality. In the [Cheat Sheet](#cheat-sheet), dependent targets are marked with <sup>D</sup>.

For example, in the cheat sheet, the `ci`, `clean`, and `misspell` targets are meta targets that only run other targets.

On the other hand, examples of dependent targets are `deps-check`, `gen-check`, and `semgrep-code-quality`.

When you call a meta or dependent target and it runs other targets, those targets must complete successfully in order for the target you called to succeed.

## Variables

In the [Cheat Sheet](#cheat-sheet), you can see which variables affect which [targets](#phony-targets). This section describes the variables in more detail.

Variables are often defined before the `make` call on the same line, such as `MY_VAR=42 make my-target`. However, they can also be set on the same line _after_ the `make` call or in your environment, using, for example, `export MY_VAR=42`.

!!! note
    Targets that [meta and dependent targets](#meta-targets-and-dependent-targets) run may not all respect the same set of variables.

* `ACCTEST_PARALLELISM` - (Default: `20`) Number of concurrent acceptance tests to run. Overridden if `P` is set.
* `ACCTEST_TIMEOUT` - (Default: `360m`) Timeout before acceptance tests panic.
* `BASE_REF` - (Default: `main`) Origin reference to use for Git `diff` comparison, as in `origin/BASE_REF`.
* `CURDIR` - (Default: Value of `$PWD`) Root path to use for `/.ci/scripts/`.
* `GO_VER` - (Default: Value in `.go-version` file) Version of Go to use. To use the default version on your system, use `GO_VER=go`.
* `K` - (Default: _None_) Name of the service package you want to use, such as `ec2`, `iam`, or `lambda`, limiting Go processing to that package and dependencies. Equivalent to `PKG` variable. Assigns values to `PKG_NAME`, `SVC_DIR`, and `TEST` overridding any values set.
* `P` - (Default: `20`) Number of concurrent acceptance tests to run. Assigns a value to `ACCTEST_PARALLELISM` overridding any value set.
* `PKG` - (Default: _None_) Name of the service package you want to use, such as `ec2`, `iam`, or `lambda`, limiting Go processing to that package and dependencies. Equivalent to `K` variable. Assigns values to `PKG_NAME`, `SVC_DIR`, and `TEST` overridding any values set.
* `PKG_NAME` - (Default: `internal`) Subdirectory (Go package) to use as the basis for Go processing. Overridden if `PKG` or `K` is set.
* `RUNARGS` - (Default: _None_) Raw arguments passed to Go when running acceptance tests. For example, `RUNARGS=-run=TestMyTest`. Overridden if `TESTS` or `T` is set.
* `SEMGREP_ARGS` - (Default: `--error`) Semgrep arguments. See the [Semgrep reference](https://semgrep.dev/docs/cli-reference#semgrep-scan-command-options).
* `SEMGREP_ENABLE_VERSION_CHECK` - (Default: `false`) Whether to check Semgrep servers to verify you are running the latest Semgrep version.
* `SEMGREP_SEND_METRICS` - (Default: `off`) When Semgrep usage metrics are sent to Semgrep.
* `SEMGREP_TIMEOUT` - (Default: `900`) Maximum time to spend running a rule on a single file, in seconds.
* `SVC_DIR` - (Default: `./internal/service`) Directory to as the base for recursive processing. Overridden if `PKG` or `K` is set.
* `SWEEP_DIR` - (Default: `./internal/sweep`) Location of the sweep directory.
* `SWEEP` - (Default: `us-west-2,us-east-1,us-east-2,us-west-1`) Comma-separated list of AWS regions to sweep.
* `SWEEP_TIMEOUT` - (Default: `360m`) Time Go will spend sweeping resources before panicking.
* `SWEEPARGS` - (Default: _None_) Raw arguments that define what to sweep, including dependencies. Similar to `SWEEPERS`. For example, `SWEEPARGS=-sweep-run=aws_example_thing`.
* `SWEEPERS` - (Default: _None_) Resources to sweep, including dependencies. Similar to `SWEEPARGS`. For example, `SWEEPERS=aws_example_thing`. Assigns a value to `SWEEPARGS` overridding any value set.
* `T` - (Default: _None_) Names of tests to run. Equivalent to `TESTS`. Assigns a value to `RUNARGS` overridding any value set.
* `TEST` - (Default: `./...`) Limit tests to this directory and dependencies. Overridden if `PKG` or `K` is set.
* `TEST_COUNT` - (Default: `1`) Number of times to run each acceptance or unit test.
* `TESTS` - (Default: _None_) Names of tests to run. Equivalent to `T`. Assigns a value to `RUNARGS` overridding any value set.
* `TESTARGS` - (Default: _None_) Raw arguments passed to Go when running tests. Unlike `RUNARGS`, this is _not_ overridden if `TESTS` or `T` is set.

## Cheat Sheet

* **Target**: Use as a subcommand to `make`, such as `make gen`. [Meta and dependent targets](#meta-targets-and-dependent-targets) are marked with <sup>M</sup> and <sup>D</sup>, respectively.
* **Description**: When CI-related, this aligns with the name of the check as seen on GitHub.
* **CI?**: Indicates whether the target is equivalent or largely equivalent to a check run on the GitHub repository for a pull request. See [continuous integration](continuous-integration.md) for more details.
* **Legacy?**: Indicates whether the target is a legacy holdover. Use caution with a legacy target! It may not work, or it may perform checks or fixes that do _not_ align with current practices. In the future, this target should be removed, modernized, or verified to still have value.
* **Vars**: [Variables](#variables) that you can set when using the target, such as `MY_VAR=42 make my-target`. [Meta and dependent targets](#meta-targets-and-dependent-targets) run other targets that may not respect the same variables.

!!! tip
    Makefile autocompletion works out of the box on Zsh (the default shell for Terminal on macOS) and Fish shells. For Bash, the `bash-completion` package, among others, provides Makefile autocompletion. Using autocompletion allows you, for example, to type `make ac`, press _tab_, and the shell autocompletes `make acctest-lint`.

| Target | Description | CI? | Legacy? | Vars |
| --- | --- | --- | --- | --- |
| `acctest-lint`<sup>M</sup> | Run all CI acceptance test checks | ✔️ |  | `K`, `PKG`, `SVC_DIR` |
| `build`<sup>D</sup> | Build the provider |  |  | `GO_VER` |
| `changelog-misspell` | CHANGELOG Misspell / misspell | ✔️ |  |  |
| `ci`<sup>M</sup> | Run all CI checks | ✔️ |  | `BASE_REF`, `GO_VER`, `K`, `PKG`, `SEMGREP_ARGS`, `SVC_DIR`, `TEST`, `TESTARGS` |
| `ci-quick`<sup>M</sup> | Run quicker CI checks | ✔️ |  | `BASE_REF`, `GO_VER`, `K`, `PKG`, `SEMGREP_ARGS`, `SVC_DIR`, `TEST`, `TESTARGS` |
| `clean`<sup>M</sup> | Clean up Go cache, tidy and re-install tools |  |  | `GO_VER` |
| `clean-go`<sup>D</sup> | Clean up Go cache |  |  | `GO_VER` |
| `clean-make-tests` | Clean up artifacts from make tests |  |  |  |
| `clean-tidy`<sup>D</sup> | Clean up tidy |  |  | `GO_VER` |
| `copyright` | Copyright Checks / add headers check | ✔️ |  |  |
| _default_ | = `build` |  |  | `GO_VER` |
| `deps-check`<sup>D</sup> | Dependency Checks / go_mod | ✔️ |  | `GO_VER` |
| `docs`<sup>M</sup> | Run all CI documentation checks | ✔️ |  |  |
| `docs-check` | Check provider documentation |  | ✔️ |  |
| `docs-link-check` | Documentation Checks / markdown-link-check | ✔️ |  |  |
| `docs-lint` | Lint documentation |  | ✔️ |  |
| `docs-lint-fix` | Fix documentation linter findings |  | ✔️ |  |
| `docs-markdown-lint` | Documentation Checks / markdown-lint | ✔️ |  |  |
| `docs-misspell` | Documentation Checks / misspell | ✔️ |  |  |
| `examples-tflint` | Examples Checks / tflint | ✔️ |  |  |
| `fix-constants`<sup>M</sup> | Use Semgrep to fix constants |  |  | `K`, `PKG`, `PKG_NAME`, `SEMGREP_ARGS` |
| `fix-imports` | Fixing source code imports with goimports |  |  |  |
| `fmt` | Fix Go source formatting |  |  | `K`, `PKG`, `PKG_NAME` |
| `fmt-check` | Verify Go source is formatted |  |  | `CURDIR` |
| `fumpt` | Run gofumpt |  |  | `K`, `PKG`, `PKG_NAME` |
| `gen`<sup>D</sup> | Run all Go generators |  |  | `GO_VER` |
| `gen-check`<sup>D</sup> | Provider Checks / go_generate | ✔️ |  |  |
| `generate-changelog` | Generate changelog |  |  | `CURDIR` |
| `gh-workflow-lint` | Workflow Linting / actionlint | ✔️ |  |  |
| `go-build` | Provider Checks / go-build | ✔️ |  |  |
| `go-misspell` | Provider Checks / misspell | ✔️ |  |  |
| `golangci-lint`<sup>M</sup> | All golangci-lint Checks | ✔️ |  | `K`, `PKG`, `TEST` |
| `golangci-lint1` | golangci-lint Checks / 1 of 2 | ✔️ |  | `K`, `PKG`, `TEST` |
| `golangci-lint2` | golangci-lint Checks / 2 of 2 | ✔️ |  | `K`, `PKG`, `TEST` |
| `help` | Display help |  |  |  |
| `import-lint` | Provider Checks / import-lint | ✔️ |  | `K`, `PKG`, `TEST` |
| `install`<sup>M</sup> | = `build` |  |  | `GO_VER` |
| `lint`<sup>M</sup> | Legacy target, use caution |  | ✔️ |  |
| `lint-fix`<sup>M</sup> | Fix acceptance test, website, and docs linter findings |  | ✔️ |  |
| `misspell`<sup>M</sup> | Run all CI misspell checks | ✔️ |  |  |
| `prereq-go` | Install the project's Go version |  |  | `GO_VER` |
| `provider-lint` | ProviderLint Checks / providerlint | ✔️ |  | `K`, `PKG`, `SVC_DIR` |
| `provider-markdown-lint` | Provider Check / markdown-lint | ✔️ |  |  |
| `sane`<sup>D</sup> | Run sane check |  |  | `ACCTEST_PARALLELISM`, `ACCTEST_TIMEOUT`, `GO_VER`, `TEST_COUNT` |
| `sanity`<sup>D</sup> | Run sanity check (failures allowed) |  |  | `ACCTEST_PARALLELISM`, `ACCTEST_TIMEOUT`, `GO_VER`, `TEST_COUNT` |
| `semgrep`<sup>M</sup> | Run all CI Semgrep checks | ✔️ |  | `K`, `PKG`, `PKG_NAME`, `SEMGREP_ARGS` |
| `semgrep-all`<sup>D</sup> | Run semgrep on all files |  |  | `K`, `PKG`, `PKG_NAME`, `SEMGREP_ARGS` |
| `semgrep-code-quality`<sup>D</sup> | Semgrep Checks / Code Quality Scan | ✔️ |  | `K`, `PKG`, `PKG_NAME`, `SEMGREP_ARGS` |
| `semgrep-constants`<sup>D</sup> | Fix constants with Semgrep --autofix |  |  | `K`, `PKG`, `PKG_NAME`, `SEMGREP_ARGS` |
| `semgrep-docker`<sup>D</sup> | Run Semgrep |  | ✔️ |  |
| `semgrep-fix`<sup>D</sup> | Fix Semgrep issues that have fixes |  |  | `K`, `PKG`, `PKG_NAME`, `SEMGREP_ARGS` |
| `semgrep-naming`<sup>D</sup> | Semgrep Checks / Test Configs Scan | ✔️ |  | `K`, `PKG`, `PKG_NAME`, `SEMGREP_ARGS` |
| `semgrep-naming-cae`<sup>D</sup> | Semgrep Checks / Naming Scan Caps/`AWS`/EC2 | ✔️ |  | `K`, `PKG`, `PKG_NAME`, `SEMGREP_ARGS` |
| `semgrep-service-naming`<sup>D</sup> | Semgrep Checks / Service Name Scan A-Z | ✔️ |  | `K`, `PKG`, `PKG_NAME`, `SEMGREP_ARGS` |
| `semgrep-validate` | Validate Semgrep configuration files |  |  |  |
| `skaff`<sup>D</sup> | Install skaff |  |  | `GO_VER` |
| `skaff-check-compile` | Skaff Checks / Compile skaff | ✔️ |  |  |
| `sweep`<sup>D</sup> | Run sweepers |  |  | `GO_VER`, `SWEEP_DIR`, `SWEEP_TIMEOUT`, `SWEEP`, `SWEEPARGS` |
| `sweeper`<sup>D</sup> | Run sweepers with failures allowed |  |  | `GO_VER`, `SWEEP_DIR`, `SWEEP_TIMEOUT`, `SWEEP` |
| `sweeper-check`<sup>M</sup> | Provider Checks / Sweeper Linked, Unlinked | ✔️ |  |  |
| `sweeper-linked` | Provider Checks / Sweeper Functions Linked | ✔️ |  |  |
| `sweeper-unlinked`<sup>D</sup> | Provider Checks / Sweeper Functions Not Linked | ✔️ |  |  |
| `t`<sup>D</sup> | Run acceptance tests  (similar to `testacc`) |  |  | `ACCTEST_PARALLELISM`, `ACCTEST_TIMEOUT`, `GO_VER`, `K`, `PKG`, `PKG_NAME`, `RUNARGS`, `TEST_COUNT`, `TESTARGS` |
| `test`<sup>D</sup> | Run unit tests |  |  | `GO_VER`, `K`, `PKG`, `TEST`, `TESTARGS` |
| `test-compile`<sup>D</sup> | Test package compilation |  |  | `GO_VER`, `K`, `PKG`, `PKG_NAME`, `TEST`, `TESTARGS` |
| `testacc`<sup>D</sup> | Run acceptance tests |  |  | `ACCTEST_PARALLELISM`, `ACCTEST_TIMEOUT`, `GO_VER`, `K`, `PKG`, `PKG_NAME`, `RUNARGS`, `TEST_COUNT`, `TESTARGS` |
| `testacc-lint` | Acceptance Test Linting / terrafmt | ✔️ |  | `K`, `PKG`, `SVC_DIR` |
| `testacc-lint-fix` | Fix acceptance test linter findings |  |  | `K`, `PKG`, `SVC_DIR` |
| `testacc-short`<sup>D</sup> | Run acceptace tests with the -short flag |  |  | `ACCTEST_PARALLELISM`, `ACCTEST_TIMEOUT`, `GO_VER`, `K`, `PKG`, `PKG_NAME`, `RUNARGS`, `TEST_COUNT`, `TESTARGS` |
| `testacc-tflint` | Acceptance Test Linting / tflint | ✔️ |  | `K`, `PKG`, `SVC_DIR` |
| `testacc-tflint-dir` | Run `tflint` on Terraform acceptance test directories | ✔️ |  | `K`, `PKG`, `SVC_DIR` |
| `testacc-tflint-dir-fix` | Fix `tflint` issues in Terraform acceptance test directories | ✔️ |  | `K`, `PKG`, `SVC_DIR` |
| `testacc-tflint-embedded` | Run `tflint` on embedded Terraform configurations | ✔️ |  | `K`, `PKG`, `SVC_DIR` |
| `tfproviderdocs`<sup>D</sup> | Provider Checks / tfproviderdocs | ✔️ |  |  |
| `tfsdk2fw`<sup>D</sup> | Install tfsdk2fw |  |  | `GO_VER` |
| `tools`<sup>D</sup> | Install tools |  |  | `GO_VER` |
| `ts`<sup>M</sup> | Alias to `testacc-short` |  |  |  |
| `website`<sup>M</sup> | Run all CI website checks | ✔️ |  |  |
| `website-link-check` | Check website links |  | ✔️ |  |
| `website-link-check-ghrc` | Check website links with ghrc |  | ✔️ |  |
| `website-link-check-markdown` | Website Checks / markdown-link-check-a-z-markdown | ✔️ |  |  |
| `website-link-check-md` | Website Checks / markdown-link-check-md | ✔️ |  |  |
| `website-lint` | Lint website files |  | ✔️ |  |
| `website-lint-fix` | Fix website linter findings |  | ✔️ |  |
| `website-markdown-lint` | Website Checks / markdown-lint | ✔️ |  |  |
| `website-misspell` | Website Checks / misspell | ✔️ |  |  |
| `website-terrafmt` | Website Checks / terrafmt | ✔️ |  |  |
| `website-tflint` | Website Checks / tflint | ✔️ |  |  |
| `yamllint` | `YAML` Linting / yamllint | ✔️ |  |  |
# Naming Conventions for the AWS Provider

## Service Identifier

In the AWS Provider, a service identifier should consistently identify an AWS service from code to documentation to provider used by a practitioner. Prominent places you will see service identifiers:

* The package name (e.g., `internal/service/<serviceidentifier>`)
* In resource and data source names (e.g., `aws_<serviceidentifier>_thing`)
* Documentation file names (e.g., `website/docs/r/<serviceidentifier>_thing`)

Typically, choosing the AWS Provider identifier for a service is simple. AWS consistently uses one name and we use that name as the identifier. However, some services are not simple. To provide consistency, and to help contributors and practitioners know what to expect, we provide this rule for defining a service identifier:

### Rule

1. Determine the service package name for [AWS Go SDK v2](https://pkg.go.dev/github.com/aws/aws-sdk-go-v2).
2. Determine the [AWS CLI v2](https://awscli.amazonaws.com/v2/documentation/api/latest/index.html) _command_ corresponding to the service (i.e., the word following `aws` in CLI commands; e.g., for `aws sts get-caller-identity`, `sts` is the _command_, `get-caller-identity` is the _subcommand_).
3. If the SDK and CLI agree, use that. If the service only exists in one, use that.
4. If they differ, use the shorter of the two.
5. Use lowercase letters and do not include any underscores (`_`).

### How Well Is It Followed?

With 156+ services having some level of implementation, the following is a summary of how well this rule is currently followed.

For AWS provider service package names, only five packages violate this rule: `appautoscaling` should be `applicationautoscaling`, `codedeploy` should be `deploy`, `elasticsearch` should be `es`, `cloudwatchlogs` should be `logs`, and `simpledb` should be `sdb`.

For the service identifiers used in resource and data source configuration names (e.g., `aws_acmpca_certificate_authority`), 32 wholly or partially violate the rule.

* EC2, ELB, ELBv2, and RDS have legacy but heavily used resources and data sources that do not or inconsistently use service identifiers.
* The remaining 28 services violate the rule in a consistent way: `appautoscaling` should be `applicationautoscaling`, `codedeploy` should be `deploy`, `elasticsearch` should be `es`, `cloudwatch_log` should be `logs`, `simpledb` should be `sdb`, `prometheus` should be `amp`, `api_gateway` should be `apigateway`, `cloudcontrolapi` should be `cloudcontrol`, `cognito_identity` should be `cognitoidentity`, `cognito` should be `cognitoidp`, `config` should be `configservice`, `dx` should be `directconnect`, `directory_service` should be `ds`, `elastic_beanstalk` should be `elasticbeanstalk`, `cloudwatch_event` should be `events`, `kinesis_firehose` should be `firehose`, `msk` should be `kafka`, `mskconnect` should be `kafkaconnect`, `kinesis_analytics` should be `kinesisanalytics`, `kinesis_video` should be `kinesisvideo`, `lex` should be `lexmodels`, `media_convert` should be `mediaconvert`, `media_package` should be `mediapackage`, `media_store` should be `mediastore`, `route53_resolver` should be `route53resolver`, relevant `s3` should be `s3control`, `serverlessapplicationrepository` should be `serverlessrepo`, and `service_discovery` should be `servicediscovery`.

## Packages

Package names are not seen or used by practitioners. However, they should still be carefully considered.

### Rule

1. For service packages (i.e., packages under `internal/service`), use the AWS Provider [service identifier](#service-identifier) as the package name.
2. For other packages, use a short name for the package. Common Go lengths are 3-9 characters.
3. Use a descriptive name. The name should capture the key purpose of the package.
4. Use lowercase letters and do not include any underscores (`_`).
5. Avoid useless names like `helper`. These names convey zero information. Everything in the AWS Provider is helping something or someone do something so the name `helper` doesn't narrow down the purpose of the package within the codebase.
6. Use a name that is not too narrow or too broad as Go packages should not be too big or too small. Tiny packages can be combined using a broader name encompassing both. For example, `verify` is a good name because it tells you _what_ the package does and allows a broad set of validation, comparison, and checking functionality.

## Resources and Data Sources

When creating a new resource or data source, it is important to get names right. Once practitioners rely on names, we can only change them through breaking changes. If you are unsure about what to call a resource or data source, discuss it with the community and maintainers.

### Rule

1. Follow the [AWS SDK for Go v2](https://pkg.go.dev/github.com/aws/aws-sdk-go-v2). Almost always, the API operations make determining the name simple. For example, the [Amazon CloudWatch Evidently](https://pkg.go.dev/github.com/aws/aws-sdk-go-v2/service/evidently) service includes `CreateExperiment`, `GetExperiment`, `UpdateExperiment`, and `DeleteExperiment`. Thus, the resource (or data source) name is "Experiment."
2. Give a resource its Terraform configuration (i.e., HCL) name (e.g., `aws_imagebuilder_image_pipeline`) by joining these three parts with underscores:
    * `aws` prefix
    * [Service identifier](#service-identifier) (service identifiers do not include underscores), all lowercase (e.g., `imagebuilder`)
    * Resource (or data source) name in snake case (spaces replaced with underscores, if any), all lowercase (e.g., `image_pipeline`)
3. Name the main resource function `Resource<ResourceName>()`, with the resource name in [Mixed Caps](#mixed-caps). Do not include the service name or identifier. For example, define `ResourceImagePipeline()` in a file called `internal/service/imagebuilder/image_pipeline.go`.
4. Similarly, name the main data source function `DataSource<ResourceName>()`, with the data source name in [Mixed Caps](#mixed-caps). Do not include the service name or identifier. For example, define `DataSourceImagePipeline()` in a file called `internal/service/imagebuilder/image_pipeline_data_source.go`.

## Files

File names should follow Go and Markdown conventions with these additional points.

### Resource and Data Source Documentation Rule

1. Resource markdown goes in the `website/docs/r` directory. Data source markdown goes in the `website/docs/d` directory.
2. Use the [service identifier](#service-identifier) and resource or data source name, separated by an underscore (`_`).
3. All letters are lowercase.
4. Use `.html.markdown` as the extension.
5. Do not include "aws" in the name.

A correct example is `accessanalyzer_analyzer.html.markdown`. An incorrect example is `service_discovery_instance.html.markdown` because the [service identifier](#service-identifier) should not include an underscore.

### Go File Rule

1. Resource and data source files are in the `internal/service/<service>` directory.
2. Do not include the service as part of the file name.
3. Data sources should include `_data_source` after the data source name (e.g., `application_data_source.go`).
4. Put unit and acceptance tests in a file ending with `_test.go` (e.g., `custom_domain_association_test.go`).
5. Use snake case for multiword names (i.e., all letters are lowercase, words separated by underscores).
6. Use the `.go` extension.
7. Idiomatic names for common non-resource, non-data-source files include `consts.go` (service-wide constants), `find.go` (finders), `flex.go` (FLatteners and EXpanders), `generate.go` (directives for code generation), `id.go` (ID creators and parsers), `status.go` (status functions), `sweep.go` (sweepers), `tags_gen.go` (generated tag code), `validate.go` (validators), and `wait.go` (waiters).

## Mixed Caps

!!! note
    Mixed Caps is different than camel case, Pascal case, or snake case!

Idiomatic Go uses [_Mixed Caps_](https://go.dev/wiki/CodeReviewComments#initialisms) for multiword names in code. Mixed caps is similar to camel case except **initialisms and abbreviations in mixed caps should be the correct, human-readable case**, such as `VPCEndpoint` not `VpcEndpoint`. After all, names in code _are for humans_.

An acronym such as "VPC" should either be all capitalized ("VPC") or all lowercase ("vpc"), never "Vpc" or "vPC." Similarly, in mixedCaps, "DynamoDB" should either be "DynamoDB" or "dynamoDB", depending on whether an initial cap is needed or not, and never "dynamoDb" or "DynamoDb."

For more details on capitalizations we enforce with CI Semgrep tests, see the [Caps List](https://github.com/hashicorp/terraform-provider-aws/blob/main/names/caps.md).

### Rule

1. Use _mixedCaps_ for names (such as for functions, types, methods, variables, and constants) in the Terraform AWS Provider Go code.

## Functions

In general, follow Go best practices for good function naming. This rule is for functions defined outside of the _test_ context (i.e., not in a file ending with `_test.go`). For test functions, see [Test Support Functions](#test-support-functions) or [Acceptance Test Configurations](#acceptance-test-configurations) below.

### Rule

1. Only export functions (capitalize) when necessary, i.e., when the function is used outside the current package, including in the `_test` (`.test`) package.
2. Use [MixedCaps](#mixed-caps) (exported) or [mixedCaps](#mixed-caps) (not exported). Do not use underscores for multiwords.
3. Do not include the service name in the function name. (If functions are used outside the current package, the import package clarifies a function's origin. For example, the EC2 function `FindVPCEndpointByID()` is used outside the `internal/service/ec2` package but where it is used, the call is `tfec2.FindVPCEndpointByID()`.)
4. For CRUD functions for resources, use this format: `resource<ResourceName><CRUDFunction>`. For example, `resourceImageRecipeUpdate()`, `resourceBaiduChannelRead()`.
5. For data sources, for Read functions, use this format: `dataSource<DataSourceName>Read`. For example, `dataSourceBrokerRead()`, `dataSourceEngineVersionRead()`.
6. To improve readability, consider including the resource name in helper function names that pertain only to that resource. For example, for an expander function for an "App" resource and a "Campaign Hook" expander, use `expandAppCampaignHook()`.
7. Do not include "AWS" or "Aws" in the name.

## Variables and Constants

In general, follow Go best practices for good variable and constant naming.

### Rule

1. Only export variables and constants (capitalize) when necessary, i.e., the variable or constant is used outside the current package, including in the `_test` (`.test`) package.
2. Use [MixedCaps](#mixed-caps) (exported) or [mixedCaps](#mixed-caps) (not exported). Do not use underscores for multiwords.
3. Do not include the service name in variable or constant names. (If variables or constants are used outside the current package, the import package clarifies its origin. For example, IAM's `PropagationTimeout` is widely used outside of IAM but each instance is through the package import alias, `tfiam.PropagationTimeout`. "IAM" is unnecessary in the constant name.)
4. To improve readability, consider including the resource name in variable and constant names that pertain only to that resource. For example, for a string constant for a "Role" resource and a "not found" status, use `roleStatusNotFound` or `RoleStatusNotFound`, if used outside the service's package.
5. Do not include "AWS" or "Aws" in the name.

!!! note
    Give priority to constants from the AWS SDK for Go rather than defining new constants for the same values.

## Acceptance and Unit Tests

With about 6000 acceptance and unit tests, following these naming conventions is essential to organization and (human) context switching between services.

There are three types of tests in the AWS Provider: (regular) acceptance tests, serialized acceptance tests, and unit tests. All are functions that take a variable of type `*testing.T`. Acceptance tests and unit tests have exported (i.e., capitalized) names while serialized tests do not. Serialized tests are called by another exported acceptance test, often ending with `_serial`. The majority of tests in the AWS provider are acceptance tests.

### Acceptance Test Rule

Acceptance test names have a minimum of two (e.g., `TestAccBackupPlan_tags`) or a maximum of three (e.g., `TestAccDynamoDBTable_Replica_multiple`) parts, joined with underscores:

1. First part: All have a _prefix_ (i.e., `TestAcc`), _service name_ (e.g., `Backup`, `DynamoDB`), and _resource name_ (e.g., `Plan`, `Table`), [Mixed Caps](#mixed-caps) without underscores between. Do not include "AWS" or "Aws" in the name.
2. Middle part (Optional): _Test group_ (e.g., `Replica`), uppercase, [Mixed Caps](#mixed-caps). Consider a metaphor where tests are chapters in a book. If it is helpful, tests can be grouped together like chapters in a book that are sometimes grouped into parts or sections of the book.
3. Last part: _Test identifier_ (e.g., `basic`, `tags`, or `multiple`), lowercase, [mixedCaps](#mixed-caps)). The identifier should make the test's purpose clear but be concise. For example, the identifier `conflictsWithCloudFrontDefaultCertificate` (41 characters) conveys no more information than `conflictDefaultCertificate` (26 characters), since "CloudFront" is implied and "with" is _always_ implicit. Avoid words that convey no meaning or whose meaning is implied. For example, "with" (e.g., `_withTags`) is not needed because we imply the name is telling us what the test is _with_. `withTags` can be simplified to `tags`.

### Serialized Acceptance Test Rule

The names of serialized acceptance tests follow the regular [acceptance test name rule](#acceptance-test-rule) **_except_** for serialized acceptance test names:

1. Start with `testAcc` instead of `TestAcc`
2. Do not include the name of the service (e.g., a serialized acceptance test would be called `testAccApp_basic` not `testAccAmplifyApp_basic`).

### Unit Test Rule

Unit test names follow the same [rule](#acceptance-test-rule) as acceptance test names except for unit test names:

1. Start with `Test`, not `TestAcc`
2. Do not include the name of the service
3. Usually do not have any underscores
4. If they test a function, should include the function name (e.g., a unit test of `ExpandListener()` should be called `TestExpandListener()`)

## Test Support Functions

This rule is for functions defined in the _test_ context (i.e., in a file ending with `_test.go`) that do not return a string with Terraform configuration. For non-test functions, see [Functions](#functions) above. Or, see [Acceptance Test Configurations](#acceptance-test-configurations) below.

### Rule

1. Only export functions (capitalize) when necessary, i.e., when the function is used outside the current package. _This is very rare._
2. Use [MixedCaps](#mixed-caps) (exported) or [mixedCaps](#mixed-caps) (not exported). Do not use underscores for multiwords.
3. Do not include the service name in the function name. For example, `testAccCheckAMPWorkspaceExists()` should be named `testAccCheckWorkspaceExists()` instead, dropping the service name.
4. Several types of support functions occur commonly and should follow these patterns:
    * Destroy: `testAccCheck<Resource>Destroy`
    * Disappears: `testAccCheck<Resource>Disappears`
    * Exists: `testAccCheck<Resource>Exists`
    * Not Recreated: `testAccCheck<Resource>NotRecreated`
    * PreCheck: `testAccPreCheck` (often, only one PreCheck is needed per service so no resource name is needed)
    * Recreated: `testAccCheck<Resource>Recreated`
5. Do not include "AWS" or "Aws" in the name.

## Acceptance Test Configurations

This rule is for functions defined in the _test_ context (i.e., in a file ending with `_test.go`) that return a string with Terraform configuration. For test support functions, see [Test Support Functions](#test-support-functions) above. Or, for non-test functions, see [Functions](#functions) above.

!!! note
    This rule is not widely used currently. However, new functions and functions you change should follow it.

### Rule

1. Only export functions (capitalize) when necessary, i.e., when the function is used outside the current package. _This is very rare._
2. Use [MixedCaps](#mixed-caps) (exported) or [mixedCaps](#mixed-caps) (not exported). Do not use underscores for multiwords.
3. Do not include the service name in the function name.
4. Follow this pattern: `testAccConfig<Resource>_<TestGroup>_<configDescription>`
    * `_<TestGroup>` is optional. Refer to the [Acceptance Test Rule](#acceptance-test-rule) test group discussion.
    * Especially when an acceptance test only uses one configuration, the `<configDescription>` should be the same as the test identifier discussed in the [Acceptance Test Rule](#acceptance-test-rule).
5. Do not include "AWS" or "Aws" in the name.
# How We Prioritize

## Intro

### What this document is

This document describes how we handle prioritization of work from a variety of input sources. Our focus is always to deliver tangible value to the practitioner on a predictable and frequent schedule, and we feel it is important to be transparent in how we weigh input in order to deliver on this goal.

### What this document is not

Due to the variety of input sources, the scale of the provider, and resource constraints, it is impossible to give a hard number on how each of the factors outlined in this document is weighted. Instead, the goal of the document is to give a transparent, but generalized assessment of each of the sources of input so that the community has a better idea of why things are prioritized the way they are. Additional information may be found in the [FAQ](faq.md#how-do-you-decide-what-gets-merged-for-each-release).

## Prioritization

We prioritize work based on a number of factors, including community feedback, issue/PR reactions, as well as the source of the request. While community feedback is heavily weighted, there are times when other factors take precedence. By their nature, some factors are less visible to the community, and so are outlined here as a way to be as transparent as possible. Each of the sources of input is detailed below.

### Community

Our large community of practitioners is vocal and immensely productive in contributing to the provider codebase. Unfortunately, our current team capacity means that we are unable to give every issue or pull request the same level of attention. This means we need to prioritize the issues that provide the most value to the greatest number of practitioners.

We will always focus on the issues which have the most attention. The main rubric we have for assessing community wants is GitHub reactions. In addition to reactions, we look at comments, reactions to comments, and links to additional issues and PRs to help get a more holistic view of where the community stands. We try to ensure that for the issues where we have the most community support, we are responsive to that support and attempt to give timelines wherever possible.

### Customer

Another source of work that must be weighted is escalations around particular feature requests and bugs from HashiCorp and AWS customers. Escalations typically come via several routes:

- Customer Support
- Sales Engineering
- AWS Solutions Architects contacting us on behalf of their clients.

These reports flow into an internal board and are triaged weekly to determine whether the escalation request should be prioritized for an upcoming release or added to the backlog to monitor for additional community support. During triage, we verify whether a GitHub issue or PR exists for the request and will create one if it does not exist. In this way, these requests are visible to the community to some degree. An escalation coming from a customer does not necessarily guarantee that it will be prioritized over requests made by the community. Instead, we assess them based on the following rubric:

- Does the issue have considerable community support?
- Does the issue pertain to one of our [Core Services](core-services.md)?

By weighing these factors, we can make a call to determine whether, and how it is to be prioritized.

### Partner

AWS Service Teams and Partner representatives regularly contact us to discuss upcoming features or new services. This work is often done under an NDA, so usually needs to be done in private. Often the ask is to enable Terraform support or an upcoming feature or service.

As with customer escalations, a request from a partner does not necessarily mean that it will be prioritized over other efforts; capacity restraints require us to prioritize major releases or prefer offerings in line with our [core services](core-services.md).

### Internal

#### SDK/Core Updates

We endeavor to keep in step with all minor SDK releases, so these are automatically pulled in by our GitHub automation. Major releases normally include breaking changes and usually require us to bump the provider itself to a major version. We plan to make one major version change a year and try to avoid any more than that.

#### Technical Debt

We always include capacity for technical debt work in every iteration, but engineers are free to include minor tech debt work on their own recognizance. Larger items are discussed and prioritized in an internal meeting aimed at reviewing technical debt.

#### Adverse User Experience or Security Vulnerabilities

Issues with the provider that provide a poor user experience (bugs, crashes), or involve a threat to security are always prioritized for inclusion. The severity of these will determine how soon they are included for release.
# Provider Design

The Terraform AWS Provider follows the guidelines established in the [HashiCorp Provider Design Principles](https://www.terraform.io/plugin/hashicorp-provider-design-principles). That general documentation provides many high-level design points gleaned from years of experience with Terraform's design and implementation concepts. Sections below will expand on specific design details between that documentation and this provider, while others will capture other pertinent information that may not be covered there. Other pages of the contributing guide cover implementation details such as code, testing, and documentation specifics.

## API and SDK Boundary

The AWS provider implements support for the [AWS](https://aws.amazon.com/) service APIs using the [AWS Go SDK](https://aws.amazon.com/sdk-for-go/). The API and SDK limits extend to the provider. In general, SDK operations manage the lifecycle of AWS components, such as creating, describing, updating, and deleting a database. Operations do not usually handle functionality within those components, such as executing a query on a database. If you are interested in other APIs/SDKs, we invite you to view the many Terraform Providers available, as each has a community of domain expertise.

Some examples of functionality that is not expected in this provider:

* Raw HTTP(S) handling. See the [Terraform HTTP Provider](https://registry.terraform.io/providers/hashicorp/http/latest) and [Terraform TLS Provider](https://registry.terraform.io/providers/hashicorp/tls/latest) instead.
* Kubernetes resource management beyond the EKS service APIs. See the [Terraform Kubernetes Provider](https://registry.terraform.io/providers/hashicorp/kubernetes/latest) instead.
* Active Directory or other protocol clients. See the [Terraform Active Directory Provider](https://registry.terraform.io/providers/hashicorp/ad/latest/docs) and other available providers instead.
* Functionality that requires additional software beyond the Terraform AWS Provider to be installed on the host executing Terraform. This currently includes the AWS CLI. See the [Terraform External Provider](https://registry.terraform.io/providers/hashicorp/external/latest) and other available providers instead.

## Infrastructure as Code Suitability

The provider maintainers' design goal is to cover as much of the AWS API as pragmatically possible. However, not every aspect of the API is compatible with an infrastructure-as-code (IaC) conception. Specifically: IaC is best suited for [immutable rather than mutable infrastructure](https://www.hashicorp.com/resources/what-is-mutable-vs-immutable-infrastructure) -- i.e. for resources with a single desired state described in its entirety, as opposed to resources defined via a dynamic process.

If such limits affect you, we recommend that you open an AWS Support case and encourage others to do the same. Request that AWS components be made more self-contained and compatible with IaC. These AWS Support cases can also yield insights into the AWS service and API that are not well documented.

## Resource Type Considerations

Terraform resources work best as the smallest infrastructure blocks on which practitioners can build more complex configurations and abstractions, such as [Terraform Modules](https://www.terraform.io/language/modules). The general heuristic guiding when to implement a new Terraform resource for an aspect of AWS is whether the AWS service API provides create, read, update, and delete (CRUD) operations. However, not all AWS service API functionality falls cleanly into CRUD lifecycle management. In these situations, there is extra consideration necessary for properly mapping API operations to Terraform resources.

This section highlights design patterns when considering an implementation within a singular Terraform resource or as separate Terraform resources.

Please note: the overall design and implementation across all AWS functionality is federated: individual services may implement concepts and use terminology differently. As such, this guide is not exhaustive. The aim is to provide general concepts and basic terminology that point contributors in the right direction, especially in understanding previous implementations.

### Authorization and Acceptance Resources

Some AWS services use an authorization-acceptance model for cross-account associations or access. Examples include:

* Direct Connect Association Proposals
* GuardDuty Member Invitations
* RAM Resource Share Associations
* Route 53 VPC Associations
* Security Hub Member Invitations

Depending on the API and components, AWS uses two basic ways of creating cross-region and cross-account associations. One way is to generate an invitation (or proposal) identifier from one AWS account to another. Then in the other AWS account, that identifier is used to accept the invitation. The second way is configuring a reference to another AWS account identifier. These may not require explicit acceptance on the receiving account to finish creating the association or begin working.

To model creating an association using an invitation or proposal, follow these guidelines.

* Follow the naming in the AWS service API to determine whether to use the term "invitation" or "proposal."
* For the originating account, create an "invitation" or "proposal" resource. Make sure that the AWS service API has operations for creating and reading invitations.
* For the responding account, create an "accepter" resource. Ensure that the API has operations for accepting, reading, and rejecting invitations in the responding account. Map the operations as follows:
    * Create: Accepts the invitation.
    * Read: Reads the invitation to determine its status. Note that in some APIs, invitations expire and disappear, complicating associations. If a resource does not find an invitation, the developer should implement a fallback to read the API resource associated with the invitation/proposal.
    * Delete: Rejects or otherwise deletes the invitation.

To model the second type of association, implicit associations, create an "association" resource and, optionally, an "authorization" resource. Map create, read, and delete to the corresponding operations in the AWS service API.

### Cross-Service Functionality

Many AWS service APIs build on top of other AWS services. Some examples of these include:

* EKS Node Groups managing Auto Scaling Groups
* Lambda Functions managing EC2 ENIs
* Transfer Servers managing EC2 VPC Endpoints

Some cross-service API implementations lack the management or description capabilities of the other service. The lack can make the Terraform resource implementation seem incomplete or unsuccessful in end-to-end configurations. Given the overall “resources should represent a single API object” goal from the [HashiCorp Provider Design Principles](https://www.terraform.io/plugin/hashicorp-provider-design-principles), a resource must only communicate with a single AWS service API. As such, maintainers will not approve cross-service resources.

The rationale behind this design decision includes the following:

* Unexpected IAM permissions being necessary for the resource. In high-security environments, all the service permissions may not be available or acceptable.
* Unexpected services generating CloudTrail logs for the resource.
* Needing extra and unexpected API endpoints configuration for organizations using custom endpoints, such as VPC endpoints.
* Unexpected changes to the AWS service internals for the cross-service implementations. Given that this functionality is not part of the primary service API, these details can change over time and may not be considered as a breaking change by the service team for an API upgrade.

A poignant real-world example of the last point involved a Lambda resource. The resource helped clean up extra resources (ENIs) due to a common misconfiguration. Practitioners found the functionality helpful since the issue was hard to diagnose. Years later, AWS updated the Lambda API. Immediately, practitioners reported that Terraform executions were failing. Downgrading the provider was not possible since many configurations depended on recent releases. For environments running many versions behind, forcing an upgrade with the fix would likely cause unrelated and unexpected changes. In the end, HashiCorp and AWS performed a large-scale outreach to help upgrade and fix the misconfigurations. Provider maintainers and practitioners lost considerable time.

### Data Sources

A separate class of Terraform resource types are [data sources](https://www.terraform.io/docs/language/data-sources/). These are typically intended as a configuration method to lookup or fetch data in a read-only manner. Data sources should not have side effects on the remote system.

When discussing data sources, they are typically classified by the intended number of return objects or data. Singular data sources represent a one-to-one lookup or data operation. Plural data sources represent a one-to-many operation.

#### Plural Data Sources

These data sources are intended to return zero, one, or many results, usually associated with a managed resource type. Typically results are a set unless ordering guarantees are provided by the remote system. These should be named with a plural suffix (e.g., `s` or `es`) and should not include any specific attribute in the naming (e.g., prefer `aws_ec2_transit_gateways` instead of `aws_ec2_transit_gateway_ids`).

#### Singular Data Sources

These data sources are intended to return one result or an error. These should not include any specific attribute in the naming (e.g., prefer `aws_ec2_transit_gateway` instead of `aws_ec2_transit_gateway_id`).

### IAM Resource-Based Policy Resources

For some AWS components, the AWS API allows specifying an [IAM resource-based policy](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_identity-vs-resource.html), the IAM policy to associate with a component. Some examples include:

* ECR Repository Policies
* EFS File System Policies
* SNS Topic Policies

Provider developers should implement this capability in a new resource rather than adding it to the associated resource. Reasons for this include:

* Many of the policies must include the ARN of the resource. Working around this requirement with custom difference handling within a self-contained resource is unnecessarily cumbersome.
* Some policies involving multiple resources need to cross-reference each other's ARNs. Without a separate resource, this introduces a configuration cycle.
* Splitting the resources allows operators to logically split their configurations into purely operational and security boundaries. This allows environments to have distinct practitioner roles and permissions for IAM versus infrastructure changes.

One rare exception to this guideline is where the policy is _required_ during resource creation.

### Managing Resource Running State

The AWS API provides the ability to start, stop, enable, or disable some AWS components. Some examples include:

* Batch Job Queues
* CloudFront Distributions
* RDS DB Event Subscriptions

In this situation, provider developers should implement this ability within the resource instead of creating a separate resource. Since a practitioner cannot practically manage interaction with a resource's states in Terraform's declarative configuration, developers should implement the state management in the resource. This design provides consistency and future-proofing even where updating a resource in the current API is not problematic.

### Task Execution and Waiter Resources

Some AWS operations are asynchronous. Terraform requests that AWS perform a task. Initially, AWS only notifies Terraform that it received the request. Terraform then requests the status while awaiting completion. Examples of this include:

* ACM Certificate validation
* EC2 AMI copying
* RDS DB Cluster Snapshot management

In this situation, provider developers should create a separate resource representing the task, assuming that the AWS service API provides operations to start the task and read its status. Adding the task functionality to the parent resource muddies its infrastructure-management purpose. The maintainers prefer this approach even though there is some duplication of an existing resource. For example, the provider has a resource for copying an EC2 AMI in addition to the EC2 AMI resource itself. This modularity allows practitioners to manage the result of the task resource with another resource.

For a related consideration, see the [Managing Resource Running State section](#managing-resource-running-state).

### Versioned Resources

AWS supports having multiple versions of some components. Examples of this include:

* ECS Task Definitions
* Lambda Functions
* Secrets Manager Secrets

In general, provider developers should create a separate resource to represent a single version. For example, the provider has both the `aws_secretsmanager_secret` and `aws_secretsmanager_secret_version` resources. However, in some cases, developers should handle versioning in the main resource.

In deciding when to create a separate resource, follow these guidelines:

* If AWS necessarily creates a version when you make a new AWS component, include version handling in the same Terraform resource. Creating an AWS component with one Terraform resource and later using a different resource for updates is confusing.
* If the AWS service API allows deleting versions and practitioners want to delete versions, provider developers should implement a separate version resource.
* If the API only supports publishing new versions, either method is acceptable, however most current implementations are self-contained. Terraform's current configuration language does not natively support triggering resource updates or recreation across resources without a state value change. This can make the implementation more difficult for practitioners without special resource and configuration workarounds, such as a `triggers` attribute. If this changes in the future, then this guidance may be updated towards separate resources, following the [Task Execution and Waiter Resources](#task-execution-and-waiter-resources) guidance.

## Other Considerations

### AWS Credential Exfiltration

In the interest of security, the maintainers will not approve data sources that provide the ability to reference or export the AWS credentials of the running provider. There are valid use cases for this information, such as executing AWS CLI calls as part of the same Terraform configuration. However, this mechanism may allow credentials to be discovered and used outside of Terraform. Some specific concerns include:

* The values may be visible in Terraform user interface output or logging, allowing anyone with a user interface or log access to see the credentials.
* The values are currently stored in plaintext in the Terraform state, allowing anyone with access to the state file or another Terraform configuration that references the state access to the credentials.
* Any new related functionality, while opt-in to implement, is also opt-in to prevent via security controls or policies. Adopting a weaker default security posture requires advance notice and prevents organizations that implement those controls from updating to a version with any such functionality.
# Raising a Pull Request

1. [Fork the GitHub repository](https://help.github.com/en/articles/fork-a-repo) allowing you to make the changes in your own copy of the repository.

1. Create a branch using the following naming prefixes:

    - f = feature
    - b = bug fix
    - d = documentation
    - t = tests
    - td = technical debt
    - v = dependencies ("vendoring" previously)

    Some indicative example branch names would be `f-aws_emr_instance_group-refactor` or `td-staticcheck-st1008`

1. Make the changes you would like to include in the provider, add new tests as required, and make sure that all relevant existing tests are passing.

1. [Create a pull request](https://help.github.com/en/articles/creating-a-pull-request-from-a-fork). Please ensure (if possible) that the 'Allow edits from maintainers' checkbox is checked. This will allow the maintainers to make changes and merge the PR without requiring action from the contributor.
   You are welcome to submit your pull request for commentary or review before
   it is fully completed by creating a [draft pull request](https://help.github.com/en/articles/about-pull-requests#draft-pull-requests).
   Please include specific questions or items you'd like feedback on.

1. Create a changelog entry following the process outlined [here](changelog-process.md)

1. Once you believe your pull request is ready to be reviewed, ensure the
   pull request is not a draft pull request by [marking it ready for review](https://help.github.com/en/articles/changing-the-stage-of-a-pull-request)
   or removing `[WIP]` from the pull request title if necessary, and a
   maintainer will review it. Follow [the checklists below](#resource-contribution-guidelines)
   to help ensure that your contribution can be easily reviewed and potentially
   merged.

1. One of Terraform's provider team members will look over your contribution and
   either approve it or provide comments letting you know if there is anything
   left to do. We'll try to give you the opportunity to make the required changes yourself, but in some cases, we may perform the changes ourselves if it makes sense to (minor changes, or for urgent issues).  We do our best to keep up with the volume of PRs waiting for review, but it may take some time depending on the complexity of the work.

1. Once all outstanding comments and checklist items have been addressed, your
   contribution will be merged! Merged PRs will be included in the next
   Terraform release.

1. In some cases, we might decide that a PR should be closed without merging.
   We'll make sure to provide clear reasoning when this happens.

### Go Coding Style

All Go code is automatically checked for compliance with various linters, such as `gofmt`. These tools can be installed using the `GNUMakefile` in this repository.

```console
make tools
```

Check your code with the linters:

```console
make lint
```

We use [Semgrep](https://semgrep.dev/docs/) to check for other code standards.
This can be run directly on the command line, i.e.,

```console
semgrep
```

or it can be run using Docker via the Makefile, i.e.,

```console
make semgrep
```

`gofmt` will also fix many simple formatting issues for you. The Makefile includes a target for this:

```console
make fmt
```

The import statement in a Go file follows these rules (see [#15903](https://github.com/hashicorp/terraform-provider-aws/issues/15903)):

1. Import declarations are grouped into a maximum of three groups in the following order:
    - Standard packages (also called short import path or built-in packages)
    - Third-party packages (also called long import path packages)
    - Local packages
1. Groups are separated by a single blank line
1. Packages within each group are alphabetized

Check your imports:

```console
make import-lint
```

For greater detail, the following Go language resources provide common coding preferences that may be referenced during review, if not automatically handled by the project's linting tools.

- [Effective Go](https://golang.org/doc/effective_go.html)
- [Go Code Review Comments](https://github.com/golang/go/wiki/CodeReviewComments)

### Resource Contribution Guidelines

The following resource checks need to be addressed before your contribution can be merged. The exclusion of any applicable check may result in a delayed time to merge. Some of these are not handled by the automated code testing that occurs during submission, so reviewers (even those outside the maintainers) are encouraged to reach out to contributors about any issues to save time.

This Contribution Guide also includes separate sections on topics such as [Error Handling](error-handling.md), which also applies to contributions.

- __Passes Testing__: All code and documentation changes must pass unit testing, code linting, and website link testing. Resource code changes must pass all acceptance testing for the resource.
- __Avoids API Calls Across Account, Region, and Service Boundaries__: Resources should not implement cross-account, cross-region, or cross-service API calls.
- __Does Not Set Optional or Required for Non-Configurable Attributes__: Resource schema definitions for read-only attributes must not include `Optional: true` or `Required: true`.
- __Avoids retry.RetryContext() without retry.RetryableError()__: Resource logic should only implement [`retry.Retry()`](https://godoc.org/github.com/hashicorp/terraform/helper/retry#Retry) if there is a retryable condition (e.g., `return retry.RetryableError(err)`).
- __Avoids Reusing Resource Read Function in Data Source Read Function__: Data sources should fully implement their own resource `Read` functionality.
- __Avoids Reading Schema Structure in Resource Code__: The resource `Schema` should not be read in resource `Create`/`Read`/`Update`/`Delete` functions to perform looping or otherwise complex attribute logic. Use [`d.Get()`](https://godoc.org/github.com/hashicorp/terraform/helper/schema#ResourceData.Get) and [`d.Set()`](https://godoc.org/github.com/hashicorp/terraform/helper/schema#ResourceData.Set) directly with individual attributes instead.
- __Avoids ResourceData.GetOkExists()__: Resource logic should avoid using [`ResourceData.GetOkExists()`](https://godoc.org/github.com/hashicorp/terraform/helper/schema#ResourceData.GetOkExists) as its expected functionality is not guaranteed in all scenarios.
- __Calls Read After Create and Update__: Except where API eventual consistency prohibits immediate reading of resources or updated attributes,  resource `Create` and `Update` functions should return the resource `Read` function.
- __Implements Immediate Resource ID Set During Create__: Immediately after calling the API creation function, the resource ID should be set with [`d.SetId()`](https://godoc.org/github.com/hashicorp/terraform/helper/schema#ResourceData.SetId) before other API operations or returning the `Read` function.
- __Implements Attribute Refreshes During Read__: All attributes available in the API should have [`d.Set()`](https://godoc.org/github.com/hashicorp/terraform/helper/schema#ResourceData.Set) called their values in the Terraform state during the `Read` function.
- __Performs Error Checks with Non-Primitive Attribute Refreshes__: When using [`d.Set()`](https://godoc.org/github.com/hashicorp/terraform/helper/schema#ResourceData.Set) with non-primitive types (`schema.TypeList`, `schema.TypeSet`, or `schema.TypeMap`), perform error checking to [prevent issues where the code is not properly able to refresh the Terraform state](https://www.terraform.io/plugin/sdkv2/best-practices/detecting-drift#error-checking-aggregate-types).
- __Implements Import Acceptance Testing and Documentation__: Support for resource import (`Importer` in resource schema) must include `ImportState` acceptance testing (see also the [Acceptance Testing Guidelines](running-and-writing-acceptance-tests.md)) and `## Import` section in resource documentation.
- __Implements Customizable Timeouts Documentation__: Support for customizable timeouts (`Timeouts` in resource schema) must include `## Timeouts` section in resource documentation.
- __Implements State Migration When Adding New Virtual Attribute__: For new "virtual" attributes (those only in Terraform and not in the API), the schema should implement [State Migration](https://www.terraform.io/plugin/sdkv2/resources#state-migrations) to prevent differences for existing configurations that upgrade.
- __Uses AWS Go SDK Constants__: Many AWS services provide string constants for value enumerations, error codes, and status types. See also the "Constants" sections under each of the service packages in the [AWS Go SDK documentation](https://docs.aws.amazon.com/sdk-for-go/api/).
- __Uses AWS Go SDK Pointer Conversion Functions__: Many APIs return pointer types and these functions return the zero value for the type if the pointer is `nil`. This prevents potential panics from unchecked `*` pointer dereferences and can eliminate boilerplate `nil` checking in many cases. See also the [`aws` package in the AWS Go SDK documentation](https://docs.aws.amazon.com/sdk-for-go/api/aws/).
- __Uses AWS Go SDK Types__: Use available SDK structs instead of implementing custom types with indirection.
- __Uses Existing Validation Functions__: Schema definitions including `ValidateFunc` for attribute validation should use available [Terraform `helper/validation` package](https://godoc.org/github.com/hashicorp/terraform/helper/validation) functions. `All()`/`Any()` can be used for combining multiple validation function behaviors.
- __Uses tfresource.TimedOut() with retry.Retry()__: Resource logic implementing [`retry.Retry()`](https://godoc.org/github.com/hashicorp/terraform/helper/retry#Retry) should error check with [`tfresource.TimedOut(err error)`](https://godoc.org/github.com/hashicorp/terraform-provider-aws/internal/tfresource#TimedOut) and potentially unset the error before returning the error. For example:

  ```go
  var output *kms.CreateKeyOutput
  err := retry.Retry(1*time.Minute, func() *retry.RetryError {
    var err error

    output, err = conn.CreateKey(input)

    /* ... */

    return nil
  })

  if tfresource.TimedOut(err) {
    output, err = conn.CreateKey(input)
  }

  if err != nil {
    return fmt.Errorf("creating KMS External Key: %s", err)
  }
  ```

- __Uses id.UniqueId()__: API fields for concurrency protection such as `CallerReference` and `IdempotencyToken` should use [`id.UniqueId()`](https://godoc.org/github.com/hashicorp/terraform/helper/resource#UniqueId). The implementation includes a monotonic counter which is safer for concurrent operations than solutions such as `time.Now()`.
- __Skips id Attribute__: The `id` attribute is implicit for all Terraform resources and does not need to be defined in the schema.

The below are style-based items that _may_ be noted during review and are recommended for simplicity, consistency, and quality assurance:

- __Implements arn Attribute__: APIs that return an ARN should implement `arn` as an attribute. Alternatively, the ARN can be synthesized using the AWS Go SDK [`arn.ARN`](https://docs.aws.amazon.com/sdk-for-go/api/aws/arn/#ARN) structure. For example:

  ```go
  // Direct Connect Virtual Interface ARN.
  // See https://docs.aws.amazon.com/directconnect/latest/UserGuide/security_iam_service-with-iam.html#security_iam_service-with-iam-id-based-policies-resources.
  arn := arn.ARN{
      Partition: meta.(*conns.AWSClient).Partition,
      Region:    meta.(*conns.AWSClient).Region,
      Service:   "directconnect",
      AccountID: meta.(*conns.AWSClient).AccountID,
      Resource:  fmt.Sprintf("dxvif/%s", d.Id()),
  }.String()
  d.Set("arn", arn)
  ```

  When the `arn` attribute is synthesized this way, add the resource to the [list](https://registry.terraform.io/providers/hashicorp/aws/latest/docs#skip_requesting_account_id) of those affected by the provider's `skip_requesting_account_id` attribute.

- __Implements Warning Logging With Resource State Removal__: If a resource is removed outside of Terraform (e.g., via a different tool, API, or web UI), `d.SetId("")` and `return nil` can be used in the resource `Read` function to trigger resource recreation. When this occurs, a warning log message should be printed beforehand: `log.Printf("[WARN] {SERVICE} {THING} (%s) not found, removing from state", d.Id())`
- __Uses American English for Attribute Naming__: For any ambiguity with attribute naming, prefer American English over British English. e.g., `color` without the British `u`.
- __Skips Timestamp Attributes__: Generally, creation and modification dates from the API should be omitted from the schema.
- __Uses Paginated AWS Go SDK Functions When Iterating Over a Collection of Objects__: When the API for listing a collection of objects provides a paginated function, use it instead of looping until the next page token is not set. For example, with the EC2 API, [`DescribeInstancesPages`](https://docs.aws.amazon.com/sdk-for-go/api/service/ec2/#EC2.DescribeInstancesPages) should be used instead of [`DescribeInstances`](https://docs.aws.amazon.com/sdk-for-go/api/service/ec2/#EC2.DescribeInstances) when more than one result is expected.
- __Adds Paginated Functions Missing from the AWS Go SDK to Internal Service Package__: If the AWS Go SDK does not define a paginated equivalent for a function to list a collection of objects, it should be added to a per-service internal package using the [`listpages` generator](https://github.com/hashicorp/terraform-provider-aws/blob/main/internal/generate/listpages/README.md). A support case should also be opened with AWS to have the paginated functions added to the AWS Go SDK.
# Documentation

This directory contains documentation for the [Terraform AWS Provider Contributor Guide](https://hashicorp.github.io/terraform-provider-aws/). Resource and data source documentation is located in the [`website`](../website/) directory and available in the [Terraform Registry](https://registry.terraform.io/providers/hashicorp/aws/latest/docs).

## Local Development

To serve the contributing guide locally, [`mkdocs`](https://www.mkdocs.org/user-guide/installation/) and the [`mkdocs-material`](https://github.com/squidfunk/mkdocs-material#quick-start) extension must be installed. Both require Python and `pip`.

```console
% pip3 install mkdocs
```

```console
% pip3 install mkdocs-material
```

Once installed, the documentation can be served from the root directory:

```console
% mkdocs serve
```
# Using Regular Expressions

Regular expressions are a powerful tool. However, they are also very expensive in terms of memory. Ensuring correct and useful functionality is the priority but we have a few tips to minimize impact without affecting capabilities.

* **Consider non-regular expressions options.** [`strings.Contains()`](https://pkg.go.dev/strings#Contains), [`strings.Replace()`](https://pkg.go.dev/strings#Replace), and [`strings.ReplaceAll()`](https://pkg.go.dev/strings#ReplaceAll) are dramatically faster and less memory intensive than regular expressions. If one of these will work equally well, use the non-regular expression option.
* **Order character classes consistently.** We use regular expression caching to reduce our memory footprint. This is more effective if character classes are consistently ordered. Since a character class is a set, order does not affect functionality. We have many equivalent regular expressions that only differ by character class order. Below is the order we recommend for consistency:
    1. Numeric range, _i.e._, digits (_e.g._, `0-9`)
    1. Uppercase alphabetic range (_e.g._, `A-Z`, `A-F`)
    1. Lowercase alphabetic range (_e.g._, `a-z`, `a-f`)
    1. Underscore (`_`)
    1. Everything else (except dash, `-`) in ASCII order: `\t\n\r !"#$%&()*+,./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ[\]^abcdefghijklmnopqrstuvwxyz{|}~`
    1. _Last_, dash (`-`)

        For example, consider the following expressions which are equivalent but vary character class ordering:

        ```go
        `[_a-zA-Z0-9-,.]` // wrong ordering
        `[0-9A-Za-z_,.-]` // correct
        ```

        ```go
        `[;a-z0-9]` // wrong ordering
        `[0-9a-z;]` // correct
        ```

* **Inside character classes, avoid unnecessary character escaping.** Go does not complain about extra character escaping but avoid it to improve cache performance. Inside a character class, _most_ characters do not need to be escaped, as Go assumes you mean the literal character.
    * These characters which normally have special meaning in regular expressions, _inside character classes_ do **not** need to be escaped: `$`, `(`, `)`, `*`, `+`, `.`, `?`, `^`, `{`, `|`, `}`.
    * Dash (`-`), when it is last in the character class or otherwise unambiguously not part of a range, does not need to be escaped. If in doubt, place the dash _last_ in the character class (_e.g._, `[a-c-]`) or escape the dash (_e.g._, `\-`).
    * Angle brackets (`[`, `]`) always need to be escaped in a character class.

        For example, consider the following expressions which are equivalent but include unnecessary character escapes:

        ```go
        `[\$\(\.\?\|]` // unnecessary escapes
        `[$(.?|]`      // correct
        ```

        ```go
        `[a-z\-0-9_A-Z\.]` // unnecessary escapes, wrong order
        `[0-9A-Za-z_.-]`   // correct
        ```

<!-- Add links to standard validators to use instead of custom -->
<!-- markdownlint-configure-file { "code-block-style": false } -->
# Adding Resource Filtering Support

AWS provides server-side filtering across many services and resources, which can be used when listing resources of that type, for example in the implementation of a data source.
See the [EC2 Listing and filtering your resources page](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Using_Filtering.html#Filtering_Resources_CLI) for information about how server-side filtering can be used with EC2 resources.

To determine if the supporting AWS API supports this functionality:

- Open the AWS Go SDK documentation for the service, e.g., for [`service/rds`](https://docs.aws.amazon.com/sdk-for-go/api/service/rds/). Note: there can be a delay between the AWS announcement and the updated AWS Go SDK documentation.
- Determine if the service API includes functionality for filtering resources (usually a `Filters` argument to a `DescribeThing` API call).

Implementing server-side filtering support for Terraform AWS Provider resources requires the following, each with its own section below:

- _Generated Service Filtering Code_: In the internal code generators (e.g., `internal/generate/namevaluesfilters`), implementation and customization of how a service handles filtering, which is standardized for the resources.
- _Resource Filtering Code Implementation_: In the resource's equivalent data source code (e.g., `internal/service/{servicename}/thing_data_source.go`), implementation of `filter` schema attribute, along with handling in the `Read` function.
- _Resource Filtering Documentation Implementation_: In the resource's equivalent data source documentation (e.g., `website/docs/d/service_thing.html.markdown`), addition of `filter` argument

## Adding Service to Filter Generating Code

This step is only necessary for the first implementation and may have been previously completed. If so, move on to the next section.

More details about this code generation can be found in the [namevaluesfilters documentation](https://github.com/hashicorp/terraform-provider-aws/blob/main/internal/generate/namevaluesfilters/README.md).

Add the AWS Go SDK service name (e.g., `rds`) to `sliceServiceNames` in `internal/generate/namevaluesfilters/generators/servicefilters/main.go`.

- Run `make gen` (`go generate ./...`) and ensure there are no errors via `make test` (`go test ./...`)

### Resource Filter Code Implementation

- In the resource's equivalent data source Go file (e.g., `internal/service/ec2/internet_gateway_data_source.go`), add the following Go import: `"github.com/hashicorp/terraform-provider-aws/internal/generate/namevaluesfilters"`
- In the resource schema, add `"filter": namevaluesfilters.Schema(),`
- Implement the logic to build the list of filters:

=== "Terraform Plugin SDK V2"
    ```go
    input := &ec2.DescribeInternetGatewaysInput{}

    // Filters based on attributes.
    filters := namevaluesfilters.New(map[string]string{
    	"internet-gateway-id": d.Get("internet_gateway_id").(string),
    })
    // Add filters based on key-value tags (N.B. Not applicable to all AWS services that support filtering)
    filters.Add(namevaluesfilters.EC2Tags(keyvaluetags.New(d.Get("tags").(map[string]interface{})).IgnoreAWS().IgnoreConfig(ignoreTagsConfig).Map()))
    // Add filters based on the custom filtering "filter" attribute.
    filters.Add(d.Get("filter").(*schema.Set))

    input.Filters = filters.EC2Filters()
    ```

## Resource Filtering Documentation Implementation

- In the resource's equivalent data source documentation (e.g., `website/docs/d/internet_gateway.html.markdown`), add the following to the arguments reference:

```markdown
* `filter` - (Optional) Custom filter block as described below.

More complex filters can be expressed using one or more `filter` sub-blocks, which take the following arguments:

* `name` - (Required) Name of the field to filter by, as defined by
  [the underlying AWS API](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeInternetGateways.html).

* `values` - (Required) Set of values that are accepted for the given field.
  An Internet Gateway will be selected if any one of the given values matches.
```
<!-- markdownlint-configure-file { "code-block-style": false } -->
# Adding Resource Name Generation Support

Terraform AWS Provider resources can use shared logic to support and test name generation, where the operator can choose between an expected naming value, a generated naming value with a prefix, or a fully generated name.

Implementing name generation requires modifying the following:

- _Resource Code_: In the resource code, add a `name_prefix` attribute, along with handling in the `Create` function.
- _Resource Acceptance Tests_: In the resource acceptance tests, add new acceptance test functions and configurations to exercise the naming logic.
- _Resource Documentation_: In the resource documentation, add the `name_prefix` argument and update the `name` argument description.

## Resource Code

- In the resource file (e.g., `internal/service/{service}/{thing}.go`), add the following import: `"github.com/hashicorp/terraform-provider-aws/internal/create"`.
- Inside the resource schema, add the new `name_prefix` attribute and adjust the `name` attribute to be `Optional`, `Computed`, and conflict with the `name_prefix` attribute. Be sure to keep any existing validation functions already present on the `name`.

=== "Terraform Plugin Framework (Preferred)"
    ```go
    "name": schema.StringAttribute{
        Optional: true
        Computed: true,
        PlanModifiers: []planmodifier.String{
            stringplanmodifier.UseStateForUnknown(),
            stringplanmodifier.RequiresReplace(),
        },
        Validators: append(
            stringvalidator.ExactlyOneOf(
                path.MatchRelative().AtParent().AtName("name"),
                path.MatchRelative().AtParent().AtName("name_prefix"),
            ),
        ),
    },
    "name_prefix": schema.StringAttribute{
        Optional:   true,
        Computed:   true,
        PlanModifiers: []planmodifier.String{
            stringplanmodifier.UseStateForUnknown(),
            stringplanmodifier.RequiresReplace(),
        },
    },
    ```

=== "Terraform Plugin SDK V2"
    ```go
    "name": {
      Type:          schema.TypeString,
      Optional:      true,
      Computed:      true,
      ForceNew:      true,
      ConflictsWith: []string{"name_prefix"},
    },
    "name_prefix": {
      Type:          schema.TypeString,
      Optional:      true,
      Computed:      true,
      ForceNew:      true,
      ConflictsWith: []string{"name"},
    },
    ```

- In the resource `Create` function, make use of the `create.Name()` function.

=== "Terraform Plugin Framework (Preferred)"
    ```go
    name := create.Name(plan.Name.ValueString(), plan.NamePrefix.ValueString())

    // ... in AWS Go SDK V2 Input types, etc. use aws.ToString(name)
    ```

=== "Terraform Plugin SDK V2"
    ```go
    name := create.Name(d.Get("name").(string), d.Get("name_prefix").(string))

    // ... in AWS Go SDK V2 Input types, etc. use aws.ToString(name)
    ```

- If the resource supports import, set both `name` and `name_prefix` in the resource `Read` function.

=== "Terraform Plugin Framework (Preferred)"
    ```go
    state.Name = flex.StringToFramework(ctx, resp.Name)
    state.NamePrefix = create.NamePrefixFromName(flex.StringToFramework(ctx, resp.Name))
    ```

=== "Terraform Plugin SDK V2"
    ```go
    d.Set("name", resp.Name)
    d.Set("name_prefix", create.NamePrefixFromName(aws.StringValue(resp.Name)))
    ```

## Resource Acceptance Tests

- In the resource test file (e.g., `internal/service/{service}/{thing}_test.go`), add the following import: `"github.com/hashicorp/terraform-provider-aws/internal/create"`.
- Implement two new tests named `_nameGenerated` and `_namePrefix` which verify the creation of the resource without `name` and `name_prefix` arguments, and with only the `name_prefix` argument, respectively.

```go
func TestAccServiceThing_nameGenerated(t *testing.T) {
  ctx := acctest.Context(t)
  var thing service.ServiceThing
  resourceName := "aws_service_thing.test"

  resource.ParallelTest(t, resource.TestCase{
    PreCheck:                 func() { acctest.PreCheck(ctx, t) },
    ErrorCheck:               acctest.ErrorCheck(t, names.ServiceServiceID),
    ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
    CheckDestroy:             testAccCheckThingDestroy(ctx),
    Steps: []resource.TestStep{
      {
        Config: testAccThingConfig_nameGenerated(),
        Check: resource.ComposeTestCheckFunc(
          testAccCheckThingExists(ctx, resourceName, &thing),
          acctest.CheckResourceAttrNameGenerated(resourceName, "name"),
          resource.TestCheckResourceAttr(resourceName, "name_prefix", id.UniqueIdPrefix),
        ),
      },
      // If the resource supports import:
      {
        ResourceName:      resourceName,
        ImportState:       true,
        ImportStateVerify: true,
      },
    },
  })
}

func TestAccServiceThing_namePrefix(t *testing.T) {
  ctx := acctest.Context(t)
  var thing service.ServiceThing
  resourceName := "aws_service_thing.test"

  resource.ParallelTest(t, resource.TestCase{
    PreCheck:                 func() { acctest.PreCheck(ctx, t) },
    ErrorCheck:               acctest.ErrorCheck(t, names.ServiceServiceID),
    ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
    CheckDestroy:             testAccCheckThingDestroy(ctx),
    Steps: []resource.TestStep{
      {
        Config: testAccThingConfig_namePrefix("tf-acc-test-prefix-"),
        Check: resource.ComposeTestCheckFunc(
          testAccCheckThingExists(ctx, resourceName, &thing),
          acctest.CheckResourceAttrNameFromPrefix(resourceName, "name", "tf-acc-test-prefix-"),
          resource.TestCheckResourceAttr(resourceName, "name_prefix", "tf-acc-test-prefix-"),
        ),
      },
      // If the resource supports import:
      {
        ResourceName:      resourceName,
        ImportState:       true,
        ImportStateVerify: true,
      },
    },
  })
}

func testAccThingConfig_nameGenerated() string {
  return fmt.Sprintf(`
resource "aws_service_thing" "test" {
  # ... other configuration ...
}
`)
}

func testAccThingConfig_namePrefix(namePrefix string) string {
  return fmt.Sprintf(`
resource "aws_service_thing" "test" {
  # ... other configuration ...

  name_prefix = %[1]q
}
`, namePrefix)
}
```

## Resource Documentation

- In the resource documentation (e.g., `website/docs/r/{service}_{thing}.html.markdown`), add the following to the arguments reference.

```markdown
* `name_prefix` - (Optional) Creates a unique name beginning with the specified prefix. Conflicts with `name`.
```

- Adjust the existing `name` argument description to ensure it is denoted as `Optional`, mention that it can be generated and that it conflicts with `name_prefix`.

```markdown
* `name` - (Optional) Name of the thing. If omitted, Terraform will assign a random, unique name. Conflicts with `name_prefix`.
```
<!-- markdownlint-configure-file { "code-block-style": false } -->
# Adding Resource Tagging Support

AWS provides key-value metadata across many services and resources, which can be used for a variety of use cases including billing, ownership, and more. See the [AWS Tagging Strategy page](https://aws.amazon.com/answers/account-management/aws-tagging-strategies/) for more information about tagging at a high level.

The Terraform AWS Provider supports default tags configured on the provider in addition to tags configured on the resource.
Implementing tagging support for Terraform AWS Provider resources requires the following, each with its own section below:

- _Generated Service Tagging Code_: Each service has a `generate.go` file where generator directives live.
  Through these directives and their flags, you can customize code generation for the service.
  You can find the code that the tagging generator generates in a `tags_gen.go` file in a service, such as `internal/service/ec2/tags_gen.go`.
  You should generally _not_ need to edit the generator code itself (i.e., in `internal/generate/tags`).
- _Resource Code_: In the resource code, add the `tags` and `tags_all` schema attributes,
  along with a plan modification in the resource definition, and handling in `Create`, `Read`, and `Update` functions.
- _Resource Acceptance Tests_: In the resource acceptance tests, add new acceptance test functions and configurations to exercise the new tagging logic.
- _Resource Documentation_: In the resource documentation, add the `tags` argument and `tags_all` attribute.

## Generating Tag Code for a Service

This step is generally only necessary for the first implementation and may have been previously completed.

More details about this code generation,
including fixes for potential error messages in this process,
can be found in the [`generate` package documentation](https://github.com/hashicorp/terraform-provider-aws/tree/main/internal/generate/tags/README.md).

The generator will create several types of tagging-related code.
All services that support tagging will generate the function `KeyValueTags`, which converts from service-specific structs returned by the AWS SDK into a common format used by the provider,
and the function `Tags`, which converts from the common format back to the service-specific structs.
In addition, many services have separate functions to list or update tags, so the corresponding `listTags` and `updateTags` can be generated.
Optionally, to retrieve a specific tag, you can generate the `GetTag` function.

If the service directory does not contain a `generate.go` file, create one.
This file must only contain generate directives and a package declaration (e.g., `package eks`).
For examples of the `generate.go` file, many service directories contain one, e.g., `internal/service/eks/generate.go`.

If the `generate.go` file does not contain a generate directive for tagging code, i.e., `//go:generate go run ../../generate/tags/main.go`, add it.
Note that without flags, the directive itself will not do anything useful.
You must not include more than one `generate/tags/main.go` directive, as subsequent directives will overwrite previous directives.
To generate multiple types of tag code, use multiple flags with the directive.

### Generating Tagging Types

Determine how the service implements tagging:
Some services will use a simple map style (`map[string]*string` in Go),
while others will have a separate structure, often a `[]service.Tag` struct with `Key` and `Value` fields.

If the service uses the simple map style, pass the flag `-ServiceTagsMap`.

If the service uses a slice of structs, pass the flag `-ServiceTagsSlice`.
If the name of the tag struct is not `Tag`, pass the flag `-TagType=<struct name>`.
Note that the struct name is used without the package name.
For example, the AppMesh service uses the struct `TagRef`, so the flag is `-TagType=TagRef`.
If the key and value fields on the struct are not `Key` and `Value`,
specify the names using the flags `-TagTypeKeyElem` and `-TagTypeValElem` respectively.
For example, the KMS service uses the struct `Tag`, but the key and value fields are `TagKey` and `TagValue`,
so the flags are `-TagTypeKeyElem=TagKey` and `-TagTypeValElem=TagValue`.

Some services, such as EC2 and Auto Scaling, return a different type depending on the API call used to retrieve the tag.
To indicate the additional type, include the flag `-TagType2=<struct name>`.
For example, the Auto Scaling uses the struct `Tag` as part of resource calls, but returns the struct `TagDescription` from the `DescribeTags` API call. The flag used is `-TagType2=TagDescription`.

For more details on flags for generating service keys, see the
[documentation for the tag generator](https://github.com/hashicorp/terraform-provider-aws/tree/main/internal/generate/tags/README.md)

### Generating Standalone Tag Listing Functions

If the service API uses a standalone function to retrieve tags instead of including them with the resource (usually a `ListTags` or `ListTagsForResource` API call), pass the flag `-ListTags`.

If the API call is not `ListTagsForResource`, pass the flag `-ListTagsOp=<API call name>`.
Note that this does not include the package name.
For example, the Auto Scaling service uses the API call `DescribeTags`, so the flag is `-ListTagsOp=DescribeTags`.

If the API call uses a field other than `ResourceArn` to identify the resource, pass the flag `-ListTagsInIDElem=<field name>`.
For example, the CloudWatch service uses the field `ResourceARN`, so the flag is `-ListTagsInIDElem=ResourceARN`.
Some API calls take a slice of identifiers instead of a single identifier.
In this case, pass the flag `-ListTagsInIDNeedSlice=yes`.

If the field containing the tags in the result of the API call is not named `Tags`, pass the flag `-ListTagsOutTagsElem=<struct name>`.
For example, the CloudTrail service returns a nested structure, where the resulting flag is `-ListTagsOutTagsElem=ResourceTagList[0].TagsList`.

In some cases, it can be useful to retrieve single tags.
Pass the flag `-GetTag` to generate a function to do so.

For more details on flags for generating tag listing functions, see the
[documentation for the tag generator](https://github.com/hashicorp/terraform-provider-aws/tree/main/internal/generate/tags/README.md)

### Generating Standalone Tag Updating Functions

If the service API uses a standalone function to update tags instead of including them when updating the resource (usually a `TagResource` and `UntagResource` API call), pass the flag `-UpdateTags`.

If the API call to add tags is not `TagResource`, pass the flag `-TagOp=<API call name>`.
Note that this does not include the package name.
For example, the ElastiCache service uses the API call `AddTagsToResource`, so the flag is `-TagOp=AddTagsToResource`.

If the API call to add tags uses a field other than `ResourceArn` to identify the resource, pass the flag `-TagInIDElem=<field name>`.
For example, the EC2 service uses the field `Resources`, so the flag is `-TagInIDElem=Resources`.
Some API calls take a slice of identifiers instead of a single identifier.
In this case, pass the flag `-TagInIDNeedSlice=yes`.

If the API call to remove tags is not `UntagResource`, pass the flag `-UntagOp=<API call name>`.
Note that this does not include the package name.
For example, the ElastiCache service uses the API call `RemoveTagsFromResource`, so the flag is `-UntagOp=RemoveTagsFromResource`.

If the API call to remove tags uses a field other than `ResourceArn` to identify the resource, pass the flag `-UntagInTagsElem=<field name>`.
For example, the Route 53 service uses the field `Keys`, so the flag is `-UntagInTagsElem=Keys`.

For more details on flags for generating tag updating functions, see the
[documentation for the tag generator](https://github.com/hashicorp/terraform-provider-aws/tree/main/internal/generate/tags/README.md)

#### Generating Standalone Post-Creation Tag Updating Functions

When creating a resource, some AWS APIs support passing tags in the Create call while others require setting the tags after the initial creation.
If the API does not support tagging on creation, pass the `-CreateTags` flag to generate a `createTags` function that can be called from the resource Create handler function.

### Running Code generation

Run the command `make gen` to run the code generators for the project.
To ensure that the code compiles, run `make test`.

## Resource Code

### Resource Schema

Add the following imports to the resource's Go source file:

```go
imports (
    /* ... other imports ... */
    tftags "github.com/hashicorp/terraform-provider-aws/internal/tags"
    "github.com/hashicorp/terraform-provider-aws/internal/verify"
    "github.com/hashicorp/terraform-provider-aws/names"
)
```

Add the `tags` parameter and `tags_all` attribute to the schema, using constants defined in the `names` package.
The `tags` parameter contains the tags set directly on the resource.
The `tags_all` attribute contains a union of the tags set directly on the resource and default tags configured on the provider.

=== "Terraform Plugin Framework (Preferred)"
    ```go
    func (r *resourceExample) Schema(ctx context.Context, req resource.SchemaRequest, resp *resource.SchemaResponse) {
        resp.Schema = schema.Schema{
            Attributes: map[string]schema.Attribute{
                /* ... other configuration ... */
                names.AttrTags:    tftags.TagsAttribute(),
                names.AttrTagsAll: tftags.TagsAttributeComputedOnly(),
            },
        }
    }
    ```

=== "Terraform Plugin SDK V2"
    ```go
    func ResourceExample() *schema.Resource {
        return &schema.Resource{
            /* ... other configuration ... */
            Schema: map[string]*schema.Schema{
                /* ... other configuration ... */
                names.AttrTags:    tftags.TagsSchema(),
                names.AttrTagsAll: tftags.TagsSchemaComputed(),
            },
        }
    }
    ```

Add a plan modifier (Terraform Plugin Framework) or a `CustomizeDiff` function (Terraform Plugin SDK V2) to ensure tagging diffs are handled appropriately.
These functions handle the combination of tags set on the resource and default tags, and must be set for tagging to function properly.

=== "Terraform Plugin Framework (Preferred)"
    ```go
    func (r *resourceExample) ModifyPlan(ctx context.Context, req resource.ModifyPlanRequest, resp *resource.ModifyPlanResponse) {
        r.SetTagsAll(ctx, req, resp)
    }
    ```

=== "Terraform Plugin SDK V2"
    ```go
    func ResourceExample() *schema.Resource {
      return &schema.Resource{
        /* ... other configuration ... */
        CustomizeDiff: verify.SetTagsDiff,
      }
    }
    ```

If the resource already implements `ModifyPlan`, simply include the `SetTagsAll` function at the end of the method body.

### Transparent Tagging

Most services can use a facility we call _transparent_ (or _implicit_) _tagging_, where the majority of resource tagging functionality is implemented using code located in the provider's runtime packages (see `internal/provider/intercept.go` and `internal/provider/fwprovider/intercept.go` for details) and not in the resource's CRUD handler functions. Resource implementers opt-in to transparent tagging by adding an _annotation_ (a specially formatted Go comment) to the resource's factory function (similar to the [resource self-registration mechanism](add-a-new-resource.md)).

=== "Terraform Plugin Framework (Preferred)"
    ```go
    // @FrameworkResource("aws_service_example", name="Example")
    // @Tags(identifierAttribute="arn")
    func newResourceExample(_ context.Context) (resource.ResourceWithConfigure, error) {
        return &resourceExample{}, nil
    }
    ```

=== "Terraform Plugin SDK V2"
    ```go
    // @SDKResource("aws_service_example", name="Example")
    // @Tags(identifierAttribute="arn")
    func ResourceExample() *schema.Resource {
      return &schema.Resource{
        ...
      }
    }
    ```

The `identifierAttribute` argument to the `@Tags` annotation identifies the attribute in the resource type's schema whose value is used in tag listing and updating API calls.
Common values are `"arn"` and `"id"`.
If the resource type does not need separate `createTags`, `listTags`, or `updateTags` functions, do not specify an `identifierAttribute`.

Once the annotation has been added to the resource's code, run `make gen` to register the resource for transparent tagging.
This will add an entry to the `service_package_gen.go` file located in the service package folder.

#### Resource Create Operation

When creating a resource, some AWS APIs support passing tags in the Create call
while others require setting the tags after the initial creation.

If the API supports tagging on creation (e.g., the `Input` struct accepts a `Tags` field),
use the `getTagsIn` function to get any configured tags.

=== "Terraform Plugin Framework (Preferred)"
    ```go
    input := &service.CreateExampleInput{
      /* ... other configuration ... */
      Tags: getTagsIn(ctx),
    }
    ```

=== "Terraform Plugin SDK V2"
    ```go
    input := &service.CreateExampleInput{
      /* ... other configuration ... */
      Tags: getTagsIn(ctx),
    }
    ```

Otherwise, if the API does not support tagging on creation, call `createTags` after the resource has been created.

=== "Terraform Plugin Framework (Preferred)"
    ```go
    if err := createTags(ctx, conn, plan.ID.ValueString(), getTagsIn(ctx)); err != nil {
        resp.Diagnostics.AddError(
            create.ProblemStandardMessage(names.Service, create.ErrActionCreating, ResNameExample, plan.ID.String(), nil),
            err.Error(),
        )
        return
    }
    ```

=== "Terraform Plugin SDK V2"
    ```go
    if err := createTags(ctx, conn, d.Id(), getTagsIn(ctx)); err != nil {
      return sdkdiag.AppendErrorf(diags, "setting Service Example (%s) tags: %s", d.Id(), err)
    }
    ```

#### Resource Read Operation

In the resource `Read` operation, use the `setTagsOut` function to signal to the transparent tagging mechanism that the resource has tags that should be saved into Terraform state.

=== "Terraform Plugin Framework (Preferred)"
    ```go
    setTagsOut(ctx, out.Tags)
    ```

=== "Terraform Plugin SDK V2"
    ```go
    setTagsOut(ctx, out.Tags)
    ```

If the service API does not return the tags directly from reading the resource and requires use of the generated `listTags` function, do nothing and the transparent tagging mechanism will make the `listTags` call and save any tags into the Terraform state.

#### Resource Update Operation

In the resource `Update` operation, only non-`tags` updates need to be done as the transparent tagging mechanism makes the `updateTags` call.

=== "Terraform Plugin Framework (Preferred)"
    ```go
    if !plan.Name.Equal(state.Name) ||
        !plan.Description.Equal(state.Description) ||
        // etc.
        // Do NOT check for tags changes here.
        !plan.OtherField.Equal(state.OtherField) {
        ...
    }
    ```

=== "Terraform Plugin SDK V2"
    ```go
    if d.HasChangesExcept("tags", "tags_all") {
      ...
    }
    ```

For Terraform Plugin SDK V2 based resources, ensure that the `Update` operation always calls the resource `Read` operation before returning so that the transparent tagging mechanism correctly saves any tags into the Terraform state.

=== "Terraform Plugin SDK V2"
    ```go
    func resourceAnalyzerUpdate(ctx context.Context, d *schema.ResourceData, meta interface{}) diag.Diagnostics {
      var diags diag.Diagnostics
      // Tags only.
      return append(diags, resourceAnalyzerRead(ctx, d, meta)...)
    }
    ```

### Explicit Tagging

If the resource cannot opt-in to transparent tagging, more boilerplate code must be explicitly added to the resource CRUD handler functions.
This section describes how to do this.

!!! note

    There are currently no Terraform Plugin Framework based resources which use explicit tagging. As such, the remaining examples in this section will reference legacy Terraform Plugin SDK V2 patterns.

#### Resource Create Operation

When creating a resource, some AWS APIs support passing tags in the Create call
while others require setting the tags after the initial creation.

If the API supports tagging on creation (e.g., the `Input` struct accepts a `Tags` field),
implement the logic to convert the configuration tags into the service tags, e.g., with EKS Clusters:

=== "Terraform Plugin SDK V2"
    ```go
    // Typically declared near conn := /*...*/
    defaultTagsConfig := meta.(*conns.AWSClient).DefaultTagsConfig(ctx)
    tags := defaultTagsConfig.MergeTags(tftags.New(ctx, d.Get("tags").(map[string]interface{})))

    input := &eks.CreateClusterInput{
      /* ... other configuration ... */
      Tags: Tags(tags.IgnoreAWS()),
    }
    ```

If the service API does not allow passing an empty list, the logic can be adjusted similarly to:

=== "Terraform Plugin SDK V2"
    ```go
    // Typically declared near conn := /*...*/
    defaultTagsConfig := meta.(*conns.AWSClient).DefaultTagsConfig(ctx)
    tags := defaultTagsConfig.MergeTags(tftags.New(ctx, d.Get("tags").(map[string]interface{})))

    input := &eks.CreateClusterInput{
      /* ...other configuration... */
    }

    if len(tags) > 0 {
      input.Tags = Tags(tags.IgnoreAWS())
    }
    ```

Otherwise, if the API does not support tagging on creation,
implement the logic to convert the configuration tags into the service API call to tag a resource, e.g., with Device Farm device pools:

=== "Terraform Plugin SDK V2"
    ```go
    // Typically declared near conn := /*...*/
    defaultTagsConfig := meta.(*conns.AWSClient).DefaultTagsConfig(ctx)
    tags := defaultTagsConfig.MergeTags(tftags.New(ctx, d.Get("tags").(map[string]interface{})))

    /* ... creation steps ... */

    if len(tags) > 0 {
      if err := updateTags(ctx, conn, d.Id(), nil, tags); err != nil {
        return fmt.Errorf("adding DeviceFarm Device Pool (%s) tags: %w", d.Id(), err)
      }
    }
    ```

Some EC2 resources (e.g., [`aws_ec2_fleet`](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/ec2_fleet)) have a `TagSpecifications` field in the `InputStruct` instead of a `Tags` field.
In these cases the `tagSpecificationsFromKeyValue()` helper function should be used.
This example shows using `TagSpecifications`:

=== "Terraform Plugin SDK V2"
    ```go
    // Typically declared near conn := /*...*/
    defaultTagsConfig := meta.(*conns.AWSClient).DefaultTagsConfig(ctx)
    tags := defaultTagsConfig.MergeTags(tftags.New(ctx, d.Get("tags").(map[string]interface{})))

    input := &ec2.CreateFleetInput{
        /* ... other configuration ... */
        TagSpecifications: tagSpecificationsFromKeyValue(tags, ec2.ResourceTypeFleet),
    }
    ```

#### Resource Read Operation

In the resource `Read` operation, implement the logic to convert the service tags to save them into the Terraform state for drift detection, e.g., with EKS Clusters:

=== "Terraform Plugin SDK V2"
    ```go
    // Typically declared near conn := /*...*/
    defaultTagsConfig := meta.(*conns.AWSClient).DefaultTagsConfig(ctx)
    ignoreTagsConfig := meta.(*conns.AWSClient).IgnoreTagsConfig(ctx)

    /* ... other d.Set(...) logic ... */

    tags := KeyValueTags(ctx, cluster.Tags).IgnoreAWS().IgnoreConfig(ignoreTagsConfig)

    if err := d.Set("tags", tags.RemoveDefaultConfig(defaultTagsConfig).Map()); err != nil {
      return fmt.Errorf("setting tags: %w", err)
    }

    if err := d.Set("tags_all", tags.Map()); err != nil {
      return fmt.Errorf("setting tags_all: %w", err)
    }
    ```

If the service API does not return the tags directly from reading the resource and requires a separate API call,
use the generated `listTags` function, e.g., with Athena Workgroups:

=== "Terraform Plugin SDK V2"
    ```go
    // Typically declared near conn := /*...*/
    defaultTagsConfig := meta.(*conns.AWSClient).DefaultTagsConfig(ctx)
    ignoreTagsConfig := meta.(*conns.AWSClient).IgnoreTagsConfig(ctx)

    /* ... other d.Set(...) logic ... */

    tags, err := listTags(ctx, conn, arn.String())

    if err != nil {
      return fmt.Errorf("listing tags for resource (%s): %w", arn, err)
    }

    tags = tags.IgnoreAWS().IgnoreConfig(ignoreTagsConfig)

    if err := d.Set("tags", tags.RemoveDefaultConfig(defaultTagsConfig).Map()); err != nil {
      return fmt.Errorf("setting tags: %w", err)
    }

    if err := d.Set("tags_all", tags.Map()); err != nil {
      return fmt.Errorf("setting tags_all: %w", err)
    }
    ```

#### Resource Update Operation

In the resource `Update` operation, implement the logic to handle tagging updates, e.g., with EKS Clusters:

=== "Terraform Plugin SDK V2"
    ```go
    if d.HasChange("tags_all") {
      o, n := d.GetChange("tags_all")
      if err := updateTags(ctx, conn, d.Get("arn").(string), o, n); err != nil {
        return fmt.Errorf("updating tags: %w", err)
      }
    }
    ```

If the resource `Update` function applies specific updates to attributes regardless of changes to tags, implement the following e.g., with IAM Policy:

=== "Terraform Plugin SDK V2"
    ```go
    if d.HasChangesExcept("tags", "tags_all") {
      /* ... other logic ...*/
      request := &iam.CreatePolicyVersionInput{
        PolicyArn:      aws.String(d.Id()),
        PolicyDocument: aws.String(d.Get("policy").(string)),
        SetAsDefault:   aws.Bool(true),
      }

      if _, err := conn.CreatePolicyVersionWithContext(ctx, request); err != nil {
          return fmt.Errorf("updating IAM policy (%s): %w", d.Id(), err)
      }
    }
    ```

## Resource Acceptance Tests

Some services, and some resource or data source types within services, have generated acceptance tests for tagging support.
These tests cover a broad set of tagging behaviors.
New services should use the generated acceptance tests.

### Generated Acceptance Tests

To enable generated acceptance tests for a service, add the following line to the service's `generate.go` file:

```go
//go:generate go run ../../generate/tagstests/main.go
```

#### Controlling Test Generation

By default, all resource or data source types which support transparent tagging will have tagging tests generated.
Individual resource or data source types can be excluded from generated acceptance tests by adding the annotation `@Testing(tagsTest=false)` to the resource type declaration.
If a resource or data source type supports tags but does not use transparent tagging, generate the tests by adding the annotion `@Testing(tagsTest=true)`

Additional `@Testing(...)` parameters can be used to control the generated tests.

Most testing configurations take a single parameter, often a name or a domain name.
The most common case is parameter `rName` with a value generated by `sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)`, so this is the default.
If no `rName` is required, add the annotation `@Testing(generator=false)`.
Other values can be used by setting the `generator` to a reference to a function call.
The reference optionally contains a Go package path and package alias, using the format
`[<package path>;[<package alias>;]]<function call>`.
For example, the Service Catalog Portfolio uses a five-character long random string

```go
// @Testing(generator="github.com/hashicorp/terraform-plugin-testing/helper/acctest;sdkacctest;sdkacctest.RandString(5)")
```

Some acceptance tests also require a TLS key and certificate.
This can be included by setting the annotation `@Testing(tlsKey=true)`,
which will add the Terraform variables `certificate_pem` and `private_key_pem` to the configuration.
By default, the common name for the certificate is `example.com`.
To override the common name, set the annotation `@Testing(tlsKeyDomain=<reference>) to reference an existing variable.
For example, the API Gateway v2 Domain Name sets the variable `rName` to `acctest.RandomSubdomain()`
and sets the annotation `@Testing(tlsKeyDomain=rName)` to reference it.

No additional parameters can be defined currently.
If additional parameters are required, and cannot be derived from `rName`, the resource type must use manually created acceptance tests as described below.

Most `Exists` functions used in acceptance tests take a pointer to the returned API object.
To specify the type of this parameter, use the annotion `@Testing(existsType=<reference>)`.
This references a Go type and package path with optional package alias, using the format
`<package path>;[<package alias>;]<function call>`.
For example, the S3 Object uses

```go
// @Testing(existsType="github.com/aws/aws-sdk-go-v2/service/s3;s3.GetObjectOutput")
```

Some services or resource types are using a new variant of the standard `Exists` and `DestroyCheck` functions that use `acctest.ProviderMeta` internally, and thus take a `testing.T` as a parameter.
In that case, add the annotations `@Testing(existsTakesT=true)` and `@Testing(destroyTakesT=true)`, respectively.

The generated acceptance tests use `ImportState` steps.
In most cases, these will work as-is.
To ignore the values of certain parameters when importing, set the annotation `@Testing(importIgnore="...")` to a list of the parameter names separated by semi-colons (`;`).
There are multiple methods for overriding the import ID, if needed.
To use the value of an existing variable, use the annotation `@Testing(importStateId=<var name>)`.
If the identifier can be retrieved from a specific resource attribute, use the annotation `@Testing(importStateIdAttribute=<attribute name>)`.
If the identifier can be retrieved from a `resource.ImportStateIdFunc`, use the annotation `@Testing(importStateIdFunc=<func name>)`.
If the resource type does not support importing, use the annotation `@Testing(noImport=true)`.

If the tests need to be serialized, use the annotion `@Testing(serialize=true)`.
If a delay is needed between serialized tests, also use the annotation `@Testing(serializeDelay=<duration>)` with a duration in the format used by [`time.ParseDuration()`](https://pkg.go.dev/time#ParseDuration).
For example, 3 minutes and 30 seconds is `3m30s`.

Some services do not support tags with an empty string value.
In that case, use the annotation `@Testing(skipEmptyTags=true)`.

Some services do not support tags with an null string value.
In that case, use the annotation `@Testing(skipNullTags=true)`.

Some resource types use the no-op `CheckDestroy` function `acctest.CheckDestroyNoop`.
Use the annotation `@Testing(checkDestroyNoop=true)`.

For some resource types, tags cannot be modified without recreating the resource.
Use the annotation `@Testing(tagsUpdateForceNew=true)`.

Resource types which pass the result of `getTagsIn` directly onto their Update Input may have an error where ignored tags are not correctly excluded from the update.
Use the annotation `@Testing(tagsUpdateGetTagsIn=true)`.

Some tests read the tag values directly from the AWS API.
If the resource type does not specify `identifierAttribute` in its `@Tags` annotation, specify a `@Testing(tagsIdentifierAttribute=<attribute name>)` annotation to identify which attribute value should be used by the `listTags` function.
If a resource type is also needed for the `listTags` function, also specify the `tagsResourceType` annotation.

At least one resource type, the Service Catalog Provisioned Product, does not support removing tags.
This is likely an error on the AWS side.
Add the annotation `@Testing(noRemoveTags=true)` as a workaround.

#### Test Terraform Configurations

The generated acceptance tests use `ConfigDirectory` to specify the test configurations in a directory of Terraform `.tf` files.
The configuration files are generated from a [Go template](https://pkg.go.dev/text/template) file located in `testdata/tmpl/<name>_tags.gtpl`,
where `name` is the name of the resource type's implementation file wihtout the `.go` extension.
For example, the ELB v2 Load Balancer's implementation file is `load_balancer.go`, so the template is `testdata/tmpl/load_balancer_tags.gtpl`.

To generate a configuration for a data source test, the generator reuses the configuration for the corresponding resource type.
Add an additional file `testdata/tmpl/<name>_data_source.gtpl` which contains only the data source block populated with the parameters needed to associate it with the resource.
For example, the ELB v2 Load Balancer's data source template is `testdata/tmpl/load_balancer_data_source.gtpl`.

Replace the `tags` attribute with the Go template directive `{{- template "tags" . }}`.
When the configurations are generated, this will be replaced with the appropriate assignment to the `tags` attribute.

Tags should only be applied to the resource that is being tested.

### Manually Created Acceptance Tests

In the resource acceptance tests (e.g., `internal/service/eks/cluster_test.go`), verify that existing resources without tagging are unaffected and do not have tags saved into their Terraform state. This should be done in the `_basic` acceptance test by adding one line similar to `resource.TestCheckResourceAttr(resourceName, "tags.%", "0"),` and one similar to `resource.TestCheckResourceAttr(resourceName, "tags_all.%", "0"),`

Add a new test named `_tags` with associated configurations, that verifies creating the resource with tags and updating tags. E.g., EKS Clusters:

```go
func TestAccEKSCluster_tags(t *testing.T) {
	ctx := acctest.Context(t)
  var cluster1, cluster2, cluster3 eks.Cluster
  rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)
  resourceName := "aws_eks_cluster.test"

  resource.ParallelTest(t, resource.TestCase{
    PreCheck:                 func() { acctest.PreCheck(ctx, t); testAccPreCheck(t) },
    ErrorCheck:               acctest.ErrorCheck(t, names.EKSServiceID),
    ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
    CheckDestroy:             testAccCheckClusterDestroy(ctx),
    Steps: []resource.TestStep{
      {
        Config: testAccClusterConfig_tags1(rName, "key1", "value1"),
        Check: resource.ComposeTestCheckFunc(
          testAccCheckClusterExists(ctx, resourceName, &cluster1),
          resource.TestCheckResourceAttr(resourceName, "tags.%", "1"),
          resource.TestCheckResourceAttr(resourceName, "tags.key1", "value1"),
        ),
      },
      {
        ResourceName:      resourceName,
        ImportState:       true,
        ImportStateVerify: true,
      },
      {
        Config: testAccClusterConfig_tags2(rName, "key1", "value1updated", "key2", "value2"),
        Check: resource.ComposeTestCheckFunc(
          testAccCheckClusterExists(ctx, resourceName, &cluster2),
          resource.TestCheckResourceAttr(resourceName, "tags.%", "2"),
          resource.TestCheckResourceAttr(resourceName, "tags.key1", "value1updated"),
          resource.TestCheckResourceAttr(resourceName, "tags.key2", "value2"),
        ),
      },
      {
        Config: testAccClusterConfig_tags1(rName, "key2", "value2"),
        Check: resource.ComposeTestCheckFunc(
          testAccCheckClusterExists(ctx, resourceName, &cluster3),
          resource.TestCheckResourceAttr(resourceName, "tags.%", "1"),
          resource.TestCheckResourceAttr(resourceName, "tags.key2", "value2"),
        ),
      },
    },
  })
}

func testAccClusterConfig_tags1(rName, tagKey1, tagValue1 string) string {
  return acctest.ConfigCompose(testAccClusterConfig_base(rName), fmt.Sprintf(`
resource "aws_eks_cluster" "test" {
  name     = %[1]q
  role_arn = aws_iam_role.test.arn

  tags = {
    %[2]q = %[3]q
  }

  vpc_config {
    subnet_ids = aws_subnet.test[*].id
  }

  depends_on = [aws_iam_role_policy_attachment.test-AmazonEKSClusterPolicy]
}
`, rName, tagKey1, tagValue1))
}

func testAccClusterConfig_tags2(rName, tagKey1, tagValue1, tagKey2, tagValue2 string) string {
  return acctest.ConfigCompose(testAccClusterConfig_base(rName), fmt.Sprintf(`
resource "aws_eks_cluster" "test" {
  name     = %[1]q
  role_arn = aws_iam_role.test.arn

  tags = {
    %[2]q = %[3]q
    %[4]q = %[5]q
  }

  vpc_config {
    subnet_ids = aws_subnet.test[*].id
  }

  depends_on = [aws_iam_role_policy_attachment.test-AmazonEKSClusterPolicy]
}
`, rName, tagKey1, tagValue1, tagKey2, tagValue2))
}
```

Verify all acceptance testing passes for the resource (e.g., `make testacc TESTS=TestAccEKSCluster_ PKG=eks`)

## Resource Documentation

In the resource documentation (e.g., `website/docs/r/service_example.html.markdown`), add the following to the arguments reference:

```markdown
* `tags` - (Optional) Map of tags assigned to the resource. If configured with a provider [`default_tags` configuration block](/docs/providers/aws/index.html#default_tags-configuration-block) present, tags with matching keys will overwrite those defined at the provider-level.
```

In the resource documentation (e.g., `website/docs/r/service_example.html.markdown`), add the following to the attribute reference:

```markdown
* `tags_all` - Map of tags assigned to the resource, including those inherited from the provider [`default_tags` configuration block](/docs/providers/aws/index.html#default_tags-configuration-block).
```
<!-- markdownlint-configure-file { "code-block-style": false } -->
# Retries and Waiters

Terraform plugins may run into situations where calling the remote system after an operation may be necessary. These typically fall under three classes where:

- The request never reaches the remote system.
- The request reaches the remote system and responds that it cannot handle the request temporarily.
- The implementation of the remote system requires additional requests to ensure success.

This guide describes the behavior of the Terraform AWS Provider and provides code implementations that help ensure success in each of these situations.

!!! note
    The helper functions detailed below **are** compatible with Terraform Plugin Framework based resources (the required library for net-new resources).
    While these functions currently reside in the legacy Terraform Plugin SDK repository, they are not directly tied to functionality exclusive to this library, and likely will be moved to a standalone library or into the AWS provider itself in the future.

## Terraform Plugin SDK Functionality

The [Terraform Plugin SDK](https://github.com/hashicorp/terraform-plugin-sdk/), which the AWS Provider uses, provides vital tools for handling consistency: the `retry.StateChangeConf{}` struct, and the retry function `retry.RetryContext()`.
We will discuss these throughout the rest of this guide.
Since they help keep the AWS Provider code consistent, we heavily prefer them over custom implementations.

This guide goes beyond the [Terraform Plugin SDK v2 documentation](https://www.terraform.io/plugin/sdkv2/resources/retries-and-customizable-timeouts) by providing additional context and emergent implementations specific to the Terraform AWS Provider.

### State Change Configuration and Functions

The [`retry.StateChangeConf` type](https://pkg.go.dev/github.com/hashicorp/terraform-plugin-sdk/v2/helper/retry#StateChangeConf), along with its receiver methods [`WaitForState()`](https://pkg.go.dev/github.com/hashicorp/terraform-plugin-sdk/v2/helper/retry#StateChangeConf.WaitForState) and [`WaitForStateContext()`](https://pkg.go.dev/github.com/hashicorp/terraform-plugin-sdk/v2/helper/retry#StateChangeConf.WaitForStateContext) is a generic primitive for repeating operations in Terraform resource logic until desired value(s) are received. The "state change" in this case is generic to any value and not specific to the Terraform State. Among other functionality, it supports some of these desirable optional properties:

- Expecting specific value(s) while waiting for the target value(s) to be reached. Unexpected values are returned as an error which can be augmented with additional details.
- Expecting the target value(s) to be returned multiple times in succession.
- Allowing various polling configurations such as delaying the initial request and setting the time between polls.

### Retry Functions

The [`retry.RetryContext()`](https://pkg.go.dev/github.com/hashicorp/terraform-plugin-sdk/v2/helper/retry#RetryContext) function provides a simplified retry implementation around `retry.StateChangeConf`.
The most common use is for simple error-based retries.

## AWS Request Handling

The Terraform AWS Provider's requests to AWS service APIs happen on top of Hypertext Transfer Protocol (HTTP). The following is a simplified description of the layers and handling that requests pass through:

- A Terraform resource calls an AWS Go SDK function.
- The AWS Go SDK generates an AWS-compatible HTTP request using the [Go standard library `net/http` package](https://pkg.go.dev/net/http/). This includes the following:
    - Adding HTTP headers for authentication and signing of requests to ensure authenticity.
    - Converting operation inputs into required HTTP URI parameters and/or request body type (XML or JSON).
    - If debug logging is enabled, logging of the HTTP request.
- The AWS Go SDK transmits the `net/http` request using Go's standard handling of the Operating System (OS) and Domain Name System (DNS) configuration.
- The AWS service potentially receives the request and responds, typically adding a request identifier HTTP header which can be used for AWS Support cases.
- The OS and Go `net/http` receive the response and pass it to the AWS Go SDK.
- The AWS Go SDK attempts to handle the response. This may include:
    - Parsing output
    - Converting errors into operation errors (Go `error` type of wrapped [`awserr.Error` type](https://docs.aws.amazon.com/sdk-for-go/api/aws/awserr/#Error)).
    - Converting response elements into operation outputs (AWS Go SDK operation-specific types).
    - Triggering automatic request retries based on default and custom logic.
- The Terraform resource receives the response, including any output and errors, from the AWS Go SDK.

In cases where custom operation handling is configured for a specific service client, the changes can typically be found in `internal/service/{service-name}/service_package.go`.

### Default AWS Go SDK Retries

In some situations, while handling a response, the AWS Go SDK automatically retries a request before returning the output and error. The retry mechanism implements an exponential backoff algorithm. The default conditions triggering automatic retries (implemented through [`client.DefaultRetryer`](https://docs.aws.amazon.com/sdk-for-go/api/aws/client/#DefaultRetryer)) include:

- Certain network errors. A common exception to this is connection reset errors.
- HTTP status codes 429 and 5xx.
- Certain API error codes, which are common across various AWS services (e.g., `ThrottledException`). However, not all AWS services implement these error codes consistently. A common exception to this is certain expired credentials errors.

By default, the Terraform AWS Provider sets the maximum number of AWS Go SDK retries based on the [`max_retries` provider configuration](https://registry.terraform.io/providers/hashicorp/aws/latest/docs#max_retries). The provider configuration defaults to 25 and the exponential backoff roughly equates to one hour of retries. This very high default value was present before the Terraform AWS Provider codebase was split from Terraform CLI in version 0.10.

### Lower Network Error Retries

Given the very high default number of AWS Go SDK retries configured in the Terraform AWS Provider and the excessive wait that practitioners would face, the [`hashicorp/aws-sdk-go-base` codebase](https://github.com/hashicorp/aws-sdk-go-base/blob/57529b4c2d2f8f3b5299d66a829b01259fa800d7/session.go#L108-L130) lowers retries to 10 for certain network errors that typically cannot be remediated via retries. This roughly equates to 30 seconds of retries.

### Terraform AWS Provider Service Retries

The AWS Go SDK provides hooks for injecting custom logic into service client handlers.
We prefer this handling in situations where contributors would need to apply the retry behavior to many resources.
For example, in cases where the AWS service API does not mark an error code as automatically retriable.
The AWS Provider includes other retry-changing behaviors using this method.
When custom service client configurations are applied, these will be defined in `internal/service/{service-name}/service_package.go`.

With V2 of the AWS Go SDK, the retrier is extended directly in client construction.

    ```go
    // NewClient returns a new AWS SDK for Go v2 client for this service package's AWS API.
    func (p *servicePackage) NewClient(ctx context.Context, config map[string]any) (*s3_sdkv2.Client, error) {
    	cfg := *(config["aws_sdkv2_config"].(*aws_sdkv2.Config))
    
    	return s3_sdkv2.NewFromConfig(cfg,
			s3.WithEndpointResolverV2(newEndpointResolverSDKv2()),
			withBaseEndpoint(config[names.AttrEndpoint].(string)),
			func(o *s3_sdkv2.Options) {
				// ..other configuration..
		
				o.Retryer = conns.AddIsErrorRetryables(cfg.Retryer().(aws_sdkv2.RetryerV2), retry_sdkv2.IsErrorRetryableFunc(func(err error) aws_sdkv2.Ternary {
					if tfawserr_sdkv2.ErrMessageContains(err, errCodeOperationAborted, "A conflicting conditional operation is currently in progress against this resource. Please try again.") {
						return aws_sdkv2.TrueTernary
					}
					return aws_sdkv2.UnknownTernary // Delegate to configured Retryer.
				}))
			},
		), nil
    }
    ```

## Eventual Consistency

Eventual consistency is a temporary condition where the remote system can return outdated information or errors due to not being strongly read-after-write consistent.
This is a pattern found in remote systems that must be highly scaled for broad usage.

Terraform expects any planned resource lifecycle change (create, update, destroy of the resource itself) and planned resource attribute value change to match after being applied.
Conversely, operators typically expect that Terraform resources also implement the concept of drift detection for resources and their attributes, which requires reading information back from the remote system after an operation.
A common implementation is calling the underlying `Get`/`Describe` AWS API after `Create` and `Update`.

These two concepts conflict with each other and require additional handling in Terraform resource logic as shown in the following sections.
These issues are _not_ reliably reproducible, especially in the case of writing acceptance testing, so they can be elusive with false positives to verify fixes.

### Operation Specific Error Retries

Even given a properly ordered Terraform configuration, eventual consistency can unexpectedly prevent downstream operations from succeeding.
A simple retry after a few seconds resolves many of these issues.
To reduce frustrating behavior for operators, wrap AWS Go SDK operations with the `retry.RetryContext()` function.
These retries should have a reasonably low timeout (typically two minutes but up to five minutes).
Save them in a constant for reusability.
These functions are preferably in line with the associated resource logic to remove any indirection with the code.

Do not use this type of logic to overcome improperly ordered Terraform configurations.
The approach may not work in larger environments.

```go
const (
	// Maximum amount of time to wait for Thing operation eventual consistency
	ThingOperationTimeout = 2 * time.Minute
)
```

    ```go
    // internal/service/{service}/{thing}.go

    // ... Create, Read, Update, or Delete function ...
    	err := retry.RetryContext(ctx, ThingOperationTimeout, func() *retry.RetryError {
    		_, err := conn./* ... AWS Go SDK operation with eventual consistency errors ... */

    		// Retryable conditions which can be checked.
    		// These must be updated to match the AWS service API error code and message.
            if errs.IsAErrorMessageContains[/* error type */](err, /* error message */) {
    			return retry.RetryableError(err)
    		}
    
    		if err != nil {
    			return retry.NonRetryableError(err)
    		}

    		return nil
    	})
    
    	// This check is important - it handles when the AWS Go SDK operation retries without returning.
    	// e.g., any automatic retries due to network or throttling errors.
    	if tfresource.TimedOut(err) {
    		// The use of equals assignment (over colon equals) is also important here.
    		// This overwrites the error variable to simplify logic.
    		_, err = conn./* ... AWS Go SDK operation with IAM eventual consistency errors ... */
    	}

    	if err != nil {
    		return fmt.Errorf("... error message context ... : %w", err)
    	}
    ```

#### IAM Error Retries

A common eventual consistency issue is an error returned due to IAM permissions. The IAM service itself is eventually consistent along with the propagation of its components and permissions to other AWS services. For example, if the following operations occur in quick succession:

- Create an IAM Role
- Attach an IAM Policy to the IAM Role
- Reference the new IAM Role in another AWS service, such as creating a Lambda Function

The last operation can receive varied API errors ranging from:

- IAM Role being reported as not existing
- IAM Role being reported as not having permissions for the other service to use it (assume role permissions)
- IAM Role being reported as not having sufficient permissions (inline or attached role permissions)

Each AWS service API (and sometimes even operations within the same API) varies in the implementation of these errors. To handle them, it is recommended to use the [Operation Specific Error Retries](#operation-specific-error-retries) pattern. The Terraform AWS Provider implements a standard timeout constant of two minutes in the `internal/service/iam` package which should be used for all retry timeouts associated with IAM errors. This timeout was derived from years of Terraform operational experience with all AWS APIs.

    ```go
    // internal/service/{service}/{thing}.go

    import (
    	// ... other imports ...
    	tfiam "github.com/hashicorp/terraform-provider-aws/internal/service/iam"
    )

    // ... Create and typically Update function ...
    	err := retry.RetryContext(ctx, iamwaiter.PropagationTimeout, func() *retry.RetryError {
    		_, err := conn./* ... AWS Go SDK operation with IAM eventual consistency errors ... */

    		// Example retryable condition
    		// This must be updated to match the AWS service API error code and message.
    		if errs.IsAErrorMessageContains[/* error type */](err, /* error message */) {
    			return retry.RetryableError(err)
    		}

    		if err != nil {
    			return retry.NonRetryableError(err)
    		}

    		return nil
    	})

    	if tfresource.TimedOut(err) {
    		_, err = conn./* ... AWS Go SDK operation with IAM eventual consistency errors ... */
    	}

    	if err != nil {
    		return fmt.Errorf("... error message context ... : %w", err)
    	}
    ```

#### Asynchronous Operation Error Retries

Some remote system operations run asynchronously as detailed in the [Asynchronous Operations section](#asynchronous-operations). In these cases, it is possible that the initial operation will immediately return as successful, but potentially return a retryable failure while checking the operation status that requires starting everything over. The handling for these is complicated by the fact that there are two timeouts, one for the retryable failure and one for the asynchronous operation status checking.

The below code example highlights this situation for a resource creation that also exhibited IAM eventual consistency.

```go
// internal/service/{service}/{thing}.go

import (
	// ... other imports ...
	tfiam "github.com/hashicorp/terraform-provider-aws/internal/service/iam"
)

// ... Create function ...

	// Underlying IAM eventual consistency errors can occur after the creation
	// operation. The goal is only retry these types of errors up to the IAM
	// timeout. Since the creation process is asynchronous and can take up to
	// its own timeout, we store a stop time upfront for checking.
	iamwaiterStopTime := time.Now().Add(tfiam.PropagationTimeout)

	// Ensure to add IAM eventual consistency timeout in case of retries
	err = retry.RetryContext(ctx, tfiam.PropagationTimeout+ThingOperationTimeout, func() *retry.RetryError {
		// Only retry IAM eventual consistency errors up to that timeout
		iamwaiterRetry := time.Now().Before(iamwaiterStopTime)

		_, err := conn./* ... AWS Go SDK operation without eventual consistency errors ... */

		if err != nil {
			return retry.NonRetryableError(err)
		}

		_, err = ThingOperation(conn, d.Id())

		if err != nil {
			if iamwaiterRetry && /* eventual consistency error checking */ {
				return retry.RetryableError(err)
			}

			return retry.NonRetryableError(err)
		}

		return nil
	})

	if tfresource.TimedOut(err) {
		_, err = conn./* ... AWS Go SDK operation without eventual consistency errors ... */

		if err != nil {
			return err
		}

		_, err = ThingOperation(conn, d.Id())

		if err != nil {
			return err
		}
	}
```

### Resource Lifecycle Retries

Resource lifecycle eventual consistency is a type of consistency issue that relates to the existence or state of an AWS infrastructure component.
For example, if you create a resource and immediately try to get information about it, some AWS services and operations will return a "not found" error.
Depending on the service and general AWS load, these errors can be frequent or rare.

In order to avoid this issue, identify operations that make changes.
Then, when calling any other operations that rely on the changes, account for the possibility that the AWS service has not yet fully realized them.

Handling eventual consistency looks slightly different for Terraform Plugin Framework based resources versus Plugin SDK V2. For Terraform Framework based resources, a `Get`/`Describe` API call should be made after the create request completes, all within the `Create` method. For Terraform Plugin SDK V2 resources, the `Create` function should return by calling the `Read` function. Both approaches fill in computed attributes and ensure that the AWS service applied the configuration correctly. Add retry logic to the `Get`/`Describe` API call (Plugin Framework) or `Read` function (Plugin SDK V2) to overcome the temporary condition on resource creation.

!!! note
    For eventually consistent resources, "not found" errors can still occur in the `Read` function even after implementing [Resource Lifecycle Waiters](#resource-lifecycle-waiters).

```go
const (
	// Maximum amount of time to wait for Thing eventual consistency on creation
	ThingCreationTimeout = 2 * time.Minute
)
```

=== "Terraform Plugin Framework (Preferred)"
    ```go
    // internal/service/{service}/{thing}.go

    func (r *resourceThing) Create(ctx context.Context, req resource.CreateRequest, resp *resource.CreateResponse) {
    	conn := meta.(*AWSClient).ExampleClient()

    	// ...Creation steps...

    	input := &example.OperationInput{/* ... */}

    	var output *example.OperationOutput
        createTimeout := r.CreateTimeout(ctx, plan.Timeouts)
    	err := retry.RetryContext(ctx, createTimeout, func() *retry.RetryError {
    		var err error
    		output, err = conn.Operation(input)

    		if errs.IsA[*types.ResourceNotFoundException(err) {
    			return retry.RetryableError(err)
    		}

    		if err != nil {
    			return retry.NonRetryableError(err)
    		}

    		return nil
    	})

    	// Retry AWS Go SDK operation if no response from automatic retries.
    	if tfresource.TimedOut(err) {
    		output, err = exampleconn.Operation(input)
    	}

    	if err != nil {
            resp.Diagnostics.AddError(
                create.ProblemStandardMessage(names.Example, create.ErrActionWaitingForCreation, ResNameThing, plan.ID.String(), err),
                err.Error(),
            )
            return
    	}

    	// Prevent panics.
    	if output == nil {
            resp.Diagnostics.AddError(
                create.ProblemStandardMessage(names.Example, create.ErrActionWaitingForCreation, ResNameThing, plan.ID.String(), errors.New("empty output")),
                err.Error(),
            )
            return
    	}

    	// ... refresh Terraform state as normal ...
    }
    ```

=== "Terraform Plugin SDK V2"
    ```go
    // internal/service/{service}/{thing}.go

    function ExampleThingCreate(ctx context.Context, d *schema.ResourceData, meta interface{}) diag.Diagnostics {
		var diags diag.Diagnostics
    	// ...
    	return append(diags, ExampleThingRead(ctx, d, meta)...)
    }

    function ExampleThingRead(ctx context.Context, d *schema.ResourceData, meta interface{}) diag.Diagnostics {
		var diags diag.Diagnostics

    	conn := meta.(*AWSClient).ExampleConn()

    	input := &example.OperationInput{/* ... */}

    	var output *example.OperationOutput
    	err := retry.RetryContext(ctx, ThingCreationTimeout, func() *retry.RetryError {
    		var err error
    		output, err = conn.Operation(input)

    		// Retry on any API "not found" errors, but only on new resources.
    		if d.IsNewResource() && tfawserr.ErrorCodeEquals(err, example.ErrCodeResourceNotFoundException) {
    			return retry.RetryableError(err)
    		}

    		if err != nil {
    			return retry.NonRetryableError(err)
    		}

    		return nil
    	})

    	// Retry AWS Go SDK operation if no response from automatic retries.
    	if tfresource.TimedOut(err) {
    		output, err = exampleconn.Operation(input)
    	}

    	// Prevent confusing Terraform error messaging to operators by
    	// Only ignoring API "not found" errors if not a new resource.
    	if !d.IsNewResource() && tfawserr.ErrorCodeEquals(err, example.ErrCodeNoSuchEntityException) {
    		log.Printf("[WARN] Example Thing (%s) not found, removing from state", d.Id())
    		d.SetId("")
    		return diags
    	}

    	if err != nil {
    		return sdkdiag.AppendErrorf(diags, "reading Example Thing (%s): %w", d.Id(), err)
    	}

    	// Prevent panics.
    	if output == nil {
    		return sdkdiag.AppendErrorf(diags, "reading Example Thing (%s): empty response", d.Id())
    	}

    	// ... refresh Terraform state as normal ...
    	d.Set("arn", output.Arn)
    }
    ```

    Some other general guidelines are:
    
    - If the `Create` function uses `retry.StateChangeConf`, the underlying `resource.RefreshStateFunc` should `return nil, "", nil` instead of the API "not found" error. This way the `StateChangeConf` logic will automatically retry.
    - If the `Create` function uses `retry.RetryContext()`, the API "not found" error should be caught and `return retry.RetryableError(err)` to automatically retry.
    
    In rare cases, it may be easier to duplicate all `Read` function logic in the `Create` function to handle all retries in one place.

### Resource Attribute Value Waiters

An emergent solution for handling eventual consistency with attribute values on updates is to introduce a custom `retry.StateChangeConf` and `resource.RefreshStateFunc` handlers. For example, the waiting logic can be implemented as:

    ```go
    // ThingAttribute fetches the Thing and its Attribute
    func ThingAttribute(ctx context.Context, conn *example.Client, id string) retry.StateRefreshFunc {
        return func() (interface{}, string, error) {
            output, err := /* ... AWS Go SDK operation to fetch resource/value ... */

    		if errs.IsA[*types.ResourceNotFoundException](err) {
    			return nil, "", nil
    		}
    
    		if err != nil {
    			return nil, "", err
    		}
    
    		if output == nil {
    			return nil, "", nil
    		}
    
    		return output, aws.ToString(output.Attribute), nil
    	}
    }
    
    // waitThingAttributeUpdated is an attribute waiter for Thing.Attribute
    func waitThingAttributeUpdated(ctx context.Context, conn *example.Example, id string, expectedValue string, timeout time.Duration) (*example.Thing, error) {
    	stateConf := &retry.StateChangeConf{
    		Target:  []string{expectedValue},
    		Refresh: ThingAttribute(ctx, conn, id),
    		Timeout: timeout,
    	}
    
    	outputRaw, err := stateConf.WaitForState()
    
    	if output, ok := outputRaw.(*example.Thing); ok {
    		return output, err
    	}
    
    	return nil, err
    }
    ```

And consumed within the resource update workflow as follows:

=== "Terraform Plugin Framework (Preferred)"
    ```go
    func (r *resourceThing) Update(ctx context.Context, req resource.UpdateRequest, resp resource.UpdateResponse) {
        // ...

    	!plan.Attribute.Equal(state.Attribute) {
    		// ... AWS Go SDK logic to update attribute ...

            updateTimeout := r.UpdateTimeout(ctx, plan.Timeouts)
    		if _, err := waitThingAttributeUpdated(ctx, conn, plan.ID.StringValue(), plan.Attribute.StringValue(), updateTimeout); err != nil {
                resp.Diagnostics.AddError(
                    create.ProblemStandardMessage(names.Example, create.ErrActionWaitingForUpdate, ResNameThing, plan.ID.String(), err),
                    err.Error(),
                )
            return
    		}
    	}

    	// ...
    }
    ```

=== "Terraform Plugin SDK V2"
    ```go
    function resourceThingUpdate(ctx context.Context, d *schema.ResourceData, meta interface{}) diags.Diagnostics {
        // ...

    	d.HasChange("attribute") {
    		// ... AWS Go SDK logic to update attribute ...

    		if _, err := waitThingAttributeUpdated(ctx, conn, d.Id(), d.Get("attribute").(string), d.Timeout(schema.TimeoutUpdate)); err != nil {
                return create.AppendDiagError(diags, names.Example, create.ErrActionWaitingForUpdate, ResNameThing, d.Id(), err)
    		}
    	}

    	// ...
    }
    ```

## Asynchronous Operations

When you initiate a long-running operation, an AWS service may return a successful response immediately and continue working on the request asynchronously. A resource can track the status with a component-level field (e.g., `CREATING`, `UPDATING`, etc.) or an explicit tracking identifier.

Terraform resources should wait for these background operations to complete. Failing to do so can introduce incomplete state information and downstream errors in other resources. In rare scenarios involving very long-running operations, operators may request a flag to skip the waiting. However, these should only be implemented case-by-case to prevent those previously mentioned confusing issues.

### AWS Go SDK Waiters

In limited cases, the AWS service API model includes the information to automatically generate a waiter function in the AWS Go SDK for an operation. These are typically named with the prefix `WaitUntil...`. If available, these functions can be used for an initial resource implementation. For example:

```go
if err := conn.WaitUntilEndpointInService(input); err != nil {
	return fmt.Errorf("waiting for Example Thing (%s) ...: %w", d.Id(), err)
}
```

If it is necessary to customize the timeouts and polling, we generally prefer using [Resource Lifecycle Waiters](#resource-lifecycle-waiters) instead since they are more commonly used throughout the codebase.

### Resource Lifecycle Waiters

Most of the codebase uses `retry.StateChangeConf` and `retry.StateRefreshFunc` handlers for tracking either component-level status fields or explicit tracking identifiers.
These should be placed in the `internal/service/{SERVICE}` package and split into separate functions. For example:

    ```go
    // ThingStatus fetches the Thing and its Status
    func ThingStatus(ctx context.Context, conn *example.Client, id string) retry.StateRefreshFunc {
        return func() (interface{}, string, error) {
            output, err := /* ... AWS Go SDK operation to fetch resource/status ... */

            if errs.IsA[*types.ResourceNotFoundException](err) {
    			return nil, "", nil
    		}

    		if err != nil {
    			return nil, "", err
    		}

    		if output == nil {
    			return nil, "", nil
    		}

    		return output, aws.ToString(output.Status), nil
    	}
    }
    ```

```go
// waitThingCreated is a resource waiter for Thing creation
func waitThingCreated(ctx context.Context, conn *example.Example, id string, timeout time.Duration) (*example.Thing, error) {
	stateConf := &retry.StateChangeConf{
		Pending: []string{example.StatusCreating},
		Target:  []string{example.StatusCreated},
		Refresh: ThingStatus(ctx, conn, id),
		Timeout: timeout,
	}

	outputRaw, err := stateConf.WaitForState()

	if output, ok := outputRaw.(*example.Thing); ok {
		return output, err
	}

	return nil, err
}

// waitThingDeleted is a resource waiter for Thing deletion
func waitThingDeleted(ctx context.Context, conn *example.Example, id string, timeout time.Duration) (*example.Thing, error) {
	stateConf := &retry.StateChangeConf{
		Pending: []string{example.StatusDeleting},
		Target:  []string{}, // Use empty list if the resource disappears and does not have "deleted" status
		Refresh: ThingStatus(conn, id),
		Timeout: timeout,
	}

	outputRaw, err := stateConf.WaitForState()

	if output, ok := outputRaw.(*example.Thing); ok {
		return output, err
	}

	return nil, err
}
```

=== "Terraform Plugin Framework (Preferred)"
    ```go
    func (r *resourceThing) Create(ctx context.Context, req resource.CreateRequest, resp resource.CreateResponse) {
        // ... AWS Go SDK logic to create resource ...

        createTimeout := r.CreateTimeout(ctx, plan.Timeouts)
        if _, err = waitThingCreated(ctx, conn, plan.ID.ValueString(), createTimeout); err != nil {
            resp.Diagnostics.AddError(
                create.ProblemStandardMessage(names.Example, create.ErrActionWaitingForCreation, ResNameThing, plan.ID.String(), err),
                err.Error(),
            )
            return
        }

    	resp.Diagnostics.Append(resp.State.Set(ctx, plan)...)
    }

    func (r *resourceThing) Delete(ctx context.Context, req resource.DeleteRequest, resp *resource.DeleteResponse) {
        // ... AWS Go SDK logic to delete resource ...

        deleteTimeout := r.DeleteTimeout(ctx, plan.Timeouts)
        if _, err = waitThingDeleted(ctx, conn, plan.ID.ValueString(), deleteTimeout); err != nil {
            resp.Diagnostics.AddError(
                create.ProblemStandardMessage(names.Example, create.ErrActionWaitingForDeletion, ResNameThing, plan.ID.String(), err),
                err.Error(),
            )
            return
        }
    }
    ```

=== "Terraform Plugin SDK V2"
    ```go
    func resourceThingCreate(ctx context.Context, d *schema.ResourceData, meta interface{}) diag.Diagnostics {
        var diags diag.Diagnostics

        // ... AWS Go SDK logic to create resource ...

    	if _, err := waitThingCreated(ctx, conn, d.Id(), d.Timeout(schema.TimeoutCreate)) {
            return create.AppendDiagError(diags, names.Example, create.ErrActionWaitingForCreation, ResNameThing, d.Id(), err)
    	}

    	return append(diags, ExampleThingRead(ctx, d, meta)...)
    }

    func resourceThingDelete(ctx context.Context, d *schema.ResourceData, meta interface{}) diag.Diagnostics {
        // ... AWS Go SDK logic to delete resource ...

    	if _, err := waitThingDeleted(conn, d.Id(), d.Timeout(schema.TimeoutDelete)); err != nil {
            return create.AppendDiagError(diags, names.Example, create.ErrActionWaitingForDeletion, ResNameThing, d.Id(), err)
    	}

    	return diags
    }
    ```

Typically, the AWS Go SDK should include constants for various status field values (e.g., `StatusCreating` for `CREATING`). If not, create them in a file named `internal/service/{SERVICE}/consts.go`.
# Running and Writing Acceptance Tests

Terraform includes an acceptance test harness that does most of the repetitive
work involved in testing a resource. For additional information about testing
Terraform Providers, see the [SDKv2 documentation](https://www.terraform.io/plugin/sdkv2/testing).

## In context

To help place acceptance testing in context, here is an overview of the Terraform AWS Provider's three types of tests.

1. **Acceptance tests** (_You are here!_) are end-to-end evaluations of interactions with AWS. They validate functionalities like creating, reading, and destroying resources within AWS.
2. [**Unit tests**](unit-tests.md) focus on testing isolated units of code within the software, typically at the function level. They assess functionalities solely within the provider itself.
3. [**Continuous integration tests**](continuous-integration.md) encompass a suite of automated tests that are executed on every pull request and include linting, compiling code, running unit tests, and performing static analysis.

## Acceptance Tests Often Cost Money to Run

Our acceptance test suite creates real resources, and as a result, they cost real money to run.
Because the resources only exist for a short period of time, the total amount
of money required is usually relatively small. That said there are particular services
which are very expensive to run and it's important to be prepared for those costs.

Some services which can be cost-prohibitive include (among others):

- ACM (Amazon Certificate Manager)
- Bedrock
- EC2
- ElastiCache
- FSx
- Glue
- Kinesis Analytics
- OpenSearch
- RDS
- Storage Gateway
- WorkSpaces

We don't want financial limitations to be a barrier to contribution, so if you are unable to
pay to run acceptance tests for your contribution, mention this in your
pull request. We will happily accept "best effort" implementations of
acceptance tests and run them for you on our side. This might mean that your PR
takes a bit longer to merge, but it most definitely is not a blocker for
contributions.

## Running an Acceptance Test

Acceptance tests can be run using the `testacc` target in the Terraform
`Makefile`. The individual tests to run can be controlled using a regular
expression. Prior to running the tests provider configuration details such as
access keys must be made available as environment variables.

For example, to run an acceptance test against the Amazon Web Services
provider, the following environment variables must be set:

```sh
# Using a profile
export AWS_PROFILE=...
# Otherwise
export AWS_ACCESS_KEY_ID=...
export AWS_SECRET_ACCESS_KEY=...
export AWS_DEFAULT_REGION=...
```

Please note that the default region for the testing is `us-west-2` and must be
overridden via the `AWS_DEFAULT_REGION` environment variable, if necessary. This
is especially important for testing AWS GovCloud (US), which requires:

```sh
export AWS_DEFAULT_REGION=us-gov-west-1
```

Tests can then be run by specifying a regular expression defining the tests to
run and the package in which the tests are defined:

```console
make testacc TESTS=TestAccCloudWatchDashboard_updateName PKG=cloudwatch
```

```
==> Checking that code complies with gofmt requirements...
TF_ACC=1 go test ./internal/service/cloudwatch/... -v -count 1 -parallel 20 -run=TestAccCloudWatchDashboard_updateName -timeout 180m
=== RUN   TestAccCloudWatchDashboard_updateName
=== PAUSE TestAccCloudWatchDashboard_updateName
=== CONT  TestAccCloudWatchDashboard_updateName
--- PASS: TestAccCloudWatchDashboard_updateName (25.33s)
PASS
ok  	github.com/hashicorp/terraform-provider-aws/internal/service/cloudwatch	25.387s
```

Entire resource test suites can be targeted by using the naming convention to
write the regular expression. For example, to run all tests of the
`aws_cloudwatch_dashboard` resource rather than just the `updateName` test, you
can start testing like this:

```console
make testacc TESTS=TestAccCloudWatchDashboard PKG=cloudwatch
```

```
==> Checking that code complies with gofmt requirements...
TF_ACC=1 go test ./internal/service/cloudwatch/... -v -count 1 -parallel 20 -run=TestAccCloudWatchDashboard -timeout 180m
=== RUN   TestAccCloudWatchDashboard_basic
=== PAUSE TestAccCloudWatchDashboard_basic
=== RUN   TestAccCloudWatchDashboard_update
=== PAUSE TestAccCloudWatchDashboard_update
=== RUN   TestAccCloudWatchDashboard_updateName
=== PAUSE TestAccCloudWatchDashboard_updateName
=== CONT  TestAccCloudWatchDashboard_basic
=== CONT  TestAccCloudWatchDashboard_updateName
=== CONT  TestAccCloudWatchDashboard_update
--- PASS: TestAccCloudWatchDashboard_basic (15.83s)
--- PASS: TestAccCloudWatchDashboard_updateName (26.69s)
--- PASS: TestAccCloudWatchDashboard_update (27.72s)
PASS
ok  	github.com/hashicorp/terraform-provider-aws/internal/service/cloudwatch	27.783s
```

Running acceptance tests requires version 0.12.26 or higher of the Terraform CLI to be installed.

For advanced developers, the acceptance testing framework accepts some additional environment variables that can be used to control Terraform CLI binary selection, logging, and other behaviors. See the [SDKv2 documentation](https://www.terraform.io/plugin/sdkv2/testing/acceptance-tests#environment-variables) for more information.

Please Note: On macOS 10.14 and later (and some Linux distributions), the default user open file limit is 256. This may cause unexpected issues when running the acceptance testing since this can prevent various operations from occurring such as opening network connections to AWS. To view this limit, the `ulimit -n` command can be run. To update this limit, run `ulimit -n 1024`  (or higher).

### Running Cross-Account Tests

Certain testing requires multiple AWS accounts. This additional setup is not typically required and the testing will return an error (shown below) if your current setup does not have the secondary AWS configuration:

```console
make testacc TESTS=TestAccRDSInstance_DBSubnetGroupName_ramShared PKG=rds
```

```
TF_ACC=1 go test ./internal/service/rds/... -v -count 1 -parallel 20 -run=TestAccRDSInstance_DBSubnetGroupName_ramShared -timeout 180m
=== RUN   TestAccRDSInstance_DBSubnetGroupName_ramShared
=== PAUSE TestAccRDSInstance_DBSubnetGroupName_ramShared
=== CONT  TestAccRDSInstance_DBSubnetGroupName_ramShared
    acctest.go:674: skipping test because at least one environment variable of [AWS_ALTERNATE_PROFILE AWS_ALTERNATE_ACCESS_KEY_ID] must be set. Usage: credentials for running acceptance testing in alternate AWS account.
--- SKIP: TestAccRDSInstance_DBSubnetGroupName_ramShared (0.85s)
PASS
ok      github.com/hashicorp/terraform-provider-aws/internal/service/rds        0.888s
```

Running these acceptance tests is the same as before, except the following additional AWS credential information is required:

```sh
# Using a profile
export AWS_ALTERNATE_PROFILE=...
# Otherwise
export AWS_ALTERNATE_ACCESS_KEY_ID=...
export AWS_ALTERNATE_SECRET_ACCESS_KEY=...
```

### Running Cross-Region Tests

Certain testing requires multiple AWS regions. Additional setup is not typically required because the testing defaults the second AWS region to `us-east-1` and the third AWS region to `us-east-2`.

Running these acceptance tests is the same as before, but if you wish to override the second and third regions:

```sh
export AWS_ALTERNATE_REGION=...
export AWS_THIRD_REGION=...
```

### Running Only Short Tests

Some tests have been manually marked as long-running (longer than 300 seconds) and can be skipped using the `-short` flag. However, we are adding long-running guards little by little and many services have no guarded tests.

Where guards have been implemented, do not always skip long-running tests. However, for intermediate test runs during development, or to verify functionality unrelated to the specific long-running tests, skipping long-running tests makes work more efficient. We recommend that for the final test run before submitting a PR you run affected tests without the `-short` flag.

If you want to run only short-running tests, you can use either one of these equivalent statements. Note the use of `-short`.

For example:

```console
make testacc TESTS='TestAccECSTaskDefinition_' PKG=ecs TESTARGS=-short
```

Or:

```console
TF_ACC=1 go test ./internal/service/ecs/... -v -count 1 -parallel 20 -run='TestAccECSTaskDefinition_' -short -timeout 180m
```

## Writing an Acceptance Test

Terraform has a framework for writing acceptance tests which minimizes the
amount of boilerplate code necessary to use common testing patterns. This guide is meant to augment the general [SDKv2 documentation](https://www.terraform.io/plugin/sdkv2/testing/acceptance-tests) with Terraform AWS Provider specific conventions and helpers.

### Anatomy of an Acceptance Test

This section describes in detail how the Terraform acceptance testing framework operates with respect to the Terraform AWS Provider. We recommend those unfamiliar with this provider, or Terraform resource testing in general, take a look here first to generally understand how we interact with AWS and the resource code to verify functionality.

The entry point to the framework is the `resource.ParallelTest()` function. This wraps our testing to work with the standard Go testing framework, while also preventing unexpected usage of AWS by requiring the `TF_ACC=1` environment variable. This function accepts a `TestCase` parameter, which has all the details about the test itself. For example, this includes the test steps (`TestSteps`) and how to verify resource deletion in the API after all steps have been run (`CheckDestroy`).

Each `TestStep` proceeds by applying some
Terraform configuration using the provider under test, and then verifying that
results are as expected by making assertions using the provider API. It is
common for a single test function to exercise both the creation of and updates
to a single resource. Most tests follow a similar structure.

1. Pre-flight checks are made to ensure that sufficient provider configuration
   is available to be able to proceed - for example in an acceptance test
   targeting AWS, `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY` must be set prior
   to running acceptance tests. This is common to all tests exercising a single
   provider.

Most assertion
functions are defined out of band with the tests. This keeps the tests
readable, and allows reuse of assertion functions across different tests of the
same type of resource. The definition of a complete test looks like this:

```go
func TestAccCloudWatchDashboard_basic(t *testing.T) {
  ctx := acctest.Context(t)
	var dashboard cloudwatch.GetDashboardOutput
	rInt := acctest.RandInt()

	resource.ParallelTest(t, resource.TestCase{
		PreCheck:                 func() { acctest.PreCheck(ctx, t) },
		ErrorCheck:               acctest.ErrorCheck(t, names.CloudWatchServiceID),
		ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
		CheckDestroy:             testAccCheckDashboardDestroy(ctx),
		Steps: []resource.TestStep{
			{
				Config: testAccDashboardConfig(rInt),
				Check: resource.ComposeTestCheckFunc(
					testAccCheckDashboardExists(ctx, "aws_cloudwatch_dashboard.foobar", &dashboard),
					resource.TestCheckResourceAttr("aws_cloudwatch_dashboard.foobar", "dashboard_name", testAccDashboardName(rInt)),
				),
			},
		},
	})
}
```

When executing the test, the following steps are taken for each `TestStep`:

1. The Terraform configuration required for the test is applied. This is
   responsible for configuring the resource under test, and any dependencies it
   may have. For example, to test the `aws_cloudwatch_dashboard` resource, a valid configuration with the requisite fields is required. This results in a configuration which looks like this:

    ```terraform
    resource "aws_cloudwatch_dashboard" "foobar" {
      dashboard_name = "terraform-test-dashboard-%[1]d"
      dashboard_body = <<EOF
      {
        "widgets": [{
          "type": "text",
          "x": 0,
          "y": 0,
          "width": 6,
          "height": 6,
          "properties": {
            "markdown": "Hi there from Terraform: CloudWatch"
          }
        }]
      }
      EOF
    }
    ```

1. Assertions are run using the provider API. These use the provider API
   directly rather than asserting against the resource state. For example, to
   verify that the `aws_cloudwatch_dashboard` described above was created
   successfully, a test function like this is used:

    ```go
    func testAccCheckDashboardExists(ctx context.Context, n string, dashboard *cloudwatch.GetDashboardOutput) resource.TestCheckFunc {
      return func(s *terraform.State) error {
        rs, ok := s.RootModule().Resources[n]
        if !ok {
          return fmt.Errorf("Not found: %s", n)
        }

        conn := acctest.Provider.Meta().(*conns.AWSClient).CloudWatchConn(ctx)
        params := cloudwatch.GetDashboardInput{
          DashboardName: aws.String(rs.Primary.ID),
        }

        resp, err := conn.GetDashboardWithContext(ctx, &params)
        if err != nil {
          return err
        }

        *dashboard = *resp

        return nil
      }
    }
    ```

   Notice that the only information used from the Terraform state is the ID of
   the resource. For computed properties, we instead assert that the value saved in the Terraform state was the
   expected value if possible. The testing framework provides helper functions
   for several common types of checks - for example:

   ```go
   resource.TestCheckResourceAttr("aws_cloudwatch_dashboard.foobar", "dashboard_name", testAccDashboardName(rInt)),
   ```

1. The resources created by the test are destroyed. This step happens
   automatically, and is the equivalent of calling `terraform destroy`.

1. Assertions are made against the provider API to verify that the resources
   have indeed been removed. If these checks fail, the test fails and reports
   "dangling resources". The code to ensure that the `aws_cloudwatch_dashboard` shown
   above has been destroyed looks like this:

    ```go
    func testAccCheckDashboardDestroy(ctx context.Context) resource.TestCheckFunc {
	    return func(s *terraform.State) error {
        conn := acctest.Provider.Meta().(*conns.AWSClient).CloudWatchConn(ctx)

        for _, rs := range s.RootModule().Resources {
          if rs.Type != "aws_cloudwatch_dashboard" {
            continue
          }

          params := cloudwatch.GetDashboardInput{
            DashboardName: aws.String(rs.Primary.ID),
          }

          _, err := conn.GetDashboardWithContext(ctx, &params)
          if err == nil {
            return fmt.Errorf("Dashboard still exists: %s", rs.Primary.ID)
          }
          if !isDashboardNotFoundErr(err) {
            return err
          }
        }

        return nil
      }
    }
    ```

   These functions usually test only for the resource directly under test.

### Resource Acceptance Testing

Most resources that implement standard Create, Read, Update, and Delete functionality should follow the pattern below. Each test type has a section that describes them in more detail:

- **basic**: This represents the bare minimum verification that the resource can be created, read, deleted, and optionally imported.
- **disappears**: A test that verifies Terraform will offer to recreate a resource if it is deleted outside of Terraform (e.g., via the Console) instead of returning an error that it cannot be found.
- **Per Attribute**: A test that verifies the resource with a single additional argument can be created, read, optionally updated (or force resource recreation), deleted, and optionally imported.

The leading sections below highlight additional recommended patterns.

#### Test Configurations

Most of the existing test configurations you will find in the Terraform AWS Provider are written in the following function-based style:

```go
func TestAccExampleThing_basic(t *testing.T) {
  // ... omitted for brevity ...

  resource.ParallelTest(t, resource.TestCase{
    // ... omitted for brevity ...
    Steps: []resource.TestStep{
      {
        Config: testAccExampleThingConfig(),
        // ... omitted for brevity ...
      },
    },
  })
}

func testAccExampleThingConfig() string {
  return `
resource "aws_example_thing" "test" {
  # ... omitted for brevity ...
}
`
}
```

Even when no values need to be passed in to the test configuration, we have found this setup to be the most flexible for allowing that to be easily implemented. Any configurable values are handled via `fmt.Sprintf()`. Using `text/template` or other templating styles is explicitly forbidden.

For consistency, resources in the test configuration should be named `resource "..." "test"` unless multiple of that resource are necessary.

We discourage re-using test configurations across test files (except for some common configuration helpers we provide) as it is much harder to discover potential testing regressions.

Please also note that the newline on the first line of the configuration (before `resource`) and the newline after the last line of configuration (after `}`) are important to allow test configurations to be easily combined without generating Terraform configuration language syntax errors.

#### Test Configuration Independence

_Across the entire provider_, all test configurations should be as independent of each other as possible. For example, a common place this concept comes up is with the default VPC. Since we have tests that reconfigure the default VPC, if your configuration requires a VPC, it should not rely on the default VPC. Instead, include a VPC that will be created and destroyed as part of the test.

Make sure that your test configuration:

1. Includes everything required for Terraform to run the test
1. Does not assume that any user-managed infrastructure will be in place, such as S3 buckets, IAM roles, KMS keys, VPCs, subnets, etc.

#### Combining Test Configurations

We include a helper function, `acctest.ConfigCompose()` for iteratively building and chaining test configurations together. It accepts any number of configurations to combine them. This simplifies a single resource's testing by allowing the creation of a "base" test configuration for all the other test configurations (if necessary) and also allows the maintainers to curate common configurations. Each of these is described in more detail in the below sections.

Please note that we do discourage _excessive_ chaining of configurations such as implementing multiple layers of "base" configurations. Usually these configurations are harder for maintainers and other future readers to understand due to the multiple levels of indirection.

##### Base Test Configurations

If a resource requires the same Terraform configuration as a prerequisite for all test configurations, then a common pattern is implementing a "base" test configuration that is combined with each test configuration.

For example:

```go
func testAccExampleThingConfigBase() string {
  return `
resource "aws_iam_role" "test" {
  # ... omitted for brevity ...
}

resource "aws_iam_role_policy" "test" {
  # ... omitted for brevity ...
}
`
}

func testAccExampleThingConfig() string {
  return acctest.ConfigCompose(
    testAccExampleThingConfigBase(),
    `
resource "aws_example_thing" "test" {
  # ... omitted for brevity ...
}
`)
}
```

##### Available Common Test Configurations

These test configurations are typical implementations we have found or allow testing to implement best practices easier, since the Terraform AWS Provider testing is expected to run against various AWS Regions and Partitions.

- `acctest.AvailableEC2InstanceTypeForRegion("type1", "type2", ...)`: Typically used to replace hardcoded EC2 Instance Types. Uses `aws_ec2_instance_type_offering` data source to return an available EC2 Instance Type in preferred ordering. Reference the instance type via: `data.aws_ec2_instance_type_offering.available.instance_type`. Use `acctest.AvailableEC2InstanceTypeForRegionNamed("name", "type1", "type2", ...)` to specify a name for the data source
- `acctest.ConfigLatestAmazonLinuxHVMEBSAMI()`: Typically used to replace hardcoded EC2 Image IDs (`ami-12345678`). Uses `aws_ami` data source to find the latest Amazon Linux image. Reference the AMI ID via: `data.aws_ami.amzn-ami-minimal-hvm-ebs.id`

#### Randomized Naming

For AWS resources that require unique naming, the tests should implement a randomized name, typically coded as a `rName` variable in the test and passed as a parameter to create the test configuration.

For example:

```go
func TestAccExampleThing_basic(t *testing.T) {
  ctx := acctest.Context(t)
  rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)
  // ... omitted for brevity ...

  resource.ParallelTest(t, resource.TestCase{
    // ... omitted for brevity ...
    Steps: []resource.TestStep{
      {
        Config: testAccExampleThingConfigName(rName),
        // ... omitted for brevity ...
      },
    },
  })
}

func testAccExampleThingConfigName(rName string) string {
  return fmt.Sprintf(`
resource "aws_example_thing" "test" {
  name = %[1]q
}
`, rName)
}
```

Typically the `rName` is always the first argument to the test configuration function, if used, for consistency.

Note that if `rName` (or any other variable) is used multiple times in the `fmt.Sprintf()` statement, _do not_ repeat `rName` in the `fmt.Sprintf()` arguments. Using `fmt.Sprintf(..., rName, rName)`, for example, would not be correct. Instead, use the indexed `%[1]q` (or `%[x]q`, `%[x]s`, `%[x]t`, or `%[x]d`, where `x` represents the index number) verb multiple times. For example:

```go
func testAccExampleThingConfigName(rName string) string {
  return fmt.Sprintf(`
resource "aws_example_thing" "test" {
  name = %[1]q

  tags = {
    Name = %[1]q
  }
}
`, rName)
}
```

#### Other Recommended Variables

We also typically recommend saving a `resourceName` variable in the test that contains the resource reference, e.g., `aws_example_thing.test`, which is repeatedly used in the checks.

For example:

```go
func TestAccExampleThing_basic(t *testing.T) {
  ctx := acctest.Context(t)
  // ... omitted for brevity ...
  resourceName := "aws_example_thing.test"

  resource.ParallelTest(t, resource.TestCase{
    // ... omitted for brevity ...
    Steps: []resource.TestStep{
      {
        // ... omitted for brevity ...
        Check: resource.ComposeTestCheckFunc(
          testAccCheckExampleThingExists(ctx, resourceName),
          acctest.CheckResourceAttrRegionalARN(resourceName, "arn", "example", fmt.Sprintf("thing/%s", rName)),
          resource.TestCheckResourceAttr(resourceName, "description", ""),
          resource.TestCheckResourceAttr(resourceName, "name", rName),
        ),
      },
      {
        ResourceName:      resourceName,
        ImportState:       true,
        ImportStateVerify: true,
      },
    },
  })
}

// below all TestAcc functions

func testAccExampleThingConfigName(rName string) string {
  return fmt.Sprintf(`
resource "aws_example_thing" "test" {
  name = %[1]q
}
`, rName)
}
```

#### Basic Acceptance Tests

Usually this test is implemented first. The test configuration should contain only required arguments (`Required: true` attributes) and it should check the values of all read-only attributes (`Computed: true` without `Optional: true`). If the resource supports it, it verifies import. It should _NOT_ perform other `TestStep` such as updates or verify recreation.

These are typically named `TestAcc{SERVICE}{THING}_basic`, e.g., `TestAccCloudWatchDashboard_basic`

For example:

```go
func TestAccExampleThing_basic(t *testing.T) {
  ctx := acctest.Context(t)
  rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)
  resourceName := "aws_example_thing.test"

  resource.ParallelTest(t, resource.TestCase{
    PreCheck:                 func() { acctest.PreCheck(ctx, t) },
    ErrorCheck:               acctest.ErrorCheck(t, names.ExampleServiceID),
		ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
    CheckDestroy:             testAccCheckExampleThingDestroy(ctx),
    Steps: []resource.TestStep{
      {
        Config: testAccExampleThingConfigName(rName),
        Check: resource.ComposeTestCheckFunc(
          testAccCheckExampleThingExists(ctx, resourceName),
          acctest.CheckResourceAttrRegionalARN(resourceName, "arn", "example", fmt.Sprintf("thing/%s", rName)),
          resource.TestCheckResourceAttr(resourceName, "description", ""),
          resource.TestCheckResourceAttr(resourceName, "name", rName),
        ),
      },
      {
        ResourceName:      resourceName,
        ImportState:       true,
        ImportStateVerify: true,
      },
    },
  })
}

// below all TestAcc functions

func testAccExampleThingConfigName(rName string) string {
  return fmt.Sprintf(`
resource "aws_example_thing" "test" {
  name = %[1]q
}
`, rName)
}
```

#### PreChecks

Acceptance test cases have a PreCheck. The PreCheck ensures that the testing environment meets certain preconditions. If the environment does not meet the preconditions, Go skips the test. Skipping a test avoids reporting a failure and wasting resources where the test cannot succeed.

Here is an example of the default PreCheck:

```go
func TestAccExampleThing_basic(t *testing.T) {
  ctx := acctest.Context(t)
  rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)
  resourceName := "aws_example_thing.test"

  resource.ParallelTest(t, resource.TestCase{
    PreCheck:     func() { acctest.PreCheck(ctx, t) },
    // ... additional checks follow ...
  })
}
```

Extend the default PreCheck by adding calls to functions in the anonymous PreCheck function. The functions can be existing functions in the provider or custom functions you add for new capabilities.

##### Standard Provider PreChecks

If you add a new test that has preconditions which are checked by an existing provider function, use that standard PreCheck instead of creating a new one. Some existing tests are missing standard PreChecks and you can help by adding them where appropriate.

These are some of the standard provider PreChecks:

* `acctest.PreCheckRegion(t *testing.T, regions ...string)` checks that the test region is one of the specified AWS Regions.
* `acctest.PreCheckRegionNot(t *testing.T, regions ...string)` checks that the test region is not one of the specified AWS Regions.
* `acctest.PreCheckAlternateRegionIs(t *testing.T, region string)` checks that the alternate test region is the specified AWS Region.
* `acctest.PreCheckPartition(t *testing.T, partition string)` checks that the test partition is the specified partition.
* `acctest.PreCheckPartitionNot(t *testing.T, partitions ...string)` checks that the test partition is not one of the specified partitions.
* `acctest.PreCheckPartitionHasService(t *testing.T, serviceID string)` checks whether the current partition lists the service as part of its offerings. Note: AWS may not add new or public preview services to the service list immediately. This function will return a false positive in that case.
* `acctest.PreCheckOrganizationsAccount(ctx context.Context, t *testing.T)` checks whether the current account can perform AWS Organizations tests.
* `acctest.PreCheckAlternateAccount(t *testing.T)` checks whether the environment is set up for tests across accounts.
* `acctest.PreCheckMultipleRegion(t *testing.T, regions int)` checks whether the environment is set up for tests across regions.

This is an example of using a standard PreCheck function. For an established service, such as WAF or FSx, use `acctest.PreCheckPartitionHasService()` and the service endpoint ID to check that a partition supports the service.

```go
func TestAccExampleThing_basic(t *testing.T) {
  ctx := acctest.Context(t)
  rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)
  resourceName := "aws_example_thing.test"

  resource.ParallelTest(t, resource.TestCase{
    PreCheck:     func() { acctest.PreCheck(ctx, t); acctest.PreCheckPartitionHasService(t, waf.EndpointsID) },
    // ... additional checks follow ...
  })
}
```

##### Custom PreChecks

In situations where standard PreChecks do not test for the required preconditions, create a custom PreCheck.

Below is an example of adding a custom PreCheck function. For a new or preview service that AWS does not include in the partition service list yet, you can verify the existence of the service with a simple read-only request (e.g., list all X service things). (For acceptance tests of established services, use `acctest.PreCheckPartitionHasService()` instead.)

```go
func TestAccExampleThing_basic(t *testing.T) {
  ctx := acctest.Context(t)
  rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)
  resourceName := "aws_example_thing.test"

  resource.ParallelTest(t, resource.TestCase{
    PreCheck:     func() { acctest.PreCheck(ctx, t), testAccPreCheckExample(ctx, t) },
    // ... additional checks follow ...
  })
}

func testAccPreCheckExample(ctx context.Context, t *testing.T) {
  conn := acctest.Provider.Meta().(*conns.AWSClient).ExampleConn(ctx)
	input := &example.ListThingsInput{}
	_, err := conn.ListThingsWithContext(ctx, input)
	if testAccPreCheckSkipError(err) {
		t.Skipf("skipping acceptance testing: %s", err)
	}
	if err != nil {
		t.Fatalf("unexpected PreCheck error: %s", err)
	}
}
```

#### ErrorChecks

Acceptance test cases have an ErrorCheck. The ErrorCheck provides a chance to take a look at errors before the test fails. While most errors should result in test failure, some should not. For example, an error that indicates an API operation is not supported in a particular region should cause the test to skip instead of fail. Since errors should flow through the ErrorCheck, do not handle the vast majority of failing conditions. Instead, in ErrorCheck, focus on the rare errors that should cause a test to skip, or in other words, be ignored.

##### Common ErrorCheck

In many situations, the common ErrorCheck is sufficient. It will skip tests for several normal occurrences such as when AWS reports a feature is not supported in the current region.

Here is an example of the common ErrorCheck:

```go
func TestAccExampleThing_basic(t *testing.T) {
  rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)
  resourceName := "aws_example_thing.test"

  resource.ParallelTest(t, resource.TestCase{
    // PreCheck
    ErrorCheck:   acctest.ErrorCheck(t, names.ExampleServiceID),
    // ... additional checks follow ...
  })
}
```

##### Service-Specific ErrorChecks

However, some services have special conditions that aren't caught by the common ErrorCheck. In these cases, you can create a service-specific ErrorCheck.

To add a service-specific ErrorCheck, follow these steps:

1. Make sure there is not already an ErrorCheck for the service you have in mind. For example, search the codebase for `acctest.RegisterServiceErrorCheckFunc(names.ExampleServiceID` replacing "service" with the package name of the service you're working on (e.g., `ec2`). If there is already an ErrorCheck for the service, add it to the existing service-specific ErrorCheck.
2. Create the service-specific ErrorCheck in an `_test.go` file for the service. See the example below.
3. Register the new service-specific ErrorCheck in the `init()` at the top of the `_test.go` file. See the example below.

An example of adding a service-specific ErrorCheck:

```go
// just after the imports, create or add to the init() function
func init() {
  acctest.RegisterServiceErrorCheck(names.ExampleServiceID, testAccErrorCheckSkipService)
}

// ... additional code and tests ...

// this is the service-specific ErrorCheck
func testAccErrorCheckSkipService(t *testing.T) resource.ErrorCheckFunc {
	return acctest.ErrorCheckSkipMessagesContaining(t,
		"Error message specific to the service that indicates unsupported features",
		"You can include from one to many portions of error messages",
		"Be careful to not inadvertently capture errors that should not be skipped",
	)
}
```

#### Long-Running Test Guards

For any acceptance tests that typically run longer than 300 seconds (5 minutes), add a `-short` test guard at the top of the test function.

For example:

```go
func TestAccExampleThing_longRunningTest(t *testing.T) {
  if testing.Short() {
    t.Skip("skipping long-running test in short mode")
  }

  // ... omitted for brevity ...

  resource.ParallelTest(t, resource.TestCase{
    // ... omitted for brevity ...
  })
}
```

When running acceptance tests, tests with these guards can be skipped using the Go `-short` flag. See [Running Only Short Tests](#running-only-short-tests) for examples.

#### Disappears Acceptance Tests

This test is generally implemented second. It is straightforward to set up once the basic test is passing since it can reuse that test configuration. It prevents a common bug report with Terraform resources that error when they can not be found (e.g., deleted outside Terraform).

These are typically named `TestAcc{SERVICE}{THING}_disappears`, e.g., `TestAccCloudWatchDashboard_disappears`

For example:

```go
func TestAccExampleThing_disappears(t *testing.T) {
  ctx := acctest.Context(t)
  rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)
  resourceName := "aws_example_thing.test"

  resource.ParallelTest(t, resource.TestCase{
    PreCheck:                 func() { acctest.PreCheck(ctx, t) },
    ErrorCheck:               acctest.ErrorCheck(t, names.ExampleServiceID),
		ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
    CheckDestroy:             testAccCheckExampleThingDestroy(ctx),
    Steps: []resource.TestStep{
      {
        Config: testAccExampleThingConfigName(rName),
        Check: resource.ComposeTestCheckFunc(
          testAccCheckExampleThingExists(ctx, resourceName, &job),
          acctest.CheckResourceDisappears(ctx, acctest.Provider, ResourceExampleThing(), resourceName),
        ),
        ExpectNonEmptyPlan: true,
      },
    },
  })
}
```

If this test does fail, the fix for this is generally adding error handling immediately after the `Read` API call that catches the error and tells Terraform to remove the resource before returning the error:

```go
output, err := conn.GetThing(input)

if !d.IsNewResource() && tfresource.NotFound(err) {
  log.Printf("[WARN] Example Thing (%s) not found, removing from state", d.Id())
  d.SetId("")
  return nil
}

if err != nil {
  return fmt.Errorf("reading Example Thing (%s): %w", d.Id(), err)
}
```

For children resources that are encapsulated by a parent resource, it is also preferable to verify that removing the parent resource will not generate an error either. These are typically named `TestAcc{SERVICE}{THING}_disappears_{PARENT}`, e.g., `TestAccRoute53ZoneAssociation_disappears_Vpc`

```go
func TestAccExampleChildThing_disappears_ParentThing(t *testing.T) {
  ctx := acctest.Context(t)
  rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)
  parentResourceName := "aws_example_parent_thing.test"
  resourceName := "aws_example_child_thing.test"

  resource.ParallelTest(t, resource.TestCase{
    PreCheck:                 func() { acctest.PreCheck(ctx, t) },
    ErrorCheck:               acctest.ErrorCheck(t, names.ExampleServiceID),
		ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
    CheckDestroy:             testAccCheckExampleChildThingDestroy(ctx),
    Steps: []resource.TestStep{
      {
        Config: testAccExampleThingConfigName(rName),
        Check: resource.ComposeTestCheckFunc(
          testAccCheckExampleThingExists(ctx, resourceName),
          acctest.CheckResourceDisappears(ctx, acctest.Provider, ResourceExampleParentThing(), parentResourceName),
        ),
        ExpectNonEmptyPlan: true,
      },
    },
  })
}
```

#### Per Attribute Acceptance Tests

These are typically named `TestAcc{SERVICE}{THING}_{ATTRIBUTE}`, e.g., `TestAccCloudWatchDashboard_Name`

For example:

```go
func TestAccExampleThing_Description(t *testing.T) {
  ctx := acctest.Context(t)
  rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)
  resourceName := "aws_example_thing.test"

  resource.ParallelTest(t, resource.TestCase{
    PreCheck:                 func() { acctest.PreCheck(ctx, t) },
    ErrorCheck:               acctest.ErrorCheck(t, names.ExampleServiceID),
		ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
    CheckDestroy:             testAccCheckExampleThingDestroy(ctx),
    Steps: []resource.TestStep{
      {
        Config: testAccExampleThingConfigDescription(rName, "description1"),
        Check: resource.ComposeTestCheckFunc(
          testAccCheckExampleThingExists(ctx, resourceName),
          resource.TestCheckResourceAttr(resourceName, "description", "description1"),
        ),
      },
      {
        ResourceName:      resourceName,
        ImportState:       true,
        ImportStateVerify: true,
      },
      {
        Config: testAccExampleThingConfigDescription(rName, "description2"),
        Check: resource.ComposeTestCheckFunc(
          testAccCheckExampleThingExists(ctx, resourceName),
          resource.TestCheckResourceAttr(resourceName, "description", "description2"),
        ),
      },
    },
  })
}

// below all TestAcc functions

func testAccExampleThingConfigDescription(rName string, description string) string {
  return fmt.Sprintf(`
resource "aws_example_thing" "test" {
  description = %[2]q
  name        = %[1]q
}
`, rName, description)
}
```

#### Cross-Account Acceptance Tests

When testing requires AWS infrastructure in a second AWS account, the below changes to the normal setup will allow the management or reference of resources and data sources across accounts:

- In the `PreCheck` function, include `acctest.PreCheckOrganizationsAccount(ctx, t)` to ensure a standardized set of information is required for cross-account testing credentials
- Switch usage of `ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories` to `ProtoV5ProviderFactories: acctest.ProtoV5FactoriesAlternate(ctx, t)`
- Add `acctest.ConfigAlternateAccountProvider()` to the test configuration and use `provider = awsalternate` for cross-account resources. The resource that is the focus of the acceptance test should _not_ use the alternate provider identification to simplify the testing setup.
- For any `TestStep` that includes `ImportState: true`, add the `Config` that matches the previous `TestStep` `Config`

An example acceptance test implementation can be seen below:

```go
func TestAccExample_basic(t *testing.T) {
  ctx := acctest.Context(t)
  resourceName := "aws_example.test"

  resource.ParallelTest(t, resource.TestCase{
    PreCheck: func() {
      acctest.PreCheck(ctx, t)
      acctest.PreCheckOrganizationsAccount(ctx, t)
    },
    ErrorCheck:               acctest.ErrorCheck(t, names.ExampleServiceID),
    ProtoV5ProviderFactories: acctest.ProtoV5FactoriesAlternate(ctx, t),
    CheckDestroy:             testAccCheckExampleDestroy(ctx),
    Steps: []resource.TestStep{
      {
        Config: testAccExampleConfig(),
        Check: resource.ComposeTestCheckFunc(
          testAccCheckExampleExists(ctx, resourceName),
          // ... additional checks ...
        ),
      },
      {
        Config:            testAccExampleConfig(),
        ResourceName:      resourceName,
        ImportState:       true,
        ImportStateVerify: true,
      },
    },
  })
}

func testAccExampleConfig() string {
  return acctest.ConfigCompose(
    acctest.ConfigAlternateAccountProvider(), fmt.Sprintf(`
# Cross account resources should be handled by the cross account provider.
# The standardized provider block to use is awsalternate as seen below.
resource "aws_cross_account_example" "test" {
  provider = awsalternate

  # ... configuration ...
}

# The resource that is the focus of the testing should be handled by the default provider,
# which is automatically done by not specifying the provider configuration in the resource.
resource "aws_example" "test" {
  # ... configuration ...
}
`, ...))
}
```

Searching for the usage of `acctest.PreCheckOrganizationsAccount` in the codebase will yield real-world examples of this setup in action.

#### Cross-Region Acceptance Tests

When testing requires AWS infrastructure in a second or third AWS region, the below changes to the normal setup will allow the management or reference of resources and data sources across regions:

- In the `PreCheck` function, include `acctest.PreCheckMultipleRegion(t, ###)` to ensure a standardized set of information is required for cross-region testing configuration. If the infrastructure in the second AWS region is also in a second AWS account also include `acctest.PreCheckOrganizationsAccount(ctx, t)`
- Switch usage of `ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories` to `ProtoV5ProviderFactories: acctest.ProtoV5FactoriesMultipleRegions(ctx, t, 2)` (where the last parameter is number of regions, 2 or 3)
- Add `acctest.ConfigMultipleRegionProvider(###)` to the test configuration and use `provider = awsalternate` (and potentially `provider = awsthird`) for cross-region resources. The resource that is the focus of the acceptance test should _not_ use the alternative providers to simplify the testing setup. If the infrastructure in the second AWS region is also in a second AWS account use `testAccAlternateAccountAlternateRegionProviderConfig()` (EC2) instead
- For any `TestStep` that includes `ImportState: true`, add the `Config` that matches the previous `TestStep` `Config`

An example acceptance test implementation can be seen below:

```go
func TestAccExample_basic(t *testing.T) {
  ctx := acctest.Context(t)
  var providers []*schema.Provider
  resourceName := "aws_example.test"

  resource.ParallelTest(t, resource.TestCase{
    PreCheck: func() {
      acctest.PreCheck(ctx, t)
      acctest.PreCheckMultipleRegion(t, 2)
    },
    ErrorCheck:               acctest.ErrorCheck(t, names.ExampleServiceID),
    ProtoV5ProviderFactories: acctest.ProtoV5FactoriesMultipleRegions(ctx, t, 2),
    CheckDestroy:             testAccCheckExampleDestroy(ctx),
    Steps: []resource.TestStep{
      {
        Config: testAccExampleConfig(),
        Check: resource.ComposeTestCheckFunc(
          testAccCheckExampleExists(ctx, resourceName),
          // ... additional checks ...
        ),
      },
      {
        Config:            testAccExampleConfig(),
        ResourceName:      resourceName,
        ImportState:       true,
        ImportStateVerify: true,
      },
    },
  })
}

func testAccExampleConfig() string {
  return acctest.ConfigCompose(
    acctest.ConfigMultipleRegionProvider(2), fmt.Sprintf(`
# Cross region resources should be handled by the cross region provider.
# The standardized provider is awsalternate as seen below.
resource "aws_cross_region_example" "test" {
  provider = awsalternate

  # ... configuration ...
}

# The resource that is the focus of the testing should be handled by the default provider,
# which is automatically done by not specifying the provider configuration in the resource.
resource "aws_example" "test" {
  # ... configuration ...
}
`, ...))
}
```

Searching for the usage of `acctest.PreCheckMultipleRegion` in the codebase will yield real-world examples of this setup in action.

#### Acceptance Test Concurrency

Certain AWS service APIs allow a limited number of a certain component, while the acceptance testing runs at a default concurrency of twenty tests at a time. For example as of this writing, the SageMaker service only allows one SageMaker Domain per AWS Region. Running the tests with the default concurrency will fail with API errors relating to the component quota being exceeded.

When encountering these types of components, acceptance testing can be set up to limit the available concurrency of that particular component. When limited to one component at a time, this may also be referred to as serializing the acceptance tests.

To convert to serialized (one test at a time) acceptance testing:

- Convert all existing capital `T` test functions with the limited component to begin with a lowercase `t`, e.g., `TestAccSageMakerDomain_basic` becomes `testDomain_basic`. This will prevent the test framework from executing these tests directly as the prefix `Test` is required.
    - In each of these test functions, convert `resource.ParallelTest` to `resource.Test`
- Create a capital `T` `TestAcc{Service}{Thing}_serial` test function that then references all the lowercase `t` test functions. If multiple test files are referenced, this new test be created in a new shared file such as `internal/service/{SERVICE}/{SERVICE}_test.go`. The contents of this test can be set like the following:

```go
func TestAccExampleThing_serial(t *testing.T) {
	t.Parallel()

	testCases := map[string]map[string]func(t *testing.T){
		"Thing": {
			"basic":        testAccThing_basic,
			"disappears":   testAccThing_disappears,
			// ... potentially other resource tests ...
		},
		// ... potentially other top level resource test groups ...
	}

	acctest.RunSerialTests2Levels(t, testCases, 0)
}
```

!!! note
    Future iterations of these acceptance testing concurrency instructions will include the ability to handle more than one component at a time including service quota lookup, if supported by the service API.

### Data Source Acceptance Testing

Writing acceptance testing for data sources is similar to resources, with the biggest changes being:

- Adding `DataSource` to the test and configuration naming, such as `TestAccExampleThingDataSource_Filter`
- The basic test _may_ be named after the easiest lookup attribute instead, e.g., `TestAccExampleThingDataSource_Name`
- No disappears testing
- Almost all checks should be done with [`resource.TestCheckResourceAttrPair()`](https://pkg.go.dev/github.com/hashicorp/terraform-plugin-testing/helper/resource?tab=doc#TestCheckResourceAttrPair) to compare the data source attributes to the resource attributes
- The usage of an additional `dataSourceName` variable to store a data source reference, e.g., `data.aws_example_thing.test`

Data sources testing should still use the `CheckDestroy` function of the resource, just to continue verifying that there are no dangling AWS resources after a test is run.

Please note that we do not recommend re-using test configurations between resources and their associated data source as it is harder to discover testing regressions. Authors are encouraged to potentially implement similar "base" configurations though.

For example:

```go
func TestAccExampleThingDataSource_Name(t *testing.T) {
  ctx := acctest.Context(t)
  rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)
  dataSourceName := "data.aws_example_thing.test"
  resourceName := "aws_example_thing.test"

  resource.ParallelTest(t, resource.TestCase{
    PreCheck:                 func() { acctest.PreCheck(ctx, t) },
    ErrorCheck:               acctest.ErrorCheck(t, names.ExampleServiceID),
    ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
    CheckDestroy:             testAccCheckExampleThingDestroy(ctx),
    Steps: []resource.TestStep{
      {
        Config: testAccExampleThingDataSourceConfigName(rName),
        Check: resource.ComposeTestCheckFunc(
          testAccCheckExampleThingExists(ctx, resourceName),
          resource.TestCheckResourceAttrPair(resourceName, "arn", dataSourceName, "arn"),
          resource.TestCheckResourceAttrPair(resourceName, "description", dataSourceName, "description"),
          resource.TestCheckResourceAttrPair(resourceName, "name", dataSourceName, "name"),
        ),
      },
    },
  })
}

// below all TestAcc functions

func testAccExampleThingDataSourceConfigName(rName string) string {
  return fmt.Sprintf(`
resource "aws_example_thing" "test" {
  name = %[1]q
}

data "aws_example_thing" "test" {
  name = aws_example_thing.test.name
}
`, rName)
}
```

## Acceptance Test Sweepers

When running the acceptance tests, especially when developing or troubleshooting Terraform resources, it's possible for code bugs or other issues to prevent the proper destruction of AWS infrastructure. To prevent lingering resources from consuming quota or causing unexpected billing, the Terraform Plugin SDK supports the test sweeper framework to clear out an AWS region of all resources. This section is meant to augment the [SDKv2 documentation on test sweepers](https://www.terraform.io/plugin/sdkv2/testing/acceptance-tests/sweepers) with Terraform AWS Provider specific details.

### Running Test Sweepers

!!! warning
    Test Sweepers will destroy AWS infrastructure and backups in the target AWS account and region! These are designed to override any API deletion protection. Never run these outside a development AWS account that should be completely empty of resources. <!-- markdownlint-disable-line code-block-style -->

To run the sweepers for all resources in `us-west-2` and `us-east-1` (default testing regions):

```console
make sweep
```

To run a specific resource sweeper:

```console
SWEEPARGS=-sweep-run=aws_example_thing make sweep
```

To run sweepers with an assumed role, use the following additional environment variables:

* `TF_AWS_ASSUME_ROLE_ARN` - Required.
* `TF_AWS_ASSUME_ROLE_DURATION` - Optional, defaults to 1 hour (3600).
* `TF_AWS_ASSUME_ROLE_EXTERNAL_ID` - Optional.
* `TF_AWS_ASSUME_ROLE_SESSION_NAME` - Optional.

### Sweeper Checklists

- __Add Resource Sweeper Implementation__: See [Writing Test Sweepers](#writing-test-sweepers).
- __Add Service To Sweeper List__: Once a `sweep.go` file is present in the service subdirectory, run `make gen` to regenerate the list of imports in `internal/sweep/sweep_test.go`.

### Writing Test Sweepers

Sweeper logic should be written to a file called `sweep.go` in the appropriate service subdirectory (`internal/service/{serviceName}`). This file should include the following build tags above the package declaration:

```go
package example
```

Next, register the resource into the test sweeper framework:

```go
func RegisterSweepers() {
  resource.AddTestSweepers("aws_example_thing", &resource.Sweeper{
    Name: "aws_example_thing",
    F:    sweepThings,
    // Optionally
    Dependencies: []string{
      "aws_other_thing",
    },
  })
}
```

Then add the actual implementation. Preferably, if a paginated SDK call is available:

```go
func sweepThings(region string) error {
  ctx := sweep.Context(region)
  client, err := sweep.SharedRegionalSweepClient(ctx, region)

  if err != nil {
    return fmt.Errorf("getting client: %w", err)
  }

  conn := client.ExampleConn(ctx)
  sweepResources := make([]sweep.Sweepable, 0)
  var errs *multierror.Error

  input := &example.ListThingsInput{}

  err = conn.ListThingsPages(input, func(page *example.ListThingsOutput, lastPage bool) bool {
    if page == nil {
      return !lastPage
    }

    for _, thing := range page.Things {
      r := ResourceThing()
      d := r.Data(nil)

      id := aws.StringValue(thing.Id)
      d.SetId(id)

      // Perform resource specific pre-sweep setup.
      // For example, you may need to perform one or more of these types of pre-sweep tasks, specific to the resource:
      //
      // err := sdk.ReadResource(ctx, r, d, client) // fill in data
      // d.Set("skip_final_snapshot", true)           // set an argument in order to delete

      // This "if" is only needed if the pre-sweep setup can produce errors.
      // Otherwise, do not include it.
      if err != nil {
        err := fmt.Errorf("reading Example Thing (%s): %w", id, err)
        errs = multierror.Append(errs, err)
        continue
      }

      sweepResources = append(sweepResources, sweep.NewSweepResource(r, d, client))
    }

    return !lastPage
  })

  if awsv1.SkipSweepError(err) {
    log.Printf("[WARN] Skipping Example Thing sweep for %s: %s", region, errs)
    return nil
  }
  if err != nil {
    errs = multierror.Append(errs, fmt.Errorf("listing Example Things for %s: %w", region, err))
  }

  if err := sweep.SweepOrchestrator(sweepResources); err != nil {
    errs = multierror.Append(errs, fmt.Errorf("sweeping Example Things for %s: %w", region, err))
  }

  return errs.ErrorOrNil()
}
```

If no paginated SDK call is available,
consider generating one using the [`listpages` generator](https://github.com/hashicorp/terraform-provider-aws/blob/main/internal/generate/listpages/README.md),
or implement the sweeper as follows:

```go
func sweepThings(region string) error {
  ctx := sweep.Context(region)
  client, err := sweep.SharedRegionalSweepClient(ctx, region)

  if err != nil {
    return fmt.Errorf("getting client: %w", err)
  }

  conn := client.ExampleConn(ctx)
  sweepResources := make([]sweep.Sweepable, 0)
  var errs *multierror.Error

  input := &example.ListThingsInput{}

  for {
    output, err := conn.ListThings(input)
    if awsv1.SkipSweepError(err) {
      log.Printf("[WARN] Skipping Example Thing sweep for %s: %s", region, errs)
      return nil
    }
    if err != nil {
      errs = multierror.Append(errs, fmt.Errorf("listing Example Things for %s: %w", region, err))
      return errs.ErrorOrNil()
    }

    for _, thing := range output.Things {
      r := ResourceThing()
      d := r.Data(nil)

      id := aws.StringValue(thing.Id)
      d.SetId(id)

      // Perform resource specific pre-sweep setup.
      // For example, you may need to perform one or more of these types of pre-sweep tasks, specific to the resource:
      //
      // err := sdk.ReadResource(ctx, r, d, client) // fill in data
      // d.Set("skip_final_snapshot", true)           // set an argument in order to delete

      // This "if" is only needed if the pre-sweep setup can produce errors.
      // Otherwise, do not include it.
      if err != nil {
        err := fmt.Errorf("reading Example Thing (%s): %w", id, err)
        errs = multierror.Append(errs, err)
        continue
      }

      sweepResources = append(sweepResources, sweep.NewSweepResource(r, d, client))
    }

    if aws.StringValue(output.NextToken) == "" {
      break
    }

    input.NextToken = output.NextToken
  }

  if err := sweep.SweepOrchestrator(sweepResources); err != nil {
    errs = multierror.Append(errs, fmt.Errorf("sweeping Example Thing for %s: %w", region, err))
  }

  return errs.ErrorOrNil()
}
```

## Acceptance Test Checklists

There are several aspects to writing good acceptance tests. These checklists will help ensure effective testing from the design stage through to implementation details.

### Basic Acceptance Test Design

These are basic principles to help guide the creation of acceptance tests.

- __Covers Changes__: Every line of resource or data source code added or changed should be covered by one or more tests. For example, if a resource has two ways of functioning, tests should cover both possible paths. Nearly every codebase change needs test coverage to ensure functionality and prevent future regressions. If a bug or other problem prompted a fix, a test should be added that previously would have failed, especially if the report included a configuration.
- __Follows the Single Responsibility Principle__: Every test should have a single responsibility and effectively test that responsibility. This may include individual tests for verifying basic functionality of the resource (Create, Read, Delete), separately verifying using and updating a single attribute in a resource, or separately changing between two attributes to verify two "modes"/"types" possible with a resource configuration. In following this principle, test configurations should be as simple as possible. For example, not including extra configuration unless it is necessary for the specific test.

### Test Implementation

Below are the required items that will be noted during the submission review and prevent immediate merging:

- __Implements CheckDestroy__: Resource testing should include a `CheckDestroy` function (typically named `testAccCheck{SERVICE}{RESOURCE}Destroy`) that calls the API to verify that the Terraform resource has been deleted or disassociated as appropriate. More information about `CheckDestroy` functions can be found in the [SDKv2 TestCase documentation](https://www.terraform.io/plugin/sdkv2/testing/acceptance-tests/testcase#checkdestroy).
- __Implements Exists Check Function__: Resource testing should include a `TestCheckFunc` function (typically named `testAccCheck{SERVICE}{RESOURCE}Exists`) that calls the API to verify that the Terraform resource has been created or associated as appropriate. Preferably, this function will also accept a pointer to an API object representing the Terraform resource from the API response that can be set for potential usage in later `TestCheckFunc`. More information about these functions can be found in the [SDKv2 Custom Check Functions documentation](https://www.terraform.io/plugin/sdkv2/testing/acceptance-tests/teststep#custom-check-functions).
- __Excludes Provider Declarations__: Test configurations should not include `provider "aws" {...}` declarations. If necessary, only the provider declarations in `acctest.go` should be used for multiple account/region or otherwise specialized testing.
- __Passes in us-west-2 Region__: Tests default to running in `us-west-2` and at a minimum should pass in that region or include necessary `PreCheck` functions to skip the test when run outside an expected environment.
- __Includes ErrorCheck__: All acceptance tests should include a call to the common ErrorCheck (`ErrorCheck:   acctest.ErrorCheck(t, names.ExampleServiceID),`).
- __Uses resource.ParallelTest__: Tests should use [`resource.ParallelTest()`](https://godoc.org/github.com/hashicorp/terraform/helper/resource#ParallelTest) instead of [`resource.Test()`](https://godoc.org/github.com/hashicorp/terraform/helper/resource#Test) except where serialized testing is absolutely required.
- [ ] __Uses fmt.Sprintf()__: Test configurations preferably should be separated into their own functions (typically named `testAcc{SERVICE}{RESOURCE}Config{PURPOSE}`) that call [`fmt.Sprintf()`](https://golang.org/pkg/fmt/#Sprintf) for variable injection or a string `const` for completely static configurations. Test configurations should avoid `var` or other variable injection functionality such as [`text/template`](https://golang.org/pkg/text/template/).
- __Uses Randomized Infrastructure Naming__: Test configurations that use resources where a unique name is required should generate a random name. Typically this is created via `rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)` in the acceptance test function before generating the configuration.
- __Prevents S3 Bucket Deletion Errors__: Test configurations that use `aws_s3_bucket` resources as a logging destination should include the `force_destroy = true` configuration. This is to prevent race conditions where logging objects may be written during the testing duration which will cause `BucketNotEmpty` errors during deletion.

For resources that support import, the additional item below is required that will be noted during the submission review and prevent immediate merging:

- __Implements ImportState Testing__: Tests should include an additional `TestStep` configuration that verifies resource import via `ImportState: true` and `ImportStateVerify: true`. This `TestStep` should be added to all possible tests for the resource to ensure that all infrastructure configurations are properly imported into Terraform.

The below are style-based items that _may_ be noted during review and are recommended for simplicity, consistency, and quality assurance:

- __Uses Builtin Check Functions__: Tests should use already available check functions, e.g. `resource.TestCheckResourceAttr()`, to verify values in the Terraform state over creating custom `TestCheckFunc`. More information about these functions can be found in the [SDKv2 Builtin Check Functions documentation](https://www.terraform.io/plugin/sdkv2/testing/acceptance-tests/teststep#builtin-check-functions).
- __Uses TestCheckResourceAttrPair() for Data Sources__: Tests should use [`resource.TestCheckResourceAttrPair()`](https://godoc.org/github.com/hashicorp/terraform/helper/resource#TestCheckResourceAttrPair) to verify values in the Terraform state for data sources attributes to compare them with their expected resource attributes.
- __Excludes Timeouts Configurations__: Test configurations should not include `timeouts {...}` configuration blocks except for explicit testing of customizable timeouts (typically very short timeouts with `ExpectError`).
- __Implements Default and Zero Value Validation__: The basic test for a resource (typically named `TestAcc{SERVICE}{RESOURCE}_basic`) should use available check functions, e.g. `resource.TestCheckResourceAttr()`, to verify default and zero values in the Terraform state for all attributes. Empty/missing configuration blocks can be verified with `resource.TestCheckResourceAttr(resourceName, "{ATTRIBUTE}.#", "0")` and empty maps with `resource.TestCheckResourceAttr(resourceName, "{ATTRIBUTE}.%", "0")`

### Avoid Hard Coding

Avoid hard coding values in acceptance test checks and configurations for consistency and testing flexibility. Resource testing is expected to pass across multiple AWS environments supported by the Terraform AWS Provider (e.g., AWS Standard and AWS GovCloud (US)). Contributors are not expected or required to perform testing outside of AWS Standard, e.g., running only in the `us-west-2` region is perfectly acceptable. However, contributors are expected to avoid hard coding with these guidelines.

#### Hardcoded Account IDs

- __Uses Account Data Sources__: Any hardcoded account numbers in configuration, e.g., `137112412989`, should be replaced with a data source. Depending on the situation, there are several data sources for account IDs including:
    - [`aws_caller_identity` data source](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/caller_identity),
    - [`aws_canonical_user_id` data source](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/canonical_user_id),
    - [`aws_billing_service_account` data source](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/billing_service_account), and
    - [`aws_sagemaker_prebuilt_ecr_image` data source](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/sagemaker_prebuilt_ecr_image).
- __Uses Account Test Checks__: Any check required to verify an AWS Account ID of the current testing account or another account should use one of the following available helper functions over the usage of `resource.TestCheckResourceAttrSet()` and `resource.TestMatchResourceAttr()`:
    - `acctest.CheckResourceAttrAccountID()`: Validates the state value equals the AWS Account ID of the current account running the test. This is the most common implementation.
    - `acctest.MatchResourceAttrAccountID()`: Validates the state value matches any AWS Account ID (e.g. a 12 digit number). This is typically only used in data source testing of AWS managed components.

Here's an example of using `aws_caller_identity`:

```terraform
data "aws_caller_identity" "current" {}

resource "aws_backup_selection" "test" {
  plan_id      = aws_backup_plan.test.id
  name         = "tf_acc_test_backup_selection_%[1]d"
  iam_role_arn = "arn:${data.aws_partition.current.partition}:iam::${data.aws_caller_identity.current.account_id}:role/service-role/AWSBackupDefaultServiceRole"
}
```

#### Hardcoded AMI IDs

- __Uses aws_ami Data Source__: Any hardcoded AMI ID configuration, e.g. `ami-12345678`, should be replaced with the [`aws_ami` data source](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/ami) pointing to an Amazon Linux image. The package `internal/acctest` includes test configuration helper functions to simplify these lookups:
    - `acctest.ConfigLatestAmazonLinuxHVMEBSAMI()`: The recommended AMI for most situations, using Amazon Linux, HVM virtualization, and EBS storage. To reference the AMI ID in the test configuration: `data.aws_ami.amzn-ami-minimal-hvm-ebs.id`.
    - `testAccLatestAmazonLinuxHVMInstanceStoreAMIConfig()` (EC2): AMI lookup using Amazon Linux, HVM virtualization, and Instance Store storage. Should only be used in testing that requires Instance Store storage rather than EBS. To reference the AMI ID in the test configuration: `data.aws_ami.amzn-ami-minimal-hvm-instance-store.id`.
    - `testAccLatestAmazonLinuxPVEBSAMIConfig()` (EC2): AMI lookup using Amazon Linux, Paravirtual virtualization, and EBS storage. Should only be used in testing that requires Paravirtual over Hardware Virtual Machine (HVM) virtualization. To reference the AMI ID in the test configuration: `data.aws_ami.amzn-ami-minimal-pv-ebs.id`.
    - `configLatestAmazonLinuxPvInstanceStoreAmi` (EC2): AMI lookup using Amazon Linux, Paravirtual virtualization, and Instance Store storage. Should only be used in testing that requires Paravirtual virtualization over HVM and Instance Store storage over EBS. To reference the AMI ID in the test configuration: `data.aws_ami.amzn-ami-minimal-pv-instance-store.id`.
    - `testAccLatestWindowsServer2016CoreAMIConfig()` (EC2): AMI lookup using Windows Server 2016 Core, HVM virtualization, and EBS storage. Should only be used in testing that requires Windows. To reference the AMI ID in the test configuration: `data.aws_ami.win2016core-ami.id`.

Here's an example of using `acctest.ConfigLatestAmazonLinuxHVMEBSAMI()` and `data.aws_ami.amzn-ami-minimal-hvm-ebs.id`:

```go
func testAccLaunchConfigurationDataSourceConfig_basic(rName string) string {
	return acctest.ConfigCompose(
		acctest.ConfigLatestAmazonLinuxHVMEBSAMI(),
		fmt.Sprintf(`
resource "aws_launch_configuration" "test" {
  name          = %[1]q
  image_id      = data.aws_ami.amzn-ami-minimal-hvm-ebs.id
  instance_type = "m1.small"
}
`, rName))
}
```

#### Hardcoded Availability Zones

- __Uses aws_availability_zones Data Source__: Any hardcoded AWS Availability Zone configuration, e.g. `us-west-2a`, should be replaced with the [`aws_availability_zones` data source](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/availability_zones). Use the convenience function called `acctest.ConfigAvailableAZsNoOptIn()` (defined in `internal/acctest/acctest.go`) to declare `data "aws_availability_zones" "available" {...}`. You can then reference the data source via `data.aws_availability_zones.available.names[0]` or `data.aws_availability_zones.available.names[count.index]` in resources using `count`.

Here's an example of using `acctest.ConfigAvailableAZsNoOptIn()` and `data.aws_availability_zones.available.names[0]`:

```go
func testAccInstanceVpcConfigBasic(rName string) string {
	return acctest.ConfigCompose(
		acctest.ConfigAvailableAZsNoOptIn(),
		fmt.Sprintf(`
resource "aws_subnet" "test" {
  availability_zone = data.aws_availability_zones.available.names[0]
  cidr_block        = "10.0.0.0/24"
  vpc_id            = aws_vpc.test.id
}
`, rName))
}
```

#### Hardcoded Database Versions

- __Uses Database Version Data Sources__: Hardcoded database versions, e.g., RDS MySQL Engine Version `5.7.42`, should be removed (which means the AWS-defined default version will be used) or replaced with a list of preferred versions using a data source. Because versions change over time and version offerings vary from region to region and partition to partition, using the default version or providing a list of preferences ensures a version will be available. Depending on the situation, there are several data sources for versions, including:
    - [`aws_rds_engine_version` data source](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/rds_engine_version),
    - [`aws_docdb_engine_version` data source](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/docdb_engine_version), and
    - [`aws_neptune_engine_version` data source](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/neptune_engine_version).

Here's an example of using `aws_rds_engine_version` and `data.aws_rds_engine_version.default.version`:

```terraform
data "aws_rds_engine_version" "default" {
  engine = "mysql"
}

data "aws_rds_orderable_db_instance" "test" {
  engine                     = data.aws_rds_engine_version.default.engine
  engine_version             = data.aws_rds_engine_version.default.version
  preferred_instance_classes = ["db.t3.small", "db.t2.small", "db.t2.medium"]
}

resource "aws_db_instance" "bar" {
  engine               = data.aws_rds_engine_version.default.engine
  engine_version       = data.aws_rds_engine_version.default.version
  instance_class       = data.aws_rds_orderable_db_instance.test.instance_class
  skip_final_snapshot  = true
  parameter_group_name = "default.${data.aws_rds_engine_version.default.parameter_group_family}"
}
```

#### Hardcoded Direct Connect Locations

- __Uses aws_dx_locations Data Source__: Hardcoded AWS Direct Connect locations, e.g., `EqSe2`, should be replaced with the [`aws_dx_locations` data source](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/dx_locations).

Here's an example using `data.aws_dx_locations.test.location_codes`:

```terraform
data "aws_dx_locations" "test" {}

resource "aws_dx_lag" "test" {
  name                  = "Test LAG"
  connections_bandwidth = "1Gbps"
  location              = tolist(data.aws_dx_locations.test.location_codes)[0]
  force_destroy         = true
}
```

#### Hardcoded Instance Types

- __Uses Instance Type Data Source__: Singular hardcoded instance types and classes, e.g., `t2.micro` and `db.t2.micro`, should be replaced with a list of preferences using a data source. Because offerings vary from region to region and partition to partition, providing a list of preferences dramatically improves the likelihood that one of the options will be available. Depending on the situation, there are several data sources for instance types and classes, including:
    - [`aws_ec2_instance_type_offering` data source](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/ec2_instance_type_offering) - Convenience functions declare configurations that are referenced with `data.aws_ec2_instance_type_offering.available` including:
        - The `acctest.AvailableEC2InstanceTypeForAvailabilityZone()` function for test configurations using an EC2 Subnet which is inherently within a single Availability Zone
        - The `acctest.AvailableEC2InstanceTypeForRegion()` function for test configurations that do not include specific Availability Zones
    - [`aws_rds_orderable_db_instance` data source](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/rds_orderable_db_instance),
    - [`aws_neptune_orderable_db_instance` data source](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/neptune_orderable_db_instance), and
    - [`aws_docdb_orderable_db_instance` data source](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/docdb_orderable_db_instance).

Here's an example of using `acctest.AvailableEC2InstanceTypeForRegion()` and `data.aws_ec2_instance_type_offering.available.instance_type`:

```go
func testAccSpotInstanceRequestConfig(rInt int) string {
	return acctest.ConfigCompose(
		acctest.AvailableEC2InstanceTypeForRegion("t3.micro", "t2.micro"),
		fmt.Sprintf(`
resource "aws_spot_instance_request" "test" {
  instance_type        = data.aws_ec2_instance_type_offering.available.instance_type
  spot_price           = "0.05"
  wait_for_fulfillment = true
}
`, rInt))
}
```

Here's an example of using `aws_rds_orderable_db_instance` and `data.aws_rds_orderable_db_instance.test.instance_class`:

```terraform
data "aws_rds_orderable_db_instance" "test" {
  engine                     = "mysql"
  engine_version             = "5.7.31"
  preferred_instance_classes = ["db.t3.micro", "db.t2.micro", "db.t3.small"]
}

resource "aws_db_instance" "test" {
  engine              = data.aws_rds_orderable_db_instance.test.engine
  engine_version      = data.aws_rds_orderable_db_instance.test.engine_version
  instance_class      = data.aws_rds_orderable_db_instance.test.instance_class
  skip_final_snapshot = true
  username            = "test"
}
```

#### Hardcoded Partition DNS Suffix

- __Uses aws_partition Data Source__: Any hardcoded DNS suffix configuration, e.g., the `amazonaws.com` in a `ec2.amazonaws.com` service principal, should be replaced with the [`aws_partition` data source](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/partition). A common pattern is declaring `data "aws_partition" "current" {}` and referencing it via `data.aws_partition.current.dns_suffix`.

Here's an example of using `aws_partition` and `data.aws_partition.current.dns_suffix`:

```terraform
data "aws_partition" "current" {}

resource "aws_iam_role" "test" {
  assume_role_policy = <<POLICY
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "",
      "Effect": "Allow",
      "Principal": {
        "Service": "cloudtrail.${data.aws_partition.current.dns_suffix}"
      },
      "Action": "sts:AssumeRole"
    }
  ]
}
POLICY
}
```

#### Hardcoded Partition in ARN

- __Uses aws_partition Data Source__: Any hardcoded AWS Partition configuration, e.g. the `aws` in a `arn:aws:SERVICE:REGION:ACCOUNT:RESOURCE` ARN, should be replaced with the [`aws_partition` data source](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/partition). A common pattern is declaring `data "aws_partition" "current" {}` and referencing it via `data.aws_partition.current.partition`.
- __Uses Builtin ARN Check Functions__: Tests should use available ARN check functions to validate ARN attribute values in the Terraform state over `resource.TestCheckResourceAttrSet()` and `resource.TestMatchResourceAttr()`:

    - `acctest.CheckResourceAttrRegionalARN()` verifies that an ARN matches the account ID and region of the test execution with an exact resource value
    - `acctest.MatchResourceAttrRegionalARN()` verifies that an ARN matches the account ID and region of the test execution with a regular expression of the resource value
    - `acctest.CheckResourceAttrGlobalARN()` verifies that an ARN matches the account ID of the test execution with an exact resource value
    - `acctest.MatchResourceAttrGlobalARN()` verifies that an ARN matches the account ID of the test execution with a regular expression of the resource value
    - `acctest.CheckResourceAttrRegionalARNNoAccount()` verifies that an ARN has no account ID and matches the current region of the test execution with an exact resource value
    - `acctest.CheckResourceAttrGlobalARNNoAccount()` verifies that an ARN has no account ID and matches an exact resource value
    - `acctest.CheckResourceAttrRegionalARNAccountID()` verifies that an ARN matches a specific account ID and the current region of the test execution with an exact resource value
    - `acctest.CheckResourceAttrGlobalARNAccountID()` verifies that an ARN matches a specific account ID with an exact resource value

Here's an example of using `aws_partition` and `data.aws_partition.current.partition`:

```terraform
data "aws_partition" "current" {}

resource "aws_iam_role_policy_attachment" "test" {
  policy_arn = "arn:${data.aws_partition.current.partition}:iam::aws:policy/service-role/AmazonRDSEnhancedMonitoringRole"
  role       = aws_iam_role.test.name
}
```

#### Hardcoded Region

- __Uses aws_region Data Source__: Any hardcoded AWS Region configuration, e.g., `us-west-2`, should be replaced with the [`aws_region` data source](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/region). A common pattern is declaring `data "aws_region" "current" {}` and referencing it via `data.aws_region.current.name`

Here's an example of using `aws_region` and `data.aws_region.current.name`:

```terraform
data "aws_region" "current" {}

resource "aws_route53_zone" "test" {
  vpc {
    vpc_id     = aws_vpc.test.id
    vpc_region = data.aws_region.current.name
  }
}
```

#### Hardcoded Spot Price

- __Uses aws_ec2_spot_price Data Source__: Any hardcoded spot prices, e.g., `0.05`, should be replaced with the [`aws_ec2_spot_price` data source](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/ec2_spot_price). A common pattern is declaring `data "aws_ec2_spot_price" "current" {}` and referencing it via `data.aws_ec2_spot_price.current.spot_price`.

Here's an example of using `aws_ec2_spot_price` and `data.aws_ec2_spot_price.current.spot_price`:

```terraform
data "aws_ec2_spot_price" "current" {
  instance_type = "t3.medium"

  filter {
    name   = "product-description"
    values = ["Linux/UNIX"]
  }
}

resource "aws_spot_fleet_request" "test" {
  spot_price      = data.aws_ec2_spot_price.current.spot_price
  target_capacity = 2
}
```

#### Hardcoded SSH Keys

- __Uses acctest.RandSSHKeyPair() or RandSSHKeyPairSize() Functions__: Any hardcoded SSH keys should be replaced with random SSH keys generated by either the acceptance testing framework's function [`RandSSHKeyPair()`](https://pkg.go.dev/github.com/hashicorp/terraform-plugin-sdk/helper/acctest#RandSSHKeyPair) or the provider function `RandSSHKeyPairSize()`. `RandSSHKeyPair()` generates 1024-bit keys.

Here's an example using `aws_key_pair`

```go
func TestAccKeyPair_basic(t *testing.T) {
  ...

	rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)
	publicKey, _, err := acctest.RandSSHKeyPair(acctest.DefaultEmailAddress)
	if err != nil {
		t.Fatalf("generating random SSH key: %s", err)
	}

  resource.ParallelTest(t, resource.TestCase{
		...
		Steps: []resource.TestStep{
			{
				Config: testAccKeyPairConfig(rName, publicKey),
        ...
      },
    },
  })
}

func testAccKeyPairConfig(rName, publicKey string) string {
	return fmt.Sprintf(`
resource "aws_key_pair" "test" {
  key_name   = %[1]q
  public_key = %[2]q
}
`, rName, publicKey)
}
```

#### Hardcoded Email Addresses

- __Uses either acctest.DefaultEmailAddress Constant or acctest.RandomEmailAddress() Function__: Any hardcoded email addresses should replaced with either the constant `acctest.DefaultEmailAddress` or the function `acctest.RandomEmailAddress()`.

Using `acctest.DefaultEmailAddress` is preferred when using a single email address in an acceptance test.

Here's an example using `acctest.DefaultEmailAddress`

```go
func TestAccSNSTopicSubscription_email(t *testing.T) {
	...

	rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)

	resource.ParallelTest(t, resource.TestCase{
		...
		Steps: []resource.TestStep{
			{
				Config: testAccTopicSubscriptionEmailConfig(rName, acctest.DefaultEmailAddress),
				Check: resource.ComposeTestCheckFunc(
					...
					resource.TestCheckResourceAttr(resourceName, "endpoint", acctest.DefaultEmailAddress),
				),
			},
		},
	})
}
```

Here's an example using `acctest.RandomEmailAddress()`

```go
func TestAccPinpointEmailChannel_basic(t *testing.T) {
	...

	domain := acctest.RandomDomainName()
	address1 := acctest.RandomEmailAddress(domain)
	address2 := acctest.RandomEmailAddress(domain)

	resource.ParallelTest(t, resource.TestCase{
		...
		Steps: []resource.TestStep{
			{
				Config: testAccEmailChannelConfig_FromAddress(domain, address1),
				Check: resource.ComposeTestCheckFunc(
					...
					resource.TestCheckResourceAttr(resourceName, "from_address", address1),
				),
			},
			{
				Config: testAccEmailChannelConfig_FromAddress(domain, address2),
				Check: resource.ComposeTestCheckFunc(
					...
					resource.TestCheckResourceAttr(resourceName, "from_address", address2),
				),
			},
		},
	})
}
```
# Provider Scaffolding (skaff)

`skaff` is a Terraform AWS Provider scaffolding command line tool.
It generates resource, data source, or function source files, along with test files which adhere to the latest best practices.
These files are heavily commented with instructions, serving as the best way to get started with provider development.

## Overview workflow steps

1. Figure out what you're trying to do:
    * Resource, data source, or function?
    * [Name it](naming.md).
    !!! tip
        Net-new resources should be implemented with Terraform Plugin Framework (i.e. the default `skaff` settings).
        See [Terraform Plugin Development Packages](terraform-plugin-development-packages.md) and [this issue](https://github.com/hashicorp/terraform-provider-aws/issues/32917) for additional information.
1. Use `skaff` to generate provider code.
1. Go through the generated code, customizing as necessary.
1. Run, test, refine.
1. Remove "TIP" comments.
1. Submit a pull request.

## Running `skaff`

1. Clone the [Terraform AWS Provider](https://github.com/hashicorp/terraform-provider-aws) repository.
1. Install `skaff`.

    ```sh
    make skaff
    ```

1. Change into the appropriate directory.
    - For resources and data sources, this is the service directory where the new entity will reside, e.g. `internal/service/mq`.
    - For functions, this is `internal/functions`.
1. Generate the resource, data source or function. For example,
    - `skaff resource --name BrokerReboot`.
    - `skaff datasource --name IAMRole`.
    - `skaff function --name ARNParse`.

To get help, enter `skaff` without arguments.

## Usage

### Help

```console
skaff --help
```

```
Usage:
  skaff [command]

Available Commands:
  completion  Generate the autocompletion script for the specified shell
  datasource  Create scaffolding for a data source
  function    Create scaffolding for a function
  help        Help about any command
  resource    Create scaffolding for a resource

Flags:
  -h, --help   help for skaff
```

### Autocompletion

Generate the autocompletion script for `skaff` for the specified shell

```console
skaff completion --help
```

```
Usage:
  skaff completion [command]

Available Commands:
  bash        Generate the autocompletion script for bash
  fish        Generate the autocompletion script for fish
  powershell  Generate the autocompletion script for powershell
  zsh         Generate the autocompletion script for zsh

Flags:
  -h, --help   help for completion

Use "skaff completion [command] --help" for more information about a command
```

### Data Source

Create scaffolding for a data source

```console
skaff datasource --help
```

```
Create scaffolding for a data source

Usage:
  skaff datasource [flags]

Flags:
  -c, --clear-comments     do not include instructional comments in source
  -f, --force              force creation, overwriting existing files
  -h, --help               help for datasource
  -t, --include-tags       Indicate that this resource has tags and the code for tagging should be generated
  -n, --name string        name of the entity
  -p, --plugin-sdkv2       generate for Terraform Plugin SDK V2
  -s, --snakename string   if skaff doesn't get it right, explicitly give name in snake case (e.g., db_vpc_instance)
```

### Function

Create scaffolding for a function.

```console
skaff function --help
```

```
Create scaffolding for a function

Usage:
  skaff function [flags]

Flags:
  -c, --clear-comments       do not include instructional comments in source
  -d, --description string   description of the function
  -f, --force                force creation, overwriting existing files
  -h, --help                 help for function
  -n, --name string          name of the function
  -s, --snakename string     if skaff doesn't get it right, explicitly give name in snake case (e.g., arn_build)
```

### Resource

Create scaffolding for a resource

```console
skaff resource --help
```

```
Create scaffolding for a resource

Usage:
  skaff resource [flags]

Flags:
  -c, --clear-comments     do not include instructional comments in source
  -f, --force              force creation, overwriting existing files
  -h, --help               help for resource
  -t, --include-tags       Indicate that this resource has tags and the code for tagging should be generated
  -n, --name string        name of the entity
  -p, --plugin-sdkv2       generate for Terraform Plugin SDK V2
  -s, --snakename string   if skaff doesn't get it right, explicitly give name in snake case (e.g., db_vpc_instance)
```
# Terraform Plugin Development Packages

The Terraform AWS Provider is constructed with HashiCorp-maintained packages for building plugins.
Most existing resources are implemented with [Terraform Plugin SDK V2](https://developer.hashicorp.com/terraform/plugin/sdkv2), while newer resources use [Terraform Plugin Framework](https://developer.hashicorp.com/terraform/plugin/framework).
A thorough comparison of the packages can be found [here](https://developer.hashicorp.com/terraform/plugin/framework-benefits).

## Which Plugin Version Should I Use?

At this time net-new contributions are **required to use Terraform Plugin Framework**.
Enhancements or bug fixes to existing Plugin SDKv2 based resources do not require migration.
The AWS Provider is [muxed](https://developer.hashicorp.com/terraform/plugin/framework/migrating/mux) to allow existing Terraform Plugin SDK V2 resources and data sources to remain alongside newer Plugin Framework based resources.

[`skaff`](skaff.md) will generate Plugin Framework based resources by default, though for exceptional cases the optional `-p`/`--plugin-sdkv2` flag can be used.
Where applicable, the contributor guide has been updated to include examples with both Terraform Plugin Framework and Terraform Plugin SDK V2.
# Terraform Plugin Migrations

With the introduction of [Terraform Plugin Framework](https://developer.hashicorp.com/terraform/plugin/framework) it will become necessary to migrate existing resources from SDKv2. The Provider currently implements both plugins so migration can be done at a resource level.

## Migration Tooling

Tooling has been created that will scaffold an existing resource into a Framework resource. This tool is meant to be used as a starting point so additional editing will be needed.

Build:

```console
make tfsdk2fw
```

Convert a resource:

The following pattern is used to generate a file:  `tfsdk2fw [-resource <resource-type>|-data-source <data-source-type>] <package-name> <name> <generated-file>`

Example:

```console
tfsdk2fw -resource aws_example_resource examplepackage ResourceName internal/service/examplepackage/resource_name_fw.go
```

This command creates a separate file that exists alongside the existing SDKv2 resource. Ultimately, the new file should replace the SDKv2 resource.

When done creating the resource using the Framework run `make gen` to remove the SDK resource and add the Framework resource to the list of generated service packages.

## State Upgrade

Terraform Plugin Framework introduced `null` values, which differ from `zero` values. Since the Plugin SDKv2 marked both `null` and `zero` values as the same, it will be necessary to use the [State Upgrader](https://developer.hashicorp.com/terraform/plugin/framework/migrating/resources/state-upgrade).

An example of a resource with an upgraded state, while migrating, can be found [here](https://github.com/hashicorp/terraform-provider-aws/blob/88447d09f85dc737597243b31c5d0c8e212d055b/internal/service/batch/job_queue.go#L330).

### Custom Types

The Plugin Framework introduced [custom types](https://developer.hashicorp.com/terraform/plugin/framework/handling-data/types/custom) that allow custom validation on basic types. The following attribute types will require a state upgrade to utilize these custom types.

- ARNs
- CIDR Blocks
- Duration
- Timestamps

SDKv2 `ARN` attribute.

```go
func ResourceExampleResource {
    return &schema.Schema{
        "arn_attribute": {		
	        Type:         schema.TypeString,
	        Optional:     true,
	        ValidateFunc: verify.ValidARN,
        },
        
        // other schema attributes
    }
}
```

Framework `ARN` attribute.

```go
func (r *resourceExampleResource) Schema(ctx context.Context, request resource.SchemaRequest, response *resource.SchemaResponse) {
    return schema.Schema{
        "arn_attribute": schema.StringAttribute{
            CustomType: fwtypes.ARNType,
            Optional:   true,
            PlanModifiers: []planmodifier.String{
                stringplanmodifier.UseStateForUnknown(),
            },
        },

        // other schema attributes
    }
}
```

## Tagging

Tagging in the Plugin Framework is done by implementing the `ModifyPlan()` method on a resource.

```go
func (r *resourceExampleResource) ModifyPlan(ctx context.Context, request resource.ModifyPlanRequest, response *resource.ModifyPlanResponse) {
	r.SetTagsAll(ctx, request, response)
}
```

Transparent Tagging that is used in SDKv2 also applies to the Framework by using the `@Tags` decorator when defining the resource.

```go
// @FrameworkResource("aws_service_example", name="Example Resource")
// @Tags(identifierAttribute="arn")
func newResourceExampleResrouce(_ context.Context) (resource.ResourceWithConfigure, error) {
	r := resourceExampleResource{}
	return &r, nil
}
```

## Testing

It is important to not cause any state diffs that result in breaking changes. Testing will check that the diff before and after the migration presents no changes.

!!! tip
    `VersionConstraint` should be set to the most recently published version of the AWS Provider.

```go
func TestAccExampleResource_MigrateFromPluginSDK(t *testing.T) {
	ctx := acctest.Context(t)
	var example service.ExampleResourceOutput
	resourceName := "aws_example_resource.test"
	rName := sdkacctest.RandomWithPrefix(acctest.ResourcePrefix)

	resource.ParallelTest(t, resource.TestCase{
		PreCheck:     func() { acctest.PreCheck(ctx, t); testAccPreCheck(ctx, t) },
		ErrorCheck:   acctest.ErrorCheck(t, names.ExampleServiceID),
		CheckDestroy: testAccCheckExampleResourceDestroy(ctx),
		Steps: []resource.TestStep{
			{
				ExternalProviders: map[string]resource.ExternalProvider{
					"aws": {
						Source:            "hashicorp/aws",
						VersionConstraint: "5.23.0", // always use most recently published version of the Provider
					},
				},
				Config: testAccExampleResourceConfig_basic(rName),
				Check: resource.ComposeTestCheckFunc(
					testAccCheckExampleResourceExists(ctx, resourceName, &example),
				),
			},
			{
				ProtoV5ProviderFactories: acctest.ProtoV5ProviderFactories,
				Config:                   testAccExampleResourceConfig_basic(rName),
				PlanOnly:                 true,
			},
		},
	})
}
```
# Unit Tests

Unlike acceptance tests, unit tests do not access AWS and are focused on a function (or method). Because of this, they are quick and cheap to run.

In designing a resource's implementation, isolate complex bits from AWS bits so that they can be tested through a unit test. We encourage more unit tests in the provider.

## In context

To help place unit testing in context, here is an overview of the Terraform AWS Provider's three types of tests.

1. [**Acceptance tests**](running-and-writing-acceptance-tests.md) are end-to-end evaluations of interactions with AWS. They validate functionalities like creating, reading, and destroying resources within AWS.
2. **Unit tests** (_You are here!_) focus on testing isolated units of code within the software, typically at the function level. They assess functionalities solely within the provider itself.
3. [**Continuous integration tests**](continuous-integration.md) encompass a suite of automated tests that are executed on every pull request and include linting, compiling code, running unit tests, and performing static analysis.

## What to test

Utilitarian functions that carry out processing within the provider, that don't need contact with AWS, are candidates for unit testing. In specific, any moderately to very complex utilitarian function should have a corresponding unit test.

Rather than being a burden, using unit tests often saves time (and money) during development because they can be run quickly and locally. In addition, rather than mentally processing all edge cases, you can use test cases to refine the function's behavior.

Cut and dry functions using well-used patterns, like typical flatteners and expanders (flex functions), don't need unit testing. However, if the flex functions are complex or intricate, they should be unit tested.

## Where they go

Unit tests can be placed in a test file with acceptance tests if they mainly relate to a single resource. However, if it makes sense to do so, functions and their unit tests can be moved to their files. Reasons you might split them from acceptance test files include length of the acceptance test files, or several resources using them.

Where unit tests are included with acceptance tests in resource test files, they should be placed at the top of the file, before the first acceptance test.

## Example

This is an example of a unit test.

Its name is prefixed with "Test" but not "TestAcc" like an acceptance test.

```go
func TestExampleUnitTest(t *testing.T) {
	t.Parallel()

	testCases := []struct {
		TestName string
		Input    string
		Expected string
		Error    bool
	}{
		{
			TestName: "empty",
			Input:    "",
			Expected: "",
			Error:    true,
		},
		{
			TestName: "descriptive name",
			Input:    "some input",
			Expected: "some output",
			Error:    false,
		},
		{
			TestName: "another descriptive name",
			Input:    "more input",
			Expected: "more output",
			Error:    false,
		},
	}

	for _, testCase := range testCases {
		t.Run(testCase.TestName, func(t *testing.T) {
			t.Parallel()
			got, err := tfrds.FunctionFromResource(testCase.Input)

			if err != nil && !testCase.Error {
				t.Errorf("got error (%s), expected no error", err)
			}

			if err == nil && testCase.Error {
				t.Errorf("got (%s) and no error, expected error", got)
			}

			if got != testCase.Expected {
				t.Errorf("got %s, expected %s", got, testCase.Expected)
			}
		})
	}
}
```
# Exclusive Relationship Management Resources

**Summary:** A proposal describing the use case for "exclusive relationship management" resources and their function within the Terraform AWS provider.  
**Created**: 2024-09-06  
**Author**: [@jar-b](https://github.com/jar-b)  

---

Within AWS there are several resource types which have direct relationships or dependencies on one another. These can be either "one-to-one", where a single entity is linked to another, or "one-to-many", where a single parent entity can be linked to multiple children. As the Terraform AWS provider has matured, the patterns for modeling these relationships have evolved, most notably in the "one-to-many" style relationships.

This RFC will cover a brief history of "one-to-many" resource relationships and their representation in the Terraform AWS provider, followed by a proposal for enabling exclusive management of these relationships via a standalone resource. For an in-depth review of all relationship resources in the Terraform AWS provider, refer to the [relationship resource design standards](./relationship-resource-design-standards.md) design decision.

## Background

During early development of the Terraform AWS provider, resources sometimes represented "one-to-many" relationships as arguments on the parent resource. For example, the [`inline_policy`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_role#inline_policy) argument on the [`aws_iam_role`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_role) resource allows inline policies to be created as part of the role resource lifecycle.

```terraform
resource "aws_iam_role" "example" {
  name               = "exampleRole"
  assume_role_policy = data.aws_iam_policy_document.instance_assume_role_policy.json

  inline_policy {
    name   = "exampleInlinePolicy"
    policy = data.aws_iam_policy_document.inline_policy.json
  }
}
```

While simplifying the syntax for practitioners, this approach introduces complexity within the provider implementation; a single resource now manages the lifecycle of several different remote resources. This can leave the resource in a partially provisioned state if creation of one of the child resources fails. One benefit to this design is that it enables the parent resource to retain "exclusive" control of the relationships. That is, if the parent resource includes a relationship with a child entity that is not explicitly configured, the provider can remove it.

Due to the complexity of the design described above, the Terraform AWS provider has moved toward representing "one-to-many" relationships via standalone resources. These resources are typically added alongside the argument-based method to preserve backward compatibility. Continuing with the example above, inline policies can now be managed distinctly from the assigned role via the [`aws_iam_role_policy`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_role_policy) resource.

```terraform
resource "aws_iam_role" "example" {
  name               = "exampleRole"
  assume_role_policy = data.aws_iam_policy_document.instance_assume_role_policy.json
}

resource "aws_iam_role_policy" "example" {
  name = "exampleInlinePolicy"
  role = aws_iam_role.test_role.id

  policy = data.aws_iam_policy_document.inline_policy.json
}
```

While this separates the lifecycle of distinct resource types to more closely align with the underlying AWS APIs, this approach alone does not provide a mechanism for exclusive management of all relationships to the parent. The absence of this benefit is often [cited by the community](https://github.com/hashicorp/terraform-provider-aws/issues/22336#issuecomment-1586581208) as a reason not to move away from the argument-based definitions to standalone resources. The lack of parity has also prevented maintainers from formally deprecating and removing arguments on the parent resource for configuring relationships.

### Existing Resources

There is some precedent in the Terraform AWS provider for a resource which handles only exclusive relationship management in [`aws_iam_policy_attachment`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_policy_attachment). However, the scope of responsibility in this resource (managing attachments to roles, users, and groups simultaneously), is broader than what this RFC proposes, and cannot be replicated widely due to the unique nature of customer managed IAM policies which can be associated with multiple distinct parent resource types.

## Proposal

To provide practitioners with a consistent and maintainable mechanism for exclusive management of "one-to-many" relationships, the Terraform AWS provider will introduce a new pattern for developing "exclusive relationship management" resources. Resources with this function will end in the suffix `_exclusive`, with the purpose of reconciling the relationships present in AWS against what is configured in Terraform, adding and removing relationships as necessary.

In general, exclusive relationship management resources should have the following characteristics:

1. A required argument (typically `TypeString`) storing the parent resource identifier.
1. A required argument (typically `TypeSet` with `TypeString` elements) storing identifiers of all child resources. An empty set should remove all relationships.
1. The ability to read the current state of relationships in AWS and add or remove them as necessary.
1. The ability to "inherit" exclusive ownership of existing relationship definitions without destructive action. Adding this resource to a configuration should __not__ result in a destroy/re-create relationship workflow.

As an example, the implementation for inline IAM policies would be named `aws_iam_role_policies_exclusive`, and used as follows:

```terraform
resource "aws_iam_role" "example" {
  name               = "exampleRole"
  assume_role_policy = data.aws_iam_policy_document.instance_assume_role_policy.json
}

resource "aws_iam_role_policy" "example" {
  name = "exampleInlinePolicy"
  role = aws_iam_role.example.id

  policy = data.aws_iam_policy_document.inline_policy.json
}

# This resource ensures that only `exampleInlinePolicy` is assigned
# to this role. Any other inline policies will be removed.
resource "aws_iam_role_policies_exclusive" "example" {
  role_name    = aws_iam_role.example.name
  policy_names = [aws_iam_role_policy.example.name]
}
```

A working implementation can be found on [this branch](https://github.com/hashicorp/terraform-provider-aws/tree/f-iam_role_policies_lock). The `_exclusive` resource will detect any additional inline policies assigned to the role during `plan` operations and remove them during `apply`. This behavior provides parity with the `inline_policy` argument on the `aws_iam_role` resource, allowing maintainers to formally deprecate this argument and suggest practitioners migrate to the standalone inline policy resource, optionally including an `_exclusive` resource when exclusive management of assignments is desired.

### Potential Resources

In addition to the IAM inline policy example used throughout this document, there are several other resources with "one-to-many" relationships that could benefit from exclusive management of relationships.

!!! note
    Due to the popularity of the resources in this section, argument deprecations are likely to be "soft" deprecations where removal will not happen for several major releases, or until tooling is available to limit the amount of manual changes required to migrate to the preferred pattern. Despite this long removal window, a soft deprecation is still helpful for maintainers to reference when making best practice recommendations to the community.

#### Inline IAM policies to role

Manage inline IAM policies assigned to a role. Related resources:

- [`aws_iam_role`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_role)
- [`aws_iam_role_policy`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_role_policy)

Deprecate `aws_iam_role.inline_policy`.

#### Inline IAM policies to user

Manage inline IAM policies assigned to a user. Related resources:

- [`aws_iam_user`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_user)
- [`aws_iam_user_policy`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_user_policy)

There are no arguments to deprecate on `aws_iam_user`. This may lower the relative priority.

#### Inline IAM policies to group

Manage inline IAM policies assigned to a group. Related resources:

- [`aws_iam_group`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_group)
- [`aws_iam_group_policy`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_group_policy)

There are no arguments to deprecate on `aws_iam_group`. This may lower the relative priority.

#### Customer managed IAM policies to role

Manage customer managed IAM policies attached to a role. Related resources:

- [`aws_iam_role`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_role)
- [`aws_iam_policy`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_policy)
- [`aws_iam_role_policy_attachment`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_role_policy_attachment)

Deprecate `aws_iam_role.managed_policy_arns` .

#### Customer managed IAM policies to user

Manage customer managed IAM policies attached to a user. Related resources:

- [`aws_iam_user`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_user)
- [`aws_iam_policy`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_policy)
- [`aws_iam_user_policy_attachment`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_user_policy_attachment)

There are no arguments to deprecate on `aws_iam_user`. This may lower the relative priority.

#### Customer managed IAM policies to group

Manage customer managed IAM policies attached to a group. Related resources:

- [`aws_iam_group`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_group)
- [`aws_iam_policy`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_policy)
- [`aws_iam_group_policy_attachment`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_group_policy_attachment)

There are no arguments to deprecate on `aws_iam_group`. This may lower the relative priority.

#### EC2 security groups to network interface

Manage EC2 security group attachments to network interfaces. Related resources:

- [`aws_instance`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/instance)
- [`aws_network_interface`](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/network_interface)
- [`aws_security_group`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/security_group)
- [`aws_ec2_network_interface_sg_attachment`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/network_interface_sg_attachment)

Deprecate `aws_instance.security_groups`, `aws_instance.vpc_security_group_ids`, and `aws_network_interface.security_groups`.

#### VPC security group rules to security group

Manage ingress and egress rules assigned to a VPC security group. Related resources:

- [`aws_security_group`](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/security_group)
- [`aws_security_group_rule`](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/security_group_rule)
- [`aws_vpc_security_group_egress_rule`](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/vpc_security_group_egress_rule)
- [`aws_vpc_security_group_ingress_rule`](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/vpc_security_group_ingress_rule)

Deprecate `aws_security_group.ingress` and `aws_security_group.egress`. Consider deprecating `aws_security_group_rule` entirely.

### Alternate Naming Conventions

Ideally all resources providing the "exclusive relationship management" function should utilize the same suffix. While there are several options to describe this behavior, `_exclusive` seemed the most concise. The options considered were:

| Suffix | Example |
| --- | --- |
| `_exclusive` _(selected)_ | `aws_iam_role_policies_exclusive` |
| `_management` | `aws_iam_role_policies_management` |
| `_lock` | `aws_iam_role_policies_lock` |
| `_exclusive_lock` | `aws_iam_role_policies_exclusive_lock` |
| `_exclusive_management` | `aws_iam_role_policies_exclusive_management` |

## Next Steps

If this design decision is approved, a meta-issue will be opened to track all resources listed in the [Potential Resources](#potential-resources) section, with linked issues for each individual implementation.
# RDS Blue/Green Deployments

**Summary:** Discussion of which resource types can support RDS Blue/Green Deployments for updates<br>
**Created:** 2023-11-24<br>
**Updated:** 2024-01-24

---

The Terraform Provider for AWS currently supports [RDS Blue/Green Deployments](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/blue-green-deployments-overview.html) for the resource type [`aws_db_instance`](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/db_instance).
Extending this support to other RDS resource types is a common request.

Due to Terraform's resource model and how RDS implements Blue/Green Deployments, support for Blue/Green Deployments cannot be extended to other resource types.

## Background

Terraform treats each resource as a persistent, self-contained object that can be created, modified, and deleted without interacting with other objects, other than having parameter value dependencies on other resources.
In most cases, this more or less corresponds to how objects within AWS interrelate.

RDS Blue/Green Deployments are implemented using a temporary Blue/Green Deployment orchestration object, which manages both the old and new RDS Instances, data synchronization, switchover, and deletion of the old Instances. The orchestration object is typically deleted after switchover, though it can be retained to, for example, review the operation logs for the deployment.

## Implementations

### `aws_db_instance`

Because the `aws_db_instance` resource type represents a single, self-contained object, we are able to fit within the Terraform resource model while using an RDS Blue/Green Deployment to reduce downtime for many Instance updates.
For instance, changing the backing EC2 instance type or the engine version in place can cause downtimes of over 15 minutes.
When the `blue_green_update.enabled` parameter is set, the AWS Provider will use a Blue/Green Deployment internally to perform the update, so that the downtime is only the length of the switchover.
According to [AWS documentation](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/blue-green-deployments-overview.html), "switchover typically takes under a minute".

The update takes place in a single `terraform apply`, and the Blue/Green Deployment object is not exposed by the provider, since it is only an implementation detail.

### `aws_db_instance` Replicas

Creating a replica RDS DB Instance involves one source `aws_db_instance` resource and one or more replica `aws_db_instance` resources.
Because multiple resources are involved, Terraform cannot treat the source Instance and its replicas as a single unit.
Therefore, Terraform cannot use a Blue/Green Deployment for updating an Instance and its replicas.

### `aws_rds_cluster`

The `aws_rds_cluster` resource type is used to model two types of RDS clusters, either an Aurora cluster or a multi-AZ cluster for a "traditional" database engine such as MySQL or PostgreSQL.

Blue/Green Deployments are not currently supported for multi-AZ clusters.
If, at some point, Blue/Green Deployments are supported, multi-AZ clusters may be a candidate for updates using Blue/Green Deployment for reduced downtime, since the multi-AZ cluster is treated as a single object by both the provider and the AWS API.
However, the multi-AZ cluster already performs a rolling update of the individual instances, so there may be no benefit to using a Blue/Green Deployment for updates.

Aurora clusters do support Blue/Green Deployments.
However, neither the AWS APIs nor the provider treats an Aurora cluster as a self-contained object:
A cluster consists of a containing `aws_rds_cluster` resource and one or more `aws_rds_cluster_instance` resources.
Because of this, a Blue/Green Deployment cannot be used for most updates on an Aurora cluster.

### Standalone Blue/Green Deployment Resource

The RDS Blue/Green Deployment object is a temporary orchestration object which reserves compute and other resources and manages connections.
When it is created, it first creates replicas of any existing RDS Instances, configures synchronization, and updates the engine version, DB parameter group, and instance class if needed.
Once these operations are complete, any additional updates are performed on the new (or "Green") instances.
After these updates are complete, the Green instances can be promoted to be the live instances.

Using a standalone Blue/Green Deployment resource would require multiple iterations of editing the Terraform configuration, applying the configuration, or importing resources.
This isn't a good fit for Terraform.

The following example shows the steps that would be needed to use a standalone Blue/Green Deployment resource with a single RDS Instance (`aws_db_instance`).
Using it with an Aurora cluster would be similar, but require changes to all of the resources making up the cluster.

We start with an RDS Instance with the name `example-db`.

```terraform
resource "aws_db_instance" "example" {
  identifier = "example-db"
}
```

1. Edit the Terraform configuration to add the `aws_rds_blue_green_deployment` resource

    ```terraform
    resource "aws_db_instance" "example" {
      identifier = "example-db"
    }

    resource "aws_rds_blue_green_deployment" "example" {
      source = aws_db_instance.example.arn
    }
    ```

1. Run `terraform apply`.
  This will wait until the Blue/Green Deployment and the "Green" RDS Instance  `example-db-green` are created
1. Edit the Terraform configuration to add an `aws_db_instance` resource for the RDS Instance `example-db-green` and make any desired configuration changes

    ```terraform
    resource "aws_db_instance" "example" {
      identifier = "example-db"
    }

    resource "aws_rds_blue_green_deployment" "example" {
      source = aws_db_instance.example.arn
    }

    resource "aws_db_instance" "example_updated" {
      identifier = "example-db-green"
    }
    ```

1. Run `terraform` to import the RDS Instance `example-db-green`
1. Run `terraform apply` to update the RDS Instance `example-db-green`
1. Edit the Terraform configuration to trigger the switchover on the `aws_rds_blue_green_deployment` resource

    ```terraform
    resource "aws_db_instance" "example" {
      identifier = "example-db"
    }

    resource "aws_rds_blue_green_deployment" "example" {
      source      = aws_db_instance.example.arn
      switch_over = true
    }

    resource "aws_db_instance" "example_updated" {
      identifier = "example-db-green"
    }
    ```

1. Run `terraform apply` to perform the switchover.
  The updated RDS Instance will be renamed from `example-db-green` to `example-db` and the original RDS Instance will be renamed from `example-db` to `example-db-old`.
  This means that the resource `aws_db_instance.example` will now be pointing to the updated RDS Instance, the resource `aws_db_instance.example_updated` will be pointing at a non-existent RDS Instance, and the original RDS Instance is not known to Terraform.
1. Edit the Terraform configuration to remove the resource `aws_db_instance.example_updated` and add an `aws_db_instance` resource for the RDS Instance `example-db-old`

    ```terraform
    resource "aws_db_instance" "example" {
      identifier = "example-db"
    }

    resource "aws_rds_blue_green_deployment" "example" {
      source      = aws_db_instance.example.arn
      switch_over = true
    }

    resource "aws_db_instance" "example_to_delete" {
      identifier = "example-db-old"
    }
    ```

1. Run `terraform` to import the RDS Instance `example-db-old`
1. Edit the Terraform configuration to remove the resource `aws_db_instance.example_updated` and the `aws_rds_blue_green_deployment` resource

    ```terraform
    resource "aws_db_instance" "example" {
      identifier = "example-db"
    }
    ```

1. Run `terraform apply` to delete the Blue/Green Deployment and the original RDS Instance
# Relationship Resource Design Standards

**Summary:** Align on design standards for relationship management resources in the Terraform AWS Provider.  
**Created**: 2022-07-11  

---

The goal of this document is to assess the design of existing "relationship" resources in the Terraform AWS Provider and determine if a consistent set of rules can be defined for implementing them. For the purpose of this document, a "relationship" resource is defined as a resource which manages either a direct relationship between two standalone resources ("one-to-one", ie. [`aws_ssoadmin_permission_boundary_attachment`](https://registry.terraform.io/providers/-/aws/latest/docs/resources/ssoadmin_permissions_boundary_attachment)), or a variable number of child relationships to a parent resource ("one-to-many", ie. [`aws_iam_role_policy_attachment`](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_role_policy_attachment)). Resources and AWS APIs with this function will often contain suffixes like "attachment", "assignment", "registration", or "rule".

A documented standard for implementing relationship-styled resources will inform how new resources are written, and provide guidelines to refer back to when the community requests features which may not align with internal best practices.

## Background

The first form of relationship resources ("one-to-one") typically have a straightforward, singular API design and provider implementation given only a single relationship exists. The second form of resources ("one-to-many") often has to balance two provider design principles:

* [Resources should represent a single API object](https://developer.hashicorp.com/terraform/plugin/best-practices/hashicorp-provider-design-principles#resources-should-represent-a-single-api-object)
* [Resource and attribute schema should closely match the underlying API](https://developer.hashicorp.com/terraform/plugin/best-practices/hashicorp-provider-design-principles#resource-and-attribute-schema-should-closely-match-the-underlying-api)

In these cases, the smallest possible piece of infrastructure may be a single parent-child relationship, while the AWS APIs may accept and return lists of parent-child relationships. The first principle would favor a resource representing a single relationship, while the second principle suggests a resource should manage a variable number of relationships. Additionally, practitioners coming from the AWS CLI or SDK might also have expectations about how resource schemas should be shaped compared to CLI flags or SDK inputs.

An analysis of existing resources can inform which of these principles maintainers have given precedence to up to this point. The table below documents existing relationship resources in the AWS provider. This table should not be considered exhaustive[^1], but covers a large majority of the resources implementing the patterns discussed above.

| **Resource Name** | **Form** | **AWS API** | **Terraform** |
| --- | --- | --- | --- |
| [aws_alb_target_group_attachment](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/lb_target_group_attachment) | One-to-many | [Plural](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_RegisterTargets.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/elbv2/target_group_attachment.go#L76-L79) |
| [aws_autoscaling_attachment](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/autoscaling_attachment) (ELB) | One-to-many | [Plural](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_AttachLoadBalancers.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/autoscaling/attachment.go#L58-L61) |
| [aws_autoscaling_attachment](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/autoscaling_attachment) (Target Group ARN) | One-to-many | [Plural](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_AttachLoadBalancerTargetGroups.html)| [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/autoscaling/attachment.go#L74-L77) |
| [aws_autoscaling_traffic_source_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/autoscaling_traffic_source_attachment) | One-to-many | [Plural](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_AttachTrafficSources.html)| [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/autoscaling/traffic_source_attachment.go#L78-L81) |
| [aws_cognito_identity_pool_roles_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/cognito_identity_pool_roles_attachment)[^2] | One-to-many | [Plural](https://docs.aws.amazon.com/cognitoidentity/latest/APIReference/API_SetIdentityPoolRoles.html) | [Plural](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/cognitoidentity/pool_roles_attachment.go#L123-L126) |
| [aws_ec2_transit_gateway_peering_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/ec2_transit_gateway_peering_attachment) | One-to-one | [Singular](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTransitGatewayPeeringAttachment.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/ec2/transitgateway_peering_attachment.go#L75-L81) |
| [aws_ec2_transit_gateway_vpc_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/ec2_transit_gateway_vpc_attachment) | One-to-one | [Singular](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTransitGatewayVpcAttachment.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/ec2/transitgateway_vpc_attachment.go#L102-L112) |
| [aws_elb_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/elb_attachment) | One-to-many | [Plural](https://docs.aws.amazon.com/elasticloadbalancing/2012-06-01/APIReference/API_RegisterInstancesWithLoadBalancer.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/elb/attachment.go#L54-L57) |
| [aws_iam_group_policy_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_group_policy_attachment) | One-to-many | [Singular](https://docs.aws.amazon.com/IAM/latest/APIReference/API_AttachGroupPolicy.html)| [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/iam/group_policy_attachment.go#L153-L156) |
| [aws_iam_policy_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_policy_attachment)[^3] | One-to-many | [Singular](https://docs.aws.amazon.com/IAM/latest/APIReference/API_AttachRolePolicy.html) | [Plural](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/iam/policy_attachment.go#L219-L230) |
| [aws_iam_role_policy_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_role_policy_attachment) | One-to-many | [Singular](https://docs.aws.amazon.com/IAM/latest/APIReference/API_AttachRolePolicy.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/iam/role_policy_attachment.go#L160-L163) |
| [aws_iam_user_policy_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_user_policy_attachment) | One-to-many | [Singular](https://docs.aws.amazon.com/IAM/latest/APIReference/API_AttachUserPolicy.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/iam/user_policy_attachment.go#L156-L159) |
| [aws_internet_gateway_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/internet_gateway_attachment) | One-to-one| [Singular](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AttachInternetGateway.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/ec2/vpc_internet_gateway.go#L190-L193) |
| [aws_iot_policy_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iot_policy_attachment) | One-to-many | [Singular](https://docs.aws.amazon.com/iot/latest/apireference/API_AttachPolicy.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/iot/policy_attachment.go#L48-L51) |
| [aws_iot_thing_principal_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iot_thing_principal_attachment) | One-to-many | [Singular](https://docs.aws.amazon.com/iot/latest/apireference/API_AttachThingPrincipal.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/iot/thing_principal_attachment.go#L49-L52) |
| [aws_lb_target_group_attachment](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/lb_target_group_attachment) | One-to-many | [Plural](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_RegisterTargets.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/elbv2/target_group_attachment.go#L76-L79) |
| [aws_lightsail_disk_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/lightsail_disk_attachment) | One-to-many | [Singular](https://docs.aws.amazon.com/lightsail/2016-11-28/api-reference/API_AttachDisk.html)| [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/lightsail/disk_attachment.go#L57-L61) |
| [aws_lightsail_lb_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/lightsail_lb_attachment) | One-to-many | [Plural](https://docs.aws.amazon.com/lightsail/2016-11-28/api-reference/API_AttachInstancesToLoadBalancer.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/lightsail/lb_attachment.go#L59-L62) |
| [aws_lightsail_lb_certificate_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/lightsail_lb_certificate_attachment) | One-to-one| [Singular](https://docs.aws.amazon.com/lightsail/2016-11-28/api-reference/API_AttachLoadBalancerTlsCertificate.html)| [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/lightsail/lb_certificate_attachment.go#L60-L63) |
| [aws_lightsail_static_ip_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/lightsail_static_ip_attachment) | One-to-one| [Singular](https://docs.aws.amazon.com/lightsail/2016-11-28/api-reference/API_AttachStaticIp.html)| [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/lightsail/static_ip_attachment.go#L50-L53) |
| [aws_network_interface_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/network_interface_attachment) | One-to-many | [Singular](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AttachNetworkInterface.html)| [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/ec2/vpc_network_interface.go#L1058-L1062) |
| [aws_network_interface_sg_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/network_interface_sg_attachment) | One-to-many | [Plural](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ModifyNetworkInterfaceAttribute.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/ec2/vpc_network_interface_sg_attachment.go#L63-L82) |
| [aws_networkmanager_connect_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/networkmanager_connect_attachment) | One-to-one| [Singular](https://docs.aws.amazon.com/networkmanager/latest/APIReference/API_CreateConnectAttachment.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/networkmanager/connect_attachment.go#L143-L149) |
| [aws_networkmanager_core_network_policy_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/networkmanager_core_network_policy_attachment) | One-to-one| [Singular](https://docs.aws.amazon.com/networkmanager/latest/APIReference/API_PutCoreNetworkPolicy.html)| [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/networkmanager/core_network.go#L513-L545) |
| [aws_networkmanager_site_to_site_vpn_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/networkmanager_site_to_site_vpn_attachment) | One-to-one| [Singular](https://docs.aws.amazon.com/networkmanager/latest/APIReference/API_CreateSiteToSiteVpnAttachment.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/networkmanager/site_to_site_vpn_attachment.go#L108-L112) |
| [aws_networkmanager_transit_gateway_registration](https://registry.terraform.io/providers/-/aws/latest/docs/resources/networkmanager_transit_gateway_registration) | One-to-one| [Singular](https://docs.aws.amazon.com/networkmanager/latest/APIReference/API_RegisterTransitGateway.html)| [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/networkmanager/transit_gateway_registration.go#L63-L66) |
| [aws_networkmanager_transit_gateway_route_table_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/networkmanager_transit_gateway_route_table_attachment) | One-to-one| [Singular](https://docs.aws.amazon.com/networkmanager/latest/APIReference/API_CreateTransitGatewayRouteTableAttachment.html)| [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/networkmanager/transit_gateway_route_table_attachment.go#L109-L113) |
| [aws_networkmanager_vpc_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/networkmanager_vpc_attachment) | One-to-one| [Singular](https://docs.aws.amazon.com/networkmanager/latest/APIReference/API_CreateVpcAttachment.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/networkmanager/vpc_attachment.go#L133-L138) |
| [aws_organizations_policy_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/organizations_policy_attachment) | One-to-many | [Singular](https://docs.aws.amazon.com/organizations/latest/APIReference/API_AttachPolicy.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/organizations/policy_attachment.go#L61-L64) |
| [aws_quicksight_iam_policy_assignment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/quicksight_iam_policy_assignment) | One-to-many | [Plural](https://docs.aws.amazon.com/quicksight/latest/APIReference/API_CreateIAMPolicyAssignment.html) | [Plural](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/quicksight/iam_policy_assignment.go#L131-L145) |
| [aws_security_group](https://registry.terraform.io/providers/-/aws/latest/docs/resources/security_group) (Egress)[^4] | One-to-many | [Plural](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AuthorizeSecurityGroupEgress.html)| [Plural](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/ec2/vpc_security_group.go#L781-L784) |
| [aws_security_group](https://registry.terraform.io/providers/-/aws/latest/docs/resources/security_group) (Ingress)[^4] | One-to-many | [Plural](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AuthorizeSecurityGroupIngress.html) | [Plural](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/ec2/vpc_security_group.go#L788-L791k) |
| [aws_security_group_rule](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/security_group_rule) (Egress)| One-to-many | [Plural](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AuthorizeSecurityGroupEgress.html)| [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/ec2/vpc_security_group_rule.go#L189-L205) |
| [aws_security_group_rule](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/security_group_rule) (Ingress) | One-to-many | [Plural](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AuthorizeSecurityGroupIngress.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/ec2/vpc_security_group_rule.go#L172-L187) |
| [aws_sesv2_dedicated_ip_assignment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/sesv2_dedicated_ip_assignment) | One-to-one| [Singular](https://docs.aws.amazon.com/ses/latest/APIReference-V2/API_PutDedicatedIpInPool.html)| [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/sesv2/dedicated_ip_assignment.go#L66-L69) |
| [aws_ssoadmin_account_assignment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/ssoadmin_account_assignment) | One-to-one| [Singular](https://docs.aws.amazon.com/singlesignon/latest/APIReference/API_CreateAccountAssignment.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/ssoadmin/account_assignment.go#L106-L113) |
| [aws_ssoadmin_customer_managed_policy_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/ssoadmin_customer_managed_policy_attachment) | One-to-many | [Singular](https://docs.aws.amazon.com/singlesignon/latest/APIReference/API_AttachCustomerManagedPolicyReferenceToPermissionSet.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/ssoadmin/customer_managed_policy_attachment.go#L90-L94) |
| [aws_ssoadmin_managed_policy_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/ssoadmin_managed_policy_attachment) | One-to-many | [Singular](https://docs.aws.amazon.com/singlesignon/latest/APIReference/API_AttachManagedPolicyToPermissionSet.html)| [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/ssoadmin/managed_policy_attachment.go#L69-L73) |
| [aws_ssoadmin_permissions_boundary_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/ssoadmin_permissions_boundary_attachment) | One-to-one| [Singular](https://docs.aws.amazon.com/singlesignon/latest/APIReference/API_PutPermissionsBoundaryToPermissionSet.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/ssoadmin/permissions_boundary_attachment.go#L105-L109) |
| [aws_volume_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/volume_attachment) | One-to-many | [Singular](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AttachVolume.html)| [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/ec2/ebs_volume_attachment.go#L106-L110) |
| [aws_vpc_security_group_egress_rule](https://registry.terraform.io/providers/-/aws/latest/docs/resources/vpc_security_group_egress_rule) | One-to-many | [Plural](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AuthorizeSecurityGroupEgress.html)| [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/ec2/vpc_security_group_egress_rule.go#L37-L40) |
| [aws_vpc_security_group_ingress_rule](https://registry.terraform.io/providers/-/aws/latest/docs/resources/vpc_security_group_ingress_rule) | One-to-many | [Plural](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AuthorizeSecurityGroupIngress.html) | [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/ec2/vpc_security_group_ingress_rule.go#L55-L58) |
| [aws_vpclattice_target_group_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/vpclattice_target_group_attachment) | One-to-many | [Plural](https://docs.aws.amazon.com/vpc-lattice/latest/APIReference/API_RegisterTargets.html)| [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/vpclattice/target_group_attachment.go#L81-L84) |
| [aws_vpn_gateway_attachment](https://registry.terraform.io/providers/-/aws/latest/docs/resources/vpn_gateway_attachment) | One-to-one| [Singular](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AttachVpnGateway.html)| [Singular](https://github.com/hashicorp/terraform-provider-aws/blob/v5.7.0/internal/service/ec2/vpnsite_gateway_attachment.go#L48-L51) |

[^1]: Due to the volume of resources with "rule" in the name (~70), only the prominent security group rule resources were included in the analysis above. While "rule" resources often follow the same relationship-style design, the ~40 examples above provided enough initial data to inform design standards.
[^2]: The structure of this API precludes it from being implemented in a singular fashion.
[^3]: Creates exclusive attachments.
[^4]: Creates exclusive rules.

Of the 44 resources documented above, 29 are of the "one-to-many" form and 17 have "plural" AWS APIs (ie. accept a list of child resources to be attached to a single parent). Of these 17, 13 resources (76%) use a "singular" Terraform implementation, where a list with one item is sent to the Create/Read/Update API, rather than allowing a single resource to manage multiple relationships. Of the remaining 4 with "plural" Terraform implementations, 2 do so to exclusively manage child relationships (`aws_security_group` Ingress/Egress variants), and one requires a "plural" implementation simply because of API limitations.

These metrics indicate a strong historical preference for representing a single API object over aligning the schema to the underlying AWS API. The primary exceptions to this are when exclusive management of all child resources is desired, such as [security group ingress/egress rules](https://registry.terraform.io/providers/-/aws/latest/docs/resources/security_group), or [IAM policy attachments](https://registry.terraform.io/providers/-/aws/latest/docs/resources/iam_policy_attachment).

## Proposal

The best practice for net-new "one-to-many" relationship resources should be to implement singular versions. Feature requests related to changing the singular nature of an existing relationship resource should be avoided unless necessary for the underlying API to function properly.

Variation from this pattern should only be done when:

1. There is a valid use case for a single resource to retain exclusive management of all parent/child relationships.
2. Manipulating the underlying AWS APIs to work with singular relationships is not possible or introduces unnecessary complexity.

### "One-to-many" Design Example

Given a fictional "plural" API `AttachChildren` with a request body like:

```
{
  "ParentId": "string",
  "Children": [
    {
      "ChildId: "string"
    }
  ]
}
```

The corresponding Terraform resource would only represent a single parent/child relationship with a configuration like:

```terraform
resource "aws_parent" "example" {
  name = "foo"
}

resource "aws_child" "example" {
  name = "bar"
}

resource "aws_child_attachment" "example" {
  parent_id = aws_parent.example.id
  child_id  = aws_child.example.id
}
```

## References

* The following feature request and PR initiated the discussion for this analysis:
    * [https://github.com/hashicorp/terraform-provider-aws/issues/9901](https://github.com/hashicorp/terraform-provider-aws/issues/9901)
    * [https://github.com/hashicorp/terraform-provider-aws/pull/32380](https://github.com/hashicorp/terraform-provider-aws/pull/32380)
# SecretsManager Secret Target Attachment

**Summary:** Assess the feasibility of replicating the `AWS::SecretsManager::SecretTargetAttachment` CloudFormation function with Terraform.
**Created**: 2023-10-25

---

The AWS Terraform provider has a [prioritized issue](https://github.com/hashicorp/terraform-provider-aws/issues/9183) requesting a Terraform AWS provider implementation of the CloudFormation [`AWS::SecretsManager::SecretTargetAttachment`](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html) function.
This document will assess the feasibility of replicating this functionality in the AWS Terraform provider and document the alternative options available using existing SecretsManager resources.

## Background

The `AWS::SecretsManager::SecretTargetAttachment` function is a convenience helper to supplement an existing SecretsManager secret with database connection information from services like Amazon RDS or Amazon Redshift.
This function has no API equivalent (see the SecretsManager [API documentation](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_Operations.html)), and appears to operate as an orchestration job working across AWS services.
In the absence of public APIs, the AWS provider cannot easily implement proper Terraform lifecycle handling on top of this workflow.
However, the existing SecretsManager resources and configuration options on RDS database resources provide options for practitioners to replicate most of this functionality.

### Manual Secret with Supplemental Connection Information

With this approach the database (RDS Postgres in this example) is initially created with a random password.
An empty secret is created at the same time.
Once database creation is complete, the username, password, and database connection information are all written to a new version of the existing secret.

```hcl
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 5.0"
    }
    random = {
      source  = "hashicorp/random"
      version = "~> 3.0"
    }
  }
}

provider "aws" {}
provider "random" {}

locals {
  username = "foo"
}

resource "random_password" "password" {
  length  = 20
  special = false
}

data "aws_rds_orderable_db_instance" "test" {
  engine         = "postgres"
  engine_version = "15.3"

  preferred_instance_classes = ["db.t3.micro", "db.t3.small"]
}

resource "aws_db_instance" "test" {
  allocated_storage    = 20
  db_name              = "testdb"
  engine               = data.aws_rds_orderable_db_instance.test.engine
  engine_version       = data.aws_rds_orderable_db_instance.test.engine_version
  instance_class       = data.aws_rds_orderable_db_instance.test.instance_class
  username             = local.username
  password             = random_password.password.result
  parameter_group_name = "default.postgres15"
  skip_final_snapshot  = true
}

resource "aws_secretsmanager_secret" "test" {
  name_prefix = "jb-test"
}

resource "aws_secretsmanager_secret_version" "test" {
  secret_id = aws_secretsmanager_secret.test.id
  secret_string = jsonencode({
    engine   = aws_db_instance.test.engine
    host     = aws_db_instance.test.address
    username = local.username
    password = random_password.password.result
    dbname   = aws_db_instance.test.db_name
    port     = aws_db_instance.test.port
  })
}
```

Manually created secrets require maintaining the lambda function executing the rotation.
Specifically, the [RotateSecret](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_RotateSecret.html) API requires the `LambdaFunctionArn` argument to be provided when setting a rotation for a manually created secret (it is technically optional, but can only be omitted for “managed” secrets created by AWS).
AWS provides Lambda function [templates](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html) for the most common secret rotation use cases, and the [AWS Serverless Application Repository](https://serverlessrepo.aws.amazon.com/application) contains many pre-built secret rotation functions.
Once a rotation Lambda function is deployed, rotation can be managed with the `aws_secretsmanager_secret_rotation` resource.

```hcl
resource "aws_secretsmanager_secret_rotation" "test" {
  secret_id = aws_secretsmanager_secret.test.id

  # Function templates available in the SecretsManager documentation,
  # and pre-built functions available in the Serverless Application
  # Repository.
  rotation_lambda_arn = aws_lambda_function.secret_rotation.arn

  rotation_rules {
    automatically_after_days = 30
  }
}
```

### Managed Secret

With this approach the database (RDS Postgres in this example) is initially created with the `manage_master_user_password` argument set to `true` (no password required).
RDS will create a new "managed" secret to store credentials as part of database creation.

```hcl
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 5.0"
    }
  }
}

provider "aws" {}

locals {
  username = "foo"
}

data "aws_rds_orderable_db_instance" "test" {
  engine         = "postgres"
  engine_version = "15.3"

  preferred_instance_classes = ["db.t3.micro", "db.t3.small"]
}

resource "aws_db_instance" "test" {
  allocated_storage    = 20
  db_name              = "testdb"
  engine               = data.aws_rds_orderable_db_instance.test.engine
  engine_version       = data.aws_rds_orderable_db_instance.test.engine_version
  instance_class       = data.aws_rds_orderable_db_instance.test.instance_class
  username             = local.username
  parameter_group_name = "default.postgres15"
  skip_final_snapshot  = true

  manage_master_user_password = true
}

# Optionally fetch the secret data if attributes need to be used as inputs
# elsewhere.
data "aws_secretsmanager_secret" "test" {
  arn = aws_db_instance.test.master_user_secret[0].secret_arn
}
```

If information about the managed secret is required as an input to other resources, the `aws_secretsmanager_secret` data source can be used.
Because this secret is managed by Amazon RDS, the secret value cannot be modified to include supplemental connection information.
This may be a limitation the `SecretTargetAttachment` CloudFormation is able to work around via some internal AWS process, but there is currently no mechanism to implement this with publicly documented APIs.

As an alternative, supplemental connection information could be applied as `tags` if it’s absolutely necessary for the information to exist on the secret itself.

```hcl
# Optionally import the managed secret and modify attributes via Terraform
# (secret value cannot be modified).
import {
  to = aws_secretsmanager_secret.test
  id = aws_db_instance.test.master_user_secret[0].secret_arn
}

resource "aws_secretsmanager_secret" "test" {
  # customize tags, description, etc.
}
```

## Proposal

Given the currently available AWS APIs, there isn’t a path to implement the workflow from the `SecretTargetAttachment` CloudFormation function in the AWS Terraform Provider.
Existing resources provide options to either fully customize a manual secret with both database credentials and connection information, or to fully offload secret management to AWS.
These options cover the core use case of storing and rotating database secrets via AWS SecretsManager.

With existing options already available in the provider, and no clear path forward the proposal is to close this issue.

## Consequences/Future Work

No work will be done to implement the requested functionality from the original issue. However, the investigation phase did uncover other potential enhancements to improve managed credential workflows in the AWS provider.

- The previous implementation of the `aws_secretsmanager_secret_rotation` resource did not allow for managed secret rotations to be modified (`rotation_lambda_arn` is required, but managed secrets omit this value on update). An [enhancement issue](https://github.com/hashicorp/terraform-provider-aws/issues/34108) was opened to support this use case, and the implementation was completed with [#34180](https://github.com/hashicorp/terraform-provider-aws/pull/34180).

- The `aws_redshift_cluster` resource did not implement support for managing master passwords. An [enhancement issue](https://github.com/hashicorp/terraform-provider-aws/issues/34169) was opened to support this use case, and the implementation was completed with [#34182](https://github.com/hashicorp/terraform-provider-aws/pull/34182).

## References

AWS Documentation

- [SecretsManager API Reference](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_Operations.html)
- [RDS Managed Secrets Guide](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-secrets-manager.html#rds-secrets-manager-db-instance)
- [`AWS::SecretsManager::SecretTargetAttachment`](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html)

Terraform Resources

- [`aws_secretsmanager_secret`](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/secretsmanager_secret)
- [`aws_secretsmanager_secret_version`](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/secretsmanager_secret_version)
- [`aws_secretsmanager_secret_rotation`](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/secretsmanager_secret_rotation)
- [`aws_db_instance`](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/db_instance)
