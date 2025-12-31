# terraform-aws-iamsr

Reusable terraform modulo for create and manage policies and roles.




## Usage
```hcl
module "<name>" {
  source = "git::https://github.com/wfercosta/terraform-aws-iamsr.git?ref=main"

  # required and optional inputs
}
```

## Inputs
| Name             | Description                  | Type        | Required | Default |
| ---------------- | ---------------------------- | ----------- | -------- | ------- |
| replacement_vars | Dictionary of key and values | Map(string) | no       | -       |
| roles            | Dictionary of key and values | Map(object) | no       | -       |
| policies         | Dictionary of key and values | Map(string) | no       | -       |

### Objects Definition

#### Replacement Variable
| Attribute            | Type     | Required | Description                         |
|----------------------|----------|----------|-------------------------------------|
| Variable Name        | string   | yes      | Name of the variable to be replaced |
| Variable Value       | string   | yes      | Value of the variable to be used    |


#### Policy
| Attribute                 | Type         | Required | Description                              |
|---------------------------|--------------|----------|------------------------------------------|
| Policy Name               | string       | yes      | Policy name that will be created in AWS  |
| Policy Relative File Path | string       | yes      | Policy file relative path                |


#### Role
| Attribute            | Type         | Required | Description                                        |
|----------------------|--------------|----------|----------------------------------------------------|
| trust_role           | string       | yes      | Trust role file relative path                      |
| policies_attachments | list(string) | yes      | List of policies names to be attached to this role |



## Outputs
| Name | Description |
| ---- | ----------- |
| NA   | NA |


## Examples
* examples/basic


## Assumptions & Constraints
Not applicable


## Security Considerations
* IAM permissions required


## Contributing
No guidelines defined
