# DescribeParameters<a name="API_dax_DescribeParameters"></a>

Returns the detailed parameter list for a particular parameter group\.

## Request Syntax<a name="API_dax_DescribeParameters_RequestSyntax"></a>

```
{
   "MaxResults": number,
   "NextToken": "string",
   "ParameterGroupName": "string",
   "Source": "string"
}
```

## Request Parameters<a name="API_dax_DescribeParameters_RequestParameters"></a>

The request accepts the following data in JSON format\.

**Note**  
In the following list, the required parameters are described first\.

 ** ParameterGroupName **   
The name of the parameter group\.  
Type: String  
Required: Yes

 ** MaxResults **   
The maximum number of results to include in the response\. If more results exist than the specified `MaxResults` value, a token is included in the response so that the remaining results can be retrieved\.  
The value for `MaxResults` must be between 20 and 100\.  
Type: Integer  
Required: No

 ** NextToken **   
An optional token returned from a prior request\. Use this token for pagination of results from this action\. If this parameter is specified, the response includes only results beyond the token, up to the value specified by `MaxResults`\.  
Type: String  
Required: No

 ** Source **   
How the parameter is defined\. For example, `system` denotes a system\-defined parameter\.  
Type: String  
Required: No

## Response Syntax<a name="API_dax_DescribeParameters_ResponseSyntax"></a>

```
{
   "NextToken": "string",
   "Parameters": [ 
      { 
         "AllowedValues": "string",
         "ChangeType": "string",
         "DataType": "string",
         "Description": "string",
         "IsModifiable": "string",
         "NodeTypeSpecificValues": [ 
            { 
               "NodeType": "string",
               "Value": "string"
            }
         ],
         "ParameterName": "string",
         "ParameterType": "string",
         "ParameterValue": "string",
         "Source": "string"
      }
   ]
}
```

## Response Elements<a name="API_dax_DescribeParameters_ResponseElements"></a>

If the action is successful, the service sends back an HTTP 200 response\.

The following data is returned in JSON format by the service\.

 ** NextToken **   
Provides an identifier to allow retrieval of paginated results\.  
Type: String

 ** Parameters **   
A list of parameters within a parameter group\. Each element in the list represents one parameter\.  
Type: Array of [Parameter](API_dax_Parameter.md) objects

## Errors<a name="API_dax_DescribeParameters_Errors"></a>

For information about the errors that are common to all actions, see [Common Errors](CommonErrors.md)\.

 **InvalidParameterCombinationException**   
Two or more incompatible parameters were specified\.  
HTTP Status Code: 400

 **InvalidParameterValueException**   
The value for a parameter is invalid\.  
HTTP Status Code: 400

 **ParameterGroupNotFoundFault**   
The specified parameter group does not exist\.  
HTTP Status Code: 400

## See Also<a name="API_dax_DescribeParameters_SeeAlso"></a>

For more information about using this API in one of the language\-specific AWS SDKs, see the following:

+  [AWS Command Line Interface](http://docs.aws.amazon.com/goto/aws-cli/dax-2017-04-19/DescribeParameters) 

+  [AWS SDK for \.NET](http://docs.aws.amazon.com/goto/DotNetSDKV3/dax-2017-04-19/DescribeParameters) 

+  [AWS SDK for C\+\+](http://docs.aws.amazon.com/goto/SdkForCpp/dax-2017-04-19/DescribeParameters) 

+  [AWS SDK for Go](http://docs.aws.amazon.com/goto/SdkForGoV1/dax-2017-04-19/DescribeParameters) 

+  [AWS SDK for Java](http://docs.aws.amazon.com/goto/SdkForJava/dax-2017-04-19/DescribeParameters) 

+  [AWS SDK for JavaScript](http://docs.aws.amazon.com/goto/AWSJavaScriptSDK/dax-2017-04-19/DescribeParameters) 

+  [AWS SDK for PHP V3](http://docs.aws.amazon.com/goto/SdkForPHPV3/dax-2017-04-19/DescribeParameters) 

+  [AWS SDK for Python](http://docs.aws.amazon.com/goto/boto3/dax-2017-04-19/DescribeParameters) 

+  [AWS SDK for Ruby V2](http://docs.aws.amazon.com/goto/SdkForRubyV2/dax-2017-04-19/DescribeParameters) 