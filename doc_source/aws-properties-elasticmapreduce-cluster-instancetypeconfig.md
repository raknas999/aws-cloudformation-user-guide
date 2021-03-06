# Amazon EMR Cluster InstanceTypeConfig<a name="aws-properties-elasticmapreduce-cluster-instancetypeconfig"></a>

Use the `InstanceTypeConfig` property to configure an instance types in an instance fleet\. This propery determines which EC2 instances that Amazon EMR attempts to provision to fulfill On\-Demand and Spot target capacities\. You can configure a maximum of five instance types in a fleet\. The `InstanceTypeConfigs` property of the [Amazon EMR Cluster InstanceFleetConfig](aws-properties-elasticmapreduce-cluster-instancefleetconfig.md) resource contains a list of `InstanceTypeConfig` property types\.

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-instancetypeconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-instancetypeconfig-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-instancetypeconfig-bidprice)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-instancetypeconfig-bidpriceaspercentageofondemandprice)" : Double,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-instancetypeconfig-configurations)" : [ Configuration, ...],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-instancetypeconfig-ebsconfiguration)" : EbsConfiguration,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-instancetypeconfig-instancetype)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-instancetypeconfig-weightedcapacity)" : Integer
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-instancetypeconfig-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-instancetypeconfig-bidprice): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-instancetypeconfig-bidpriceaspercentageofondemandprice): Double
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-instancetypeconfig-configurations):
  - Configuration
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-instancetypeconfig-ebsconfiguration):
  EbsConfiguration
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-instancetypeconfig-instancetype): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-instancetypeconfig-weightedcapacity): Integer
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-instancetypeconfig-properties"></a>

`BidPrice`  
The bid price for each EC2 Spot Instance type, as defined by `InstanceType`\. `BidPrice` is expressed in USD\. For more information, see [InstanceTypeConfig](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_InstanceTypeConfig.html) in the *Amazon EMR API Reference*\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`BidPriceAsPercentageOfOnDemandPrice`  
The bid price, as a percentage of the On\-Demand price, for each EC2 Spot instance as defined by `InstanceType`\. `BidPriceAsPercentageOfOnDemandPrice`is expressed as a number\. For more information, see [InstanceTypeConfig](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_InstanceTypeConfig.html) in the *Amazon EMR API Reference*\.  
*Required: *No  
*Type*: Double  
*Update requires*: Replacement

`Configurations`  
A configuration classification that applies when provisioning cluster instances\. This  can include configurations for applications and software that run on the cluster\. Duplicates are not allowed\.  
*Required: *No  
*Type*: List of [Amazon EMR Cluster Configurations](aws-properties-emr-cluster-configuration.md)  
*Update requires*: Replacement

`EbsConfiguration`  
The configuration of Amazon Elastic Block Store \(Amazon EBS\) that is attached to each instance as defined by `InstanceType`\.  
*Required: *No  
*Type*: [Amazon EMR EbsConfiguration](aws-properties-emr-ebsconfiguration.md)  
*Update requires*: Replacement

`InstanceType`  
An EC2 instance type, such as `m3.xlarge`\. For constraints, see [InstanceTypeConfig](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_InstanceTypeConfig.html) in the *Amazon EMR API Reference*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`WeightedCapacity`  
The number of units that a provisioned instance of this type provides toward fulfilling the target capacities defined in `InstanceFleetConfig`\. For more information, see [InstanceTypeConfig](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_InstanceTypeConfig.html) in the *Amazon EMR API Reference*\.  
*Required: *No  
*Type*: Integer  
*Update requires*: Replacement