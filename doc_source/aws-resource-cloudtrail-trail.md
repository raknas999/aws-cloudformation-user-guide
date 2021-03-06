# AWS::CloudTrail::Trail<a name="aws-resource-cloudtrail-trail"></a>

Use the `AWS::CloudTrail::Trail` resource to create a trail and specify where logs are published\. An AWS CloudTrail \(CloudTrail\) trail can capture AWS API calls made by your AWS account and publish the logs to an Amazon S3 bucket\. For more information, see [What is AWS CloudTrail?](http://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html) in the *AWS CloudTrail User Guide*\.


+ [Syntax](#aws-resource-cloudtrail-trail-syntax)
+ [Properties](#w3ab2c21c10d197b9)
+ [Return Values](#w3ab2c21c10d197c11)
+ [Example](#aws-resource-cloudtrail-trail-examples)

## Syntax<a name="aws-resource-cloudtrail-trail-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudtrail-trail-syntax.json"></a>

```
{
  "Type" : "AWS::CloudTrail::Trail",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-cloudwatchlogsloggrouparn)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-cloudwatchlogsrolearn)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-enablelogfilevalidation)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-eventselectors)" : [ EventSelector, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-includeglobalserviceevents)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-islogging)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-ismultiregiontrail)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-kmskeyid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-s3bucketname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-s3keyprefix)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-snstopicname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-tags)" : [ Resource Tag, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-trailname)" : String
  }
}
```

### YAML<a name="aws-resource-cloudtrail-trail-syntax.yaml"></a>

```
Type: "AWS::CloudTrail::Trail"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-cloudwatchlogsloggrouparn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-cloudwatchlogsrolearn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-enablelogfilevalidation): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-eventselectors):
    - EventSelector
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-includeglobalserviceevents): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-islogging): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-ismultiregiontrail): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-kmskeyid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-s3bucketname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-s3keyprefix): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-snstopicname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-tags):
    - Resource Tag
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudtrail-trail-trailname): String
```

## Properties<a name="w3ab2c21c10d197b9"></a>

For more information and property constraints, see [CreateTrail](http://docs.aws.amazon.com/awscloudtrail/latest/APIReference/ API_CreateTrail.html) in the *AWS CloudTrail API Reference*\.

`CloudWatchLogsLogGroupArn`  
The Amazon Resource Name \(ARN\) of a log group to which CloudTrail logs will be delivered\.  
*Required: *Conditional\. This property is required if you specify the `CloudWatchLogsRoleArn` property\.  
*Type*: String  
*Update requires*: No interruption

`CloudWatchLogsRoleArn`  
The role ARN that Amazon CloudWatch Logs \(CloudWatch Logs\) assumes to write logs to a log group\. For more information, see [Role Policy Document for CloudTrail to Use CloudWatch Logs for Monitoring](http://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-required-policy-for-cloudwatch-logs.html) in the *AWS CloudTrail User Guide*\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`EnableLogFileValidation`  
Indicates whether CloudTrail validates the integrity of log files\. By default, AWS CloudFormation sets this value to `false`\. When you disable log file integrity validation, CloudTrail stops creating digest files\. For more information, see [CreateTrail](http://docs.aws.amazon.com/awscloudtrail/latest/APIReference/API_CreateTrail.html) in the *AWS CloudTrail API Reference*\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: No interruption

`EventSelectors`  
Configures logging for management and data events\.  
*Required: *No  
*Type*: List of [CloudTrail Trail EventSelector](aws-properties-cloudtrail-trail-eventselector.md)  
*Update requires*: No interruption

`IncludeGlobalServiceEvents`  
Indicates whether the trail is publishing events from global services, such as IAM, to the log files\. By default, AWS CloudFormation sets this value to `false`\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: No interruption

`IsLogging`  
Indicates whether the CloudTrail trail is currently logging AWS API calls\.  
*Required: *Yes  
*Type*: Boolean  
*Update requires*: No interruption

`IsMultiRegionTrail`  
Indicates whether the CloudTrail trail is created in the region in which you create the stack \(`false`\) or in all regions \(`true`\)\. By default, AWS CloudFormation sets this value to `false`\. For more information, see [How Does CloudTrail Behave Regionally and Globally?](http://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-concepts.html#cloudtrail-concepts-regional-and-global-services) in the *AWS CloudTrail User Guide*\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: No interruption

`KMSKeyId`  
The AWS Key Management Service \(AWS KMS\) key ID that you want to use to encrypt CloudTrail logs\. You can specify an alias name \(prefixed with `alias/`\), an alias ARN, a key ARN, or a globally unique identifier\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`S3BucketName`  
The name of the Amazon S3 bucket where CloudTrail publishes log files\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`S3KeyPrefix`  
An Amazon S3 object key prefix that precedes the name of all log files\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`SnsTopicName`  
The name of an Amazon SNS topic that is notified when new log files are published\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`Tags`  
An arbitrary set of tags \(key–value pairs\) for this trail\.  
*Required: *No  
*Type*:   
*Update requires*: No interruption\.

`TrailName`  
The name of the trail\. For constraint information, see [CreateTrail](http://docs.aws.amazon.com/awscloudtrail/latest/APIReference/API_CreateTrail.html) in the *AWS CloudTrail API Reference*\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

## Return Values<a name="w3ab2c21c10d197c11"></a>

### Ref<a name="w3ab2c21c10d197c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="aws-resource-cloudtrail-trail-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
The ARN of the CloudTrail trail, such as `arn:aws:cloudtrail:us-east-2:123456789012:trail/myCloudTrail`\.

`SnsTopicArn`  
The ARN of the Amazon SNS topic that's associated with the CloudTrail trail, such as `arn:aws:sns:us-east-2:123456789012:mySNSTopic`\.

For more information about using `Fn::GetAtt`, see Fn::GetAtt\.

## Example<a name="aws-resource-cloudtrail-trail-examples"></a>

The following example creates a CloudTrail trail, an Amazon S3 bucket where logs are published, and an Amazon SNS topic where notifications are sent\. The bucket and topic policies allow CloudTrail \(from the specified regions\) to publish logs to the Amazon S3 bucket and to send notifications to an email that you specify\. Because CloudTrail automatically writes to the `bucket_name/AWSLogs/account_ID/` folder, the bucket policy grants write privileges for that prefix\. For information about CloudTrail bucket policies, see [Amazon S3 Bucket Policy](http://docs.aws.amazon.com/awscloudtrail/latest/userguide/create_trail_bucket_policy.html) in the *AWS CloudTrail User Guide*\.

For more information about the regions that CloudTrail supports, see [Supported Regions](http://docs.aws.amazon.com/awscloudtrail/latest/userguide/what_is_cloud_trail_supported_regions.html#what_is_cloud_trail_supported_regions.title) in the *AWS CloudTrail User Guide*\.

### JSON<a name="aws-resource-cloudtrail-trail-example.json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
  "Parameters" : {
    "OperatorEmail": {
      "Description": "Email address to notify when new logs are published.",
      "Type": "String"
    }
  },
  "Resources" : {
    "S3Bucket": {
      "DeletionPolicy" : "Retain",
      "Type": "AWS::S3::Bucket",
      "Properties": {
      }
    },
    "BucketPolicy" : {
      "Type" : "AWS::S3::BucketPolicy",
      "Properties" : {
        "Bucket" : {"Ref" : "S3Bucket"},
        "PolicyDocument" : {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Sid": "AWSCloudTrailAclCheck",
              "Effect": "Allow",
              "Principal": { "Service":"cloudtrail.amazonaws.com"},
              "Action": "s3:GetBucketAcl",
              "Resource": { "Fn::Join" : ["", ["arn:aws:s3:::", {"Ref":"S3Bucket"}]]}
            },
            {
              "Sid": "AWSCloudTrailWrite",
              "Effect": "Allow",
              "Principal": { "Service":"cloudtrail.amazonaws.com"},
              "Action": "s3:PutObject",
              "Resource": { "Fn::Join" : ["", ["arn:aws:s3:::", {"Ref":"S3Bucket"}, "/AWSLogs/", {"Ref":"AWS::AccountId"}, "/*"]]},
              "Condition": {
                "StringEquals": {
                  "s3:x-amz-acl": "bucket-owner-full-control"
                }
              }
            }
          ]
        }
      }
    },
    "Topic": {
      "Type": "AWS::SNS::Topic",
      "Properties": {
        "Subscription": [ {
          "Endpoint": { "Ref": "OperatorEmail" },
          "Protocol": "email" } ]
      }
    },
    "TopicPolicy" : {
      "Type" : "AWS::SNS::TopicPolicy",
      "Properties" : {
        "Topics" : [{"Ref":"Topic"}],
        "PolicyDocument" : {
          "Version": "2008-10-17",
          "Statement": [
            {
              "Sid": "AWSCloudTrailSNSPolicy",
              "Effect": "Allow",
              "Principal": { "Service":"cloudtrail.amazonaws.com"},
              "Resource": "*",
              "Action": "SNS:Publish"
            }
          ]
        }
      }
    },
    "myTrail" : {
      "DependsOn" : ["BucketPolicy", "TopicPolicy"],
      "Type" : "AWS::CloudTrail::Trail",
      "Properties" : {
        "S3BucketName" : {"Ref":"S3Bucket"},
        "SnsTopicName" : {"Fn::GetAtt":["Topic","TopicName"]},
        "IsLogging" : true
      }
    }
  }
}
```

### YAML<a name="aws-resource-cloudtrail-trail-example.yaml"></a>

```
  AWSTemplateFormatVersion: "2010-09-09"
  Parameters: 
    OperatorEmail: 
      Description: "Email address to notify when new logs are published."
      Type: String
  Resources: 
    S3Bucket: 
      DeletionPolicy: Retain
      Type: "AWS::S3::Bucket"
      Properties: {}
    BucketPolicy: 
      Type: "AWS::S3::BucketPolicy"
      Properties: 
        Bucket: 
          Ref: S3Bucket
        PolicyDocument: 
          Version: "2012-10-17"
          Statement: 
            - 
              Sid: "AWSCloudTrailAclCheck"
              Effect: "Allow"
              Principal: 
                Service: "cloudtrail.amazonaws.com"
              Action: "s3:GetBucketAcl"
              Resource: 
                !Sub |-
                  arn:aws:s3:::${S3Bucket}
            - 
              Sid: "AWSCloudTrailWrite"
              Effect: "Allow"
              Principal: 
                Service: "cloudtrail.amazonaws.com"
              Action: "s3:PutObject"
              Resource:
                !Sub |-
                  arn:aws:s3:::${S3Bucket}/AWSLogs/${AWS::AccountId}/*
              Condition: 
                StringEquals:
                  s3:x-amz-acl: "bucket-owner-full-control"
    Topic: 
      Type: "AWS::SNS::Topic"
      Properties: 
        Subscription: 
          - 
            Endpoint: 
              Ref: OperatorEmail
            Protocol: email
    TopicPolicy: 
      Type: "AWS::SNS::TopicPolicy"
      Properties: 
        Topics: 
          - Ref: "Topic"
        PolicyDocument: 
          Version: "2008-10-17"
          Statement: 
            - 
              Sid: "AWSCloudTrailSNSPolicy"
              Effect: "Allow"
              Principal: 
                Service: "cloudtrail.amazonaws.com"
              Resource: "*"
              Action: "SNS:Publish"
    myTrail: 
      DependsOn: 
        - BucketPolicy
        - TopicPolicy
      Type: "AWS::CloudTrail::Trail"
      Properties: 
        S3BucketName: 
          Ref: S3Bucket
        SnsTopicName: 
          Fn::GetAtt: 
            - Topic
            - TopicName
        IsLogging: true
```