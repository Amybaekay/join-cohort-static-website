# Identified Risks and Mitigation Strategies

## Overview

This document identifies the various security risks involved in deploying and reviewing of Join-Cohort-static website Amazon S3, CloudFront, and Route 53.


# Risk 1 — Public Exposure of S3 Bucket

## Description

The S3 bucket hosting the static website required public access configuration to allow website content delivery.

## Potential Impact

- Unauthorized public access to bucket contents
- Accidental exposure of sensitive files
- Increased attack surface

## Likelihood

Medium

## Mitigation Strategy

- Restrict access through CloudFront where possible
- Apply least privilege bucket policies
- Avoid storing sensitive data in publicly accessible buckets
- Enable monitoring and logging

# Risk 2 — Missing Web Application Firewall (WAF)

## Description

The architecture did not initially include AWS WAF protection.

## Potential Impact

- Increased exposure to web-based attacks
- Potential malicious traffic reaching the application

## Likelihood

Medium

## Mitigation Strategy

- Implement AWS WAF
- Configure managed security rules
- Monitor suspicious requests


# Risk 3 — Lack of CloudTrail Logging

## Description

CloudTrail logging was not initially configured for monitoring API and account activity.

## Potential Impact

- Reduced visibility into security events
- Difficulty investigating incidents

## Likelihood

High

## Mitigation Strategy

- Enable AWS CloudTrail
- Monitor logs regularly
- Integrate logging with security monitoring solutions


# Risk 4 — Excessive IAM Permissions

## Description

Excessive IAM permissions may increase security risk.

## Potential Impact

-  Unauthorized actions
-  Increased impact in the event of credential compromise

## Likelihood

Low to Medium

## Mitigation Strategy

- Apply least privilege access
- Regularly review IAM permissions
- Use role-based access controls


# Conclusion
This project provided hands-on experience in cloud security practices, risk identification, mitigation planning, and governance-oriented documentation within AWS environments.

