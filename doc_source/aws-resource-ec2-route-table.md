# AWS::EC2::RouteTable<a name="aws-resource-ec2-route-table"></a>

Creates a new route table within a VPC\. After you create a new route table, you can add routes and associate the table with a subnet\.


+ [Syntax](#aws-resource-ec2-routetable-syntax)
+ [Properties](#w3ab2c21c10d419b9)
+ [Return Values](#w3ab2c21c10d419c11)
+ [Examples](#w3ab2c21c10d419c13)
+ [See Also](#w3ab2c21c10d419c15)

## Syntax<a name="aws-resource-ec2-routetable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-routetable-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::RouteTable",
   "Properties" : {
      "VpcId" : String,
      "Tags" : [ Resource Tag, ... ]
   }
}
```

### YAML<a name="aws-resource-ec2-routetable-syntax.yaml"></a>

```
Type: "AWS::EC2::RouteTable"
Properties: 
  VpcId: String
  Tags:
    - Resource Tag
```

## Properties<a name="w3ab2c21c10d419b9"></a>

`VpcId`  
The ID of the VPC where the route table will be created\.  
Example: vpc\-11ad4878  
*Required*: Yes  
*Type*: String  
*Update requires*: Replacement

`Tags`  
An arbitrary set of tags \(key–value pairs\) for this route table\.  
*Required: *No  
*Type*:   
*Update requires*: No interruption\.

## Return Values<a name="w3ab2c21c10d419c11"></a>

### Ref<a name="w3ab2c21c10d419c11b2"></a>

When you specify an `AWS::EC2::RouteTable` type as an argument to the `Ref` function, AWS CloudFormation returns the route table ID, such as `rtb-12a34567`\.

For more information about using the `Ref` function, see Ref\.

## Examples<a name="w3ab2c21c10d419c13"></a>

The following example snippet uses the VPC ID from a VPC named *myVPC* that was declared elsewhere in the same template\.

### JSON<a name="aws-resource-ec2-routetable-example-1.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myRouteTable" : {
         "Type" : "AWS::EC2::RouteTable",
         "Properties" : {
            "VpcId" : { "Ref" : "myVPC" },
            "Tags" : [ { "Key" : "foo", "Value" : "bar" } ]
         }
      }
   }
}
```

### YAML<a name="aws-resource-ec2-routetable-example-1.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  myRouteTable:
    Type: AWS::EC2::RouteTable
    Properties:
      VpcId:
        Ref: myVPC
      Tags:
      - Key: foo
        Value: bar
```

## See Also<a name="w3ab2c21c10d419c15"></a>

+ AWS::EC2::Route

+ [CreateRouteTable](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateRouteTable.html) in the *Amazon EC2 API Reference*

+ [Route Tables](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Route_Tables.html) in the *Amazon VPC User Guide*

+ [Using Tags](http://docs.aws.amazon.com/AWSEC2/latest/DeveloperGuide/Using_Tags.html) in the *Amazon Elastic Compute Cloud User Guide*