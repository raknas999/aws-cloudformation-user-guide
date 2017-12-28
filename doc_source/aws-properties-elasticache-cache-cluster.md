# AWS::ElastiCache::CacheCluster<a name="aws-properties-elasticache-cache-cluster"></a>

The AWS::ElastiCache::CacheCluster type creates an Amazon ElastiCache cache cluster\.


+ [Syntax](#aws-resource-elasticache-cachecluster-syntax)
+ [Properties](#aws-properties-elasticache-cache-cluster-prop)
+ [Return Values](#aws-properties-elasticache-cache-cluster-ref)
+ [Template Snippets](#w3ab2c21c10d539c13)
+ [See Also](#w3ab2c21c10d539c15)

## Syntax<a name="aws-resource-elasticache-cachecluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticache-cachecluster-syntax.json"></a>

```
{
   "Type" : "AWS::ElastiCache::CacheCluster",
   "Properties" :
   {
      "AutoMinorVersionUpgrade" : Boolean,
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticache-cachecluster-azmode)" : String,
      "CacheNodeType" : String,
      "CacheParameterGroupName" : String,
      "CacheSecurityGroupNames" : [ String, ... ],
      "CacheSubnetGroupName" : String,
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticache-cachecluster-clustername)" : String,
      "Engine" : String,
      "EngineVersion" : String,
      "NotificationTopicArn" : String,
      "NumCacheNodes" : Integer,
      "Port" : Integer,
      "PreferredAvailabilityZone" : String,
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticache-cachecluster-preferredavailabilityzones)" : [String, ... ],
      "PreferredMaintenanceWindow" : String,
      "SnapshotArns" : [String, ... ],
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticache-cachecluster-snapshotname)" : String,
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticache-cachecluster-snapshotretentionlimit)" : Integer,
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticache-cachecluster-snapshotwindow)" : String,
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticache-cachecluster-tags)" : [Resource Tag, ...],
      "VpcSecurityGroupIds" : [String, ...]
   }
}
```

### YAML<a name="aws-resource-elasticache-cachecluster-syntax.yaml"></a>

```
Type: "AWS::ElastiCache::CacheCluster"
Properties:
  AutoMinorVersionUpgrade: Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticache-cachecluster-azmode): String
  CacheNodeType: String
  CacheParameterGroupName: String
  CacheSecurityGroupNames:
    - String
  CacheSubnetGroupName: String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticache-cachecluster-clustername): String
  Engine: String
  EngineVersion: String
  NotificationTopicArn: String
  NumCacheNodes: Integer
  Port: Integer
  PreferredAvailabilityZone: String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticache-cachecluster-preferredavailabilityzones):
    - String
  PreferredMaintenanceWindow: String
  SnapshotArns:
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticache-cachecluster-snapshotname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticache-cachecluster-snapshotretentionlimit): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticache-cachecluster-snapshotwindow): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticache-cachecluster-tags):
    - Resource Tag
  VpcSecurityGroupIds:
    - String
```

## Properties<a name="aws-properties-elasticache-cache-cluster-prop"></a>

For valid values, see [CreateCacheCluster](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateCacheCluster.html) in the *Amazon ElastiCache API Reference*\.

`AutoMinorVersionUpgrade`  
Indicates that minor engine upgrades will be applied automatically to the cache cluster during the maintenance window\.  
*Required: *No  
*Type*: Boolean  
*Default*: `true`  
*Update requires*: No interruption

`AZMode`  
For Memcached cache clusters, indicates whether the nodes are created in a single Availability Zone or across multiple Availability Zones in the cluster's region\. For valid values, see [CreateCacheCluster](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateCacheCluster.html) in the *Amazon ElastiCache API Reference*\.  
*Required: *Conditional\. If you specify multiple Availability Zones in the `PreferredAvailabilityZones` property, you must specify cross Availability Zones for this property\.  
*Type*: String  
*Update requires*: No interruption

`CacheNodeType`  
The compute and memory capacity of nodes in a cache cluster\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Some interruptions

`CacheParameterGroupName`  
The name of the cache parameter group that is associated with this cache cluster\.  
*Required: *No  
*Type*: String  
*Update requires*: Some interruptions

`CacheSecurityGroupNames`  
A list of cache security group names that are associated with this cache cluster\. If your cache cluster is in a VPC, specify the `VpcSecurityGroupIds` property instead\.  
*Required: *Conditional: If your cache cluster isn't in a VPC, you must specify this property\.  
*Type*: List of String values  
*Update requires*: No interruption

`CacheSubnetGroupName`  
The cache subnet group that you associate with a cache cluster\.  
*Required: *Conditional\. If you specified the `VpcSecurityGroupIds` property, you must specify this property\.  
*Type*: String  
*Update requires*: Replacement

`ClusterName`  
A name for the cache cluster\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the cache cluster\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
The name must contain 1 to 20 alphanumeric characters or hyphens\. The name must start with a letter and cannot end with a hyphen or contain two consecutive hyphens\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`Engine`  
The name of the cache engine to be used for this cache cluster, such as `memcached` or `redis`\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`EngineVersion`  
The version of the cache engine to be used for this cluster\.  
*Required: *No  
*Type*: String  
*Update requires*: Some interruptions

`NotificationTopicArn`  
The Amazon Resource Name \(ARN\) of the Amazon Simple Notification Service \(SNS\) topic to which notifications will be sent\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`NumCacheNodes`  
The number of cache nodes that the cache cluster should have\.  
*Required: *Yes  
*Type*: Integer  
*Update requires*: No interruption\. However, if the `PreferredAvailabilityZone` and `PreferredAvailabilityZones` properties were not previously specified and you don't specify any new values, an update requires replacement\.

`Port`  
The port number on which each of the cache nodes will accept connections\.  
*Required: *No  
*Type*: Integer  
*Update requires*: Replacement

`PreferredAvailabilityZone`  
The Amazon EC2 Availability Zone in which the cache cluster is created\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`PreferredAvailabilityZones`  
For Memcached cache clusters, the list of Availability Zones in which cache nodes are created\. The number of Availability Zones listed must equal the number of cache nodes\. For example, if you want to create three nodes in two different Availability Zones, you can specify `["us-east-1a", "us-east-1a", "us-east-1b"]`, which would create two nodes in us\-east\-1a and one node in us\-east\-1b\.  
If you specify a subnet group and you're creating your cache cluster in a VPC, you must specify Availability Zones that are associated with the subnets in the subnet group that you've chosen\.  
If you want all the nodes in the same Availability Zone, use the `PreferredAvailabilityZone` property or repeat the Availability Zone multiple times in the list\.  
*Required: *No  
*Type*: List of String values  
If you specify an Availability Zone that was previously specified in the template, such as in the `PreferredAvailabilityZone` property, the update requires some interruptions\. Also, if the `PreferredAvailabilityZones` property was already specified and you're updating its values \(regardless of whether you specify the same Availability Zones\), the update requires some interruptions\.  
All other updates require replacement\.

`PreferredMaintenanceWindow`  
The weekly time range \(in UTC\) during which system maintenance can occur\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`SnapshotArns`  
The ARN of the snapshot file that you want to use to seed a new Redis cache cluster\. If you manage a Redis instance outside of Amazon ElastiCache, you can create a new cache cluster in ElastiCache by using a snapshot file that is stored in an Amazon S3 bucket\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: Replacement

`SnapshotName`  
The name of a snapshot from which to restore data into a new Redis cache cluster\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`SnapshotRetentionLimit`  
For Redis cache clusters, the number of days for which ElastiCache retains automatic snapshots before deleting them\. For example, if you set the value to `5`, a snapshot that was taken today will be retained for 5 days before being deleted\.  
*Required: *No  
*Type*: Integer  
*Update requires*: No interruption

`SnapshotWindow`  
For Redis cache clusters, the daily time range \(in UTC\) during which ElastiCache will begin taking a daily snapshot of your node group\. For example, you can specify `05:00-09:00`\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`Tags`  
An arbitrary set of tags \(key–value pairs\) for this cache cluster\.  
*Required: *No  
*Type*:   
*Update requires*: No interruption\.

`VpcSecurityGroupIds`  
A list of VPC security group IDs\. If your cache cluster isn't in a VPC, specify the `CacheSecurityGroupNames` property instead\.  
You must use the `AWS::EC2::SecurityGroup` resource instead of the `AWS::ElastiCache::SecurityGroup` resource in order to specify an ElastiCache security group that is in a VPC\. In addition, if you use the [default VPC](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/default-vpc.html) for your AWS account, you must use the `Fn::GetAtt` function and the `GroupId` attribute to retrieve security group IDs \(instead of the `Ref` function\)\. To see a sample template, see the Template Snippet section\.
*Required: *Conditional: If your cache cluster is in a VPC, you must specify this property\.  
*Type*: List of String values  
*Update requires*: No interruption

## Return Values<a name="aws-properties-elasticache-cache-cluster-ref"></a>

### Ref<a name="w3ab2c21c10d539c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="w3ab2c21c10d539c11b4"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`ConfigurationEndpoint.Address`  
The DNS address of the configuration endpoint for the Memcached cache cluster\.

`ConfigurationEndpoint.Port`  
The port number of the configuration endpoint for the Memcached cache cluster\.

`RedisEndpoint.Address`  
The DNS address of the configuration endpoint for the Redis cache cluster\.

`RedisEndpoint.Port`  
The port number of the configuration endpoint for the Redis cache cluster\.

For more information about using `Fn::GetAtt`, see Fn::GetAtt\.

## Template Snippets<a name="w3ab2c21c10d539c13"></a>

### Cluster in a Default VPC<a name="w3ab2c21c10d539c13b2"></a>

The following snippet describes an ElastiCache cluster in a security group that is in a [default VPC](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/default-vpc.html)\. Usually, a security group in a VPC requires the VPC ID to be specified\. In this case, no VPC ID is needed because the security group uses the default VPC\. If you want to specify a VPC for the security group, specify its `VpcId` property\.

For the cache cluster, the `VpcSecurityGroupIds` property is used to associate the cluster with the security group\. Because the `VpcSecurityGroupIds` property requires security group IDs \(not security group names\), the template snippet uses the `Fn::GetAtt` function instead of a `Ref` function on the `ElasticacheSecurityGroup` resource\. The `Ref` function will return the security group name\. If you specify a VPC ID for the security group, `Ref` returns the security group ID\.

 Note that `InstanceSecurityGroup` refers to the logical name of a security group that is not actually defined in this snippet\. To learn more about the `SourceSecurityGroupName` property, see [AWS::EC2::SecurityGroupIngress](aws-properties-ec2-security-group-ingress.md)\. 

#### JSON<a name="aws-resource-elasticache-cachecluster-example1.json"></a>

```
"ElasticacheSecurityGroup": {
  "Type": "AWS::EC2::SecurityGroup",
  "Properties": {
    "GroupDescription": "Elasticache Security Group",
    "SecurityGroupIngress": [ {
      "IpProtocol": "tcp",
      "FromPort": "11211",
      "ToPort": "11211",
      "SourceSecurityGroupName": {"Ref": "InstanceSecurityGroup"}
    } ]
  }
},
"ElasticacheCluster": {
  "Type": "AWS::ElastiCache::CacheCluster",
  "Properties": {
    "AutoMinorVersionUpgrade": "true",
    "Engine": "memcached",
    "CacheNodeType": "cache.t2.micro",
    "NumCacheNodes": "1",
    "VpcSecurityGroupIds": [{"Fn::GetAtt": [ "ElasticacheSecurityGroup", "GroupId"]}]
  }
}
```

#### YAML<a name="aws-resource-elasticache-cachecluster-example1.yaml"></a>

```
ElasticacheSecurityGroup:
  Type: "AWS::EC2::SecurityGroup"
  Properties:
    GroupDescription: "Elasticache Security Group"
    SecurityGroupIngress:
      -
        IpProtocol: "tcp"
        FromPort: "11211"
        ToPort: "11211"
        SourceSecurityGroupName:
          Ref: "InstanceSecurityGroup"
ElasticacheCluster:
  Type: "AWS::ElastiCache::CacheCluster"
  Properties:
    AutoMinorVersionUpgrade: "true"
    Engine: "memcached"
    CacheNodeType: "cache.t2.micro"
    NumCacheNodes: "1"
    VpcSecurityGroupIds:
      -
        Fn::GetAtt:
          - "ElasticacheSecurityGroup"
          - "GroupId"
```

### Memcached Nodes in Multiple Availability Zones<a name="w3ab2c21c10d539c13b4"></a>

The following example launches a cache cluster with three nodes, where two nodes are created in us\-west\-2a and one is created in us\-west\-2b\.

#### JSON<a name="aws-resource-elasticache-cachecluster-example2.json"></a>

```
"myCacheCluster" : {
  "Type": "AWS::ElastiCache::CacheCluster",
  "Properties" : {
    "AZMode" : "cross-az",
    "CacheNodeType" : "cache.m3.medium",
    "Engine" : "memcached",
    "NumCacheNodes" : "3",
    "PreferredAvailabilityZones" : [ "us-west-2a", "us-west-2a", "us-west-2b" ]
  }
}
```

#### YAML<a name="aws-resource-elasticache-cachecluster-example2.yaml"></a>

```
myCacheCluster:
  Type: "AWS::ElastiCache::CacheCluster"
  Properties:
    AZMode: "cross-az"
    CacheNodeType: "cache.m3.medium"
    Engine: "memcached"
    NumCacheNodes: "3"
    PreferredAvailabilityZones:
      - "us-west-2a"
      - "us-west-2a"
      - "us-west-2b"
```

## See Also<a name="w3ab2c21c10d539c15"></a>

+ [CreateCacheCluster](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateCacheCluster.html) in the *Amazon ElastiCache API Reference Guide*

+ [ModifyCacheCluster](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_ModifyCacheCluster.html) in the *Amazon ElastiCache API Reference Guide*