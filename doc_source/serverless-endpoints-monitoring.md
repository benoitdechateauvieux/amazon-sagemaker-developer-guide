# Monitor a Serverless Endpoint<a name="serverless-endpoints-monitoring"></a>


****  

|  | 
| --- |
| Serverless Inference is in preview release for Amazon SageMaker and is subject to change\. We do not recommend using this feature in production environments\. | 

To monitor your serverless endpoint, you can use Amazon CloudWatch alarms\. CloudWatch is a service that collects metrics in real time from your AWS applications and resources\. An alarm watches metrics as they are collected and gives you the ability to pre\-specify a threshold and the actions to take if that threshold is breached\. For example, your CloudWatch alarm can send you a notification if your endpoint breaches an error threshold\. By setting up CloudWatch alarms, you gain visibility into the performance and functionality of your endpoint\.

To learn more about CloudWatch metrics you can use to monitor your endpoints in SageMaker, see [SageMaker Endpoint Invocation Metrics](monitoring-cloudwatch.md#cloudwatch-metrics-endpoint-invocation)\. The new `ModelSetupTime` metric tracks the time it takes to launch new compute resources for your serverless endpoint\. Serverless endpoints can also use the `Invocations4XXErrors`, `Invocations5XXErrors`, and `Invocations` metrics in the `AWS/SageMaker` namespace\. In the `aws/sagemaker/Endpoints` namespace, they can use the `MemoryUtilization` metric\. For more information about CloudWatch alarms, see [Using Amazon CloudWatch alarms](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html) in the *Amazon CloudWatch User Guide*\.

If you want to monitor the logs from your endpoint for debugging or progress analysis, you can use Amazon CloudWatch Logs\. The SageMaker\-provided log group that you can use for serverless endpoints is `/aws/sagemaker/Endpoints/[EndpointName]`\. For more information about using CloudWatch Logs in SageMaker, see [Log Amazon SageMaker Events with Amazon CloudWatch](logging-cloudwatch.md)\. To learn more about CloudWatch Logs, see [What is Amazon CloudWatch Logs?](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html) in the *Amazon CloudWatch Logs User Guide*\.