This AWS WAF (Web Application Firewall) rule configuration allows requests with large body sizes to pass through. It is designed to handle requests where the URI path starts with a specific string associated with an API Gateway endpoint.
Rule Details
Name: AllowLargeBodySizeRule
Priority: 0
Action: Allow
VisibilityConfig:
SampledRequestsEnabled: true
CloudWatchMetricsEnabled: true
MetricName: AllowLargeBodySize
Statement Details
ByteMatchStatement:
FieldToMatch:
UriPath
PositionalConstraint: STARTS_WITH
SearchString: //name of API Gateway endpoint
TextTransformations:
Type: NONE
Priority: 0
