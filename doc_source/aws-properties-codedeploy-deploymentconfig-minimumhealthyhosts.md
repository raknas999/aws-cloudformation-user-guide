# AWS CodeDeploy DeploymentConfig MinimumHealthyHosts<a name="aws-properties-codedeploy-deploymentconfig-minimumhealthyhosts"></a>

`MinimumHealthyHosts` is a property of the [AWS::CodeDeploy::DeploymentConfig](aws-resource-codedeploy-deploymentconfig.md) resource that defines how many instances must remain healthy during an AWS CodeDeploy deployment\.

## Syntax<a name="w3ab2c21c14d311b5"></a>

### JSON<a name="aws-properties-codedeploy-deploymentconfig-minimumhealthyhosts-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codedeploy-deploymentconfig-minimumhealthyhosts-type)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codedeploy-deploymentconfig-minimumhealthyhosts-value)" : Integer
}
```

### YAML<a name="aws-properties-codedeploy-deploymentconfig-minimumhealthyhosts-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codedeploy-deploymentconfig-minimumhealthyhosts-type): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codedeploy-deploymentconfig-minimumhealthyhosts-value): Integer
```

## Properties<a name="w3ab2c21c14d311b7"></a>

`Type`  
The type of count to use, such as an absolute value or a percentage of the total number of instances in the deployment\. For valid values, see [MinimumHealthyHosts](http://docs.aws.amazon.com/codedeploy/latest/APIReference/API_MinimumHealthyHosts.html) in the *AWS CodeDeploy API Reference*\.  
*Required: *Yes  
*Type*: String

`Value`  
The minimum number of healthy instances\.  
*Required: *Yes  
*Type*: Integer