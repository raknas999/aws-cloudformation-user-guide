# Amazon CloudWatch Events Rule RunCommandParameters<a name="aws-properties-events-rule-runcommandparameters"></a>

<a name="aws-properties-events-rule-runcommandparameters-description"></a>The `RunCommandParameters` property type specifies parameters used when an Amazon CloudWatch Events rule invokes Amazon EC2 Systems Manager Run Command\.

<a name="aws-properties-events-rule-runcommandparameters-inheritance"></a> `RunCommandParameters` is a property of the [CloudWatch Events Rule Target](aws-properties-events-rule-target.md) property type\. 

## Syntax<a name="aws-properties-events-rule-runcommandparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-runcommandparameters-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-runcommandparameters-runcommandtargets)" : [ RunCommandTarget, ... ]
}
```

### YAML<a name="aws-properties-events-rule-runcommandparameters-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-runcommandparameters-runcommandtargets): 
  - RunCommandTarget
```

## Properties<a name="aws-properties-events-rule-runcommandparameters-properties"></a>

For more information, including constraints and valid values, see [RunCommandParameters](http://docs.aws.amazon.com/AmazonCloudWatchEvents/latest/APIReference/API_RunCommandParameters.html) in the *Amazon CloudWatch Events API Reference*\.

`RunCommandTargets`  
The criteria \(either InstanceIds or a tag\) that specifies which EC2 instances that the command is sent to\.  
Currently, you can include only one `RunCommandTarget` block, which specifies a list of InstanceIds or a tag\.
 *Required*: Yes  
 *Type*: List of [CloudWatch Events Rule RunCommandTarget](aws-properties-events-rule-runcommandtarget.md)  
 *Update requires*: No interruption 