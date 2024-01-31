# aws-service-uptimes-cfn
This application retrieves the uptime of AWS services within a given time range. It is invoked via a POST API endpoint. The input parameters are a start date, end date, and a list of AWS regions.

- The API triggers a Lambda function which calls the AWS Health API to calculate service uptime in seconds based on any public service events occurring in the specified regions or globally during the input time range.
* To deploy the application, create a new CloudFormation stack using the template.yaml file.
+ To invoke the application, call the 'aws-service-uptime' endpoint of the API output from the CloudFormation stack. This is a POST endpoint requiring the following parameters:
  - "eventDateFrom" - Start date to calculate service uptime
  * "eventDateTo" - End date to calculate service uptime
  + "regions" - Comma-separated list of AWS regions to calculate service uptime

![image](https://github.com/anshumch/aws-service-uptimes-cfn/assets/100800132/52f88926-ac8d-4312-bc5c-9d6df75f66ad)

**Disclaimer: This does not reflect any SLA commitments, as SLAs incorporate additional factors beyond service uptime. This application provides service uptime illustrations for the given time period and AWS regions.**
