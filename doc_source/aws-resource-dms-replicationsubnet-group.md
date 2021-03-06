# AWS::DMS::ReplicationSubnetGroup<a name="aws-resource-dms-replicationsubnet-group"></a>

The `AWS::DMS::ReplicationSubnetGroup` resource creates an AWS DMS replication subnet group\. Subnet groups must contain at least two subnets in two different Availability Zones in the same region\.

**Note**  
Resource creation will fail if the `dms-vpc-role` IAM role doesn't already exist\. For more information, see [ Creating the IAM Roles to Use With the AWS CLI and AWS DMS API](http://docs.aws.amazon.com/dms/latest/userguide/CHAP_Security.APIRole.html) in the *AWS Database Migration Service User Guide*\.


+ [Syntax](#aws-resource-dms-replicationsubnet-group-syntax)
+ [Properties](#aws-resource-dms-replicationsubnet-group-prop)
+ [Return Value](#w3ab2c21c10d327c13)
+ [Example](#aws-resource-dms-replicationsubnet-group-example)
+ [See Also](#w3ab2c21c10d327c17)

## Syntax<a name="aws-resource-dms-replicationsubnet-group-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dms-replicationsubnet-group-syntax.json"></a>

```
{
  "Type" : "AWS::DMS::ReplicationSubnetGroup",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationsubnetgroup-replicationsubnetgroupidentifier)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationsubnetgroup-replicationsubnetgroupdescription)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationsubnetgroup-subnetids)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationsubnetgroup-tags)" : [ Resource Tag, ... ]
  }
}
```

### YAML<a name="aws-resource-dms-replicationsubnetgroup-syntax.yaml"></a>

```
Type: "AWS::DMS::ReplicationSubnetGroup"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationsubnetgroup-replicationsubnetgroupidentifier): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationsubnetgroup-replicationsubnetgroupdescription): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationsubnetgroup-subnetids):
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationsubnetgroup-tags):
    - Resource Tag
```

## Properties<a name="aws-resource-dms-replicationsubnet-group-prop"></a>

`ReplicationSubnetGroupIdentifier`  
The identifier for the replication subnet group\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the identifier\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`ReplicationSubnetGroupDescription`  
The description for the replication subnet group\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`SubnetIds`  
The EC2 subnet IDs for the replication subnet group\.  
*Required: *Yes  
*Type*: List of String values  
*Update requires*: No interruption

`Tags`  
The tags that you want to attach to the AWS DMS replication subnet group\.  
*Required: *No  
*Type*: A list of resource tags in key\-value format\.  
*Update requires*: Replacement 

## Return Value<a name="w3ab2c21c10d327c13"></a>

### Ref<a name="w3ab2c21c10d327c13b2"></a>

When you pass the logical ID of an `AWS::DMS::ReplicationSubnetGroup` resource to the intrinsic `Ref` function, the function returns the name of the replication subnet group, such as `mystack-myrepsubnetgroup-0a12bc456789de0fg`\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="aws-resource-dms-replicationsubnet-group-example"></a>

### JSON<a name="aws-resource-dms-replicationsubnet-group-example.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myReplicationSubnetGroup" : {
         "Type" : "AWS::DMS::ReplicationSubnetGroup",
         "Properties" : {
            "ReplicationSubnetGroupIdentifier" : "identifier",
            "ReplicationSubnetGroupDescription" : "description",
            "SubnetIds" : [ "subnet-7b5b4112", "subnet-7b5b4115" ],
            "Tags" : [ {"Key" : "String", "Value" : "String"} ]
         }
      }
   }
}
```

### YAML<a name="aws-resource-dms-replicationsubnet-group-example.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources: 
  myReplicationSubnetGroup: 
    Type: "AWS::DMS::ReplicationSubnetGroup"
    Properties: 
      ReplicationSubnetGroupIdentifier: "identifier"
      ReplicationSubnetGroupDescription: "description"
      SubnetIds: 
        - "subnet-7b5b4112"
        - "subnet-7b5b4115"
      Tags: 
        - 
          Key: "String"
          Value: "String"
```

## See Also<a name="w3ab2c21c10d327c17"></a>

+ [CreateReplicationSubnetGroup](http://docs.aws.amazon.com/dms/latest/APIReference/API_CreateReplicationSubnetGroup.html) in the *AWS Database Migration Service API Reference*\.

+ [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)