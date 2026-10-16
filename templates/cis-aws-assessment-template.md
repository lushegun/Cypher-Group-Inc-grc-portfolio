[← Portfolio home](../README.md) · [All templates](README.md)

# [ORGANISATION] — Cloud configuration review against the CIS AWS Foundations Benchmark v5.0.0 — TEMPLATE

> [!TIP]
> **How to use this template.** Blank reusable template from the CGI-AWS-001 portfolio project (simulated). All 63
> v5.0.0 recommendations are pre-filled with their profile level, CIS assessment status, AWS Security Hub control ID
> and the audit command a reviewer would run. Replace every `[BRACKETED]` field. Recommendation titles are CIS's own;
> obtain the benchmark from the Center for Internet Security for the full audit and remediation procedures.

| Field | Value |
|---|---|
| Document ID | [ORG-CLD-001] |
| Benchmark version | CIS AWS Foundations Benchmark v5.0.0 |
| Accounts and regions in scope | [LIST] |
| Review date / fieldwork | [DD Mon YYYY] / [DATES] |
| Reviewer | [NAME, ROLE] |
| Approver | [NAME, ROLE] |

## Before you start: four decisions to write down

1. **Version.** Use the version your tooling automates, and say so. Schedule the re-baseline to the newest release.
2. **Profile.** Level 1 for everyone, plus every Level 2 recommendation that a policy, a contract or a provider CUEC makes mandatory. List them with the reason.
3. **Scoring.** Score = PASS ÷ (in scope − N/A). N/A is never a pass. Publish the rule before you record a result.
4. **Gate.** Decide in advance what blocks a claim of alignment (for example: any open Critical or High finding).

## Three rules that stop the usual mistakes

- **Tool IDs are not CIS IDs.** `IAM.9` is a Security Hub control; `1.4` is the recommendation. Record both. About four in ten recommendations have no Security Hub control at all; test those by command line or by hand.
- **A PASS is one setting on one day.** It is not evidence that a control operates over time. Say what period your evidence covers.
- **CIS cannot see your policy.** A CIS PASS on MFA can still be a policy FAIL if your policy demands phishing-resistant factors. Check your own rules alongside the benchmark.

## The assessment

| CIS ID | Recommendation | Level | Status | Security Hub | In profile | Result | Observation and evidence | Audit command or console path | Finding |
|---|---|---|---|---|---|---|---|---|---|
| 1.1 | Maintain current contact details | L1 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | Console: Account > Contact information | [CF-NN] |
| 1.2 | Ensure security contact information is registered | L1 | Manual | Account.1 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws account get-alternate-contact --alternate-contact-type SECURITY | [CF-NN] |
| 1.3 | Ensure no 'root' user account access key exists | L1 | Automated | IAM.4 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws iam get-account-summary  (AccountAccessKeysPresent = 0) | [CF-NN] |
| 1.4 | Ensure MFA is enabled for the 'root' user account | L1 | Automated | IAM.9 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws iam get-account-summary  (AccountMFAEnabled = 1) | [CF-NN] |
| 1.5 | Ensure hardware MFA is enabled for the 'root' user account | L2 | Manual | IAM.6 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws iam list-virtual-mfa-devices  (root serial listed = virtual, not hardware) | [CF-NN] |
| 1.6 | Eliminate use of the 'root' user for administrative and daily tasks | L1 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws iam get-credential-report; CloudTrail lookup-events for ConsoleLogin by Root | [CF-NN] |
| 1.7 | Ensure IAM password policy requires minimum length of 14 or greater | L1 | Automated | IAM.15 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws iam get-account-password-policy  (MinimumPasswordLength) | [CF-NN] |
| 1.8 | Ensure IAM password policy prevents password reuse | L1 | Automated | IAM.16 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws iam get-account-password-policy  (PasswordReusePrevention) | [CF-NN] |
| 1.9 | Ensure MFA is enabled for all IAM users that have a console password | L1 | Automated | IAM.5 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws iam get-credential-report  (password_enabled = true AND mfa_active = false) | [CF-NN] |
| 1.10 | Do not create access keys during initial setup for IAM users with a console password | L1 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws iam get-credential-report | [CF-NN] |
| 1.11 | Ensure credentials unused for 45 days or more are disabled | L1 | Automated | IAM.22 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws iam get-credential-report  (password_last_used, access_key_1_last_used_date) | [CF-NN] |
| 1.12 | Ensure there is only one active access key for any single IAM user | L1 | Automated | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws iam list-access-keys --user-name <user> | [CF-NN] |
| 1.13 | Ensure access keys are rotated every 90 days or less | L1 | Automated | IAM.3 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws iam get-credential-report  (access_key_1_last_rotated) | [CF-NN] |
| 1.14 | Ensure IAM users receive permissions only through groups | L1 | Automated | IAM.2 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws iam list-attached-user-policies; aws iam list-user-policies | [CF-NN] |
| 1.15 | Ensure IAM policies that allow full '*:*' administrative privileges are not attached | L1 | Automated | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws iam list-policies --only-attached --scope Local; aws iam get-policy-version | [CF-NN] |
| 1.16 | Ensure a support role has been created to manage incidents with AWS Support | L1 | Automated | IAM.18 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws iam list-entities-for-policy --policy-arn arn:aws:iam::aws:policy/AWSSupportAccess | [CF-NN] |
| 1.17 | Ensure IAM instance roles are used for AWS resource access from instances | L2 | Automated | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws ec2 describe-instances --query Reservations[].Instances[].IamInstanceProfile | [CF-NN] |
| 1.18 | Ensure that all expired SSL/TLS certificates stored in AWS IAM are removed | L1 | Automated | IAM.26 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws iam list-server-certificates | [CF-NN] |
| 1.19 | Ensure that IAM External Access Analyzer is enabled for all regions | L1 | Automated | IAM.28 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws accessanalyzer list-analyzers  (per region) | [CF-NN] |
| 1.20 | Ensure IAM users are managed centrally via identity federation or AWS Organizations for multi-account environments | L2 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws sso-admin list-instances; aws iam list-saml-providers | [CF-NN] |
| 1.21 | Ensure access to AWSCloudShellFullAccess is restricted | L1 | Manual | IAM.27 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws iam list-entities-for-policy --policy-arn arn:aws:iam::aws:policy/AWSCloudShellFullAccess | [CF-NN] |
| 2.1.1 | Ensure S3 Bucket Policy is set to deny HTTP requests | L2 | Automated | S3.5 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws s3api get-bucket-policy --bucket <bucket> | [CF-NN] |
| 2.1.2 | Ensure MFA Delete is enabled on S3 buckets | L2 | Manual | S3.20 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws s3api get-bucket-versioning --bucket <bucket>  (MFADelete) | [CF-NN] |
| 2.1.3 | Ensure all data in Amazon S3 has been discovered, classified, and secured when necessary | L2 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws macie2 get-macie-session; aws s3api list-objects-v2 | [CF-NN] |
| 2.1.4 | Ensure that S3 is configured with 'Block Public Access' enabled | L1 | Automated | S3.1 (account); S3.8 (bucket) | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws s3control get-public-access-block --account-id <id>; aws s3api get-public-access-block --bucket <bucket> | [CF-NN] |
| 2.2.1 | Ensure that encryption-at-rest is enabled for RDS instances | L1 | Automated | RDS.3 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws rds describe-db-instances  (StorageEncrypted = true, KmsKeyId) | [CF-NN] |
| 2.2.2 | Ensure the Auto Minor Version Upgrade feature is enabled for RDS instances | L1 | Automated | RDS.13 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws rds describe-db-instances  (AutoMinorVersionUpgrade) | [CF-NN] |
| 2.2.3 | Ensure that RDS instances are not publicly accessible | L1 | Automated | RDS.2 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws rds describe-db-instances  (PubliclyAccessible = false) | [CF-NN] |
| 2.2.4 | Ensure Multi-AZ deployments are used for enhanced availability in Amazon RDS | L1 | Manual | RDS.5; RDS.15 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws rds describe-db-instances  (MultiAZ = true) | [CF-NN] |
| 2.3.1 | Ensure that encryption is enabled for EFS file systems | L1 | Automated | EFS.1; EFS.8 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws efs describe-file-systems | [CF-NN] |
| 3.1 | Ensure CloudTrail is enabled in all regions | L1 | Manual | CloudTrail.1 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws cloudtrail describe-trails; aws cloudtrail get-trail-status; aws cloudtrail get-event-selectors | [CF-NN] |
| 3.2 | Ensure CloudTrail log file validation is enabled | L2 | Automated | CloudTrail.4 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws cloudtrail describe-trails  (LogFileValidationEnabled) | [CF-NN] |
| 3.3 | Ensure AWS Config is enabled in all regions | L2 | Automated | Config.1 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws configservice describe-configuration-recorder-status  (per region) | [CF-NN] |
| 3.4 | Ensure that server access logging is enabled on the CloudTrail S3 bucket | L1 | Manual | CloudTrail.7 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws s3api get-bucket-logging --bucket cgi-prod-cloudtrail-logs | [CF-NN] |
| 3.5 | Ensure CloudTrail logs are encrypted at rest using KMS CMKs | L2 | Automated | CloudTrail.2 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws cloudtrail describe-trails  (KmsKeyId absent) | [CF-NN] |
| 3.6 | Ensure rotation for customer-created symmetric CMKs is enabled | L2 | Automated | KMS.4 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws kms list-keys; aws kms get-key-rotation-status --key-id <id> | [CF-NN] |
| 3.7 | Ensure VPC flow logging is enabled in all VPCs | L2 | Automated | EC2.6 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws ec2 describe-flow-logs | [CF-NN] |
| 3.8 | Ensure that object-level logging for write events is enabled for S3 buckets | L2 | Automated | S3.22 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws cloudtrail get-event-selectors --trail-name cgi-prod-trail | [CF-NN] |
| 3.9 | Ensure that object-level logging for read events is enabled for S3 buckets | L2 | Automated | S3.23 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws cloudtrail get-event-selectors --trail-name cgi-prod-trail | [CF-NN] |
| 4.1 | Ensure unauthorized API calls are monitored | L2 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws logs describe-metric-filters; aws cloudwatch describe-alarms; aws events list-rules | [CF-NN] |
| 4.2 | Ensure management console sign-in without MFA is monitored | L1 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws logs describe-metric-filters; aws cloudwatch describe-alarms; aws events list-rules | [CF-NN] |
| 4.3 | Ensure usage of the 'root' account is monitored | L1 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws logs describe-metric-filters; aws cloudwatch describe-alarms; aws events list-rules | [CF-NN] |
| 4.4 | Ensure IAM policy changes are monitored | L1 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws logs describe-metric-filters; aws cloudwatch describe-alarms; aws events list-rules | [CF-NN] |
| 4.5 | Ensure CloudTrail configuration changes are monitored | L1 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws logs describe-metric-filters; aws cloudwatch describe-alarms; aws events list-rules | [CF-NN] |
| 4.6 | Ensure AWS Management Console authentication failures are monitored | L2 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws logs describe-metric-filters; aws cloudwatch describe-alarms; aws events list-rules | [CF-NN] |
| 4.7 | Ensure disabling or scheduled deletion of customer created CMKs is monitored | L2 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws logs describe-metric-filters; aws cloudwatch describe-alarms; aws events list-rules | [CF-NN] |
| 4.8 | Ensure S3 bucket policy changes are monitored | L1 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws logs describe-metric-filters; aws cloudwatch describe-alarms; aws events list-rules | [CF-NN] |
| 4.9 | Ensure AWS Config configuration changes are monitored | L2 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws logs describe-metric-filters; aws cloudwatch describe-alarms; aws events list-rules | [CF-NN] |
| 4.10 | Ensure security group changes are monitored | L2 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws logs describe-metric-filters; aws cloudwatch describe-alarms; aws events list-rules | [CF-NN] |
| 4.11 | Ensure Network Access Control List (NACL) changes are monitored | L2 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws logs describe-metric-filters; aws cloudwatch describe-alarms; aws events list-rules | [CF-NN] |
| 4.12 | Ensure changes to network gateways are monitored | L1 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws logs describe-metric-filters; aws cloudwatch describe-alarms; aws events list-rules | [CF-NN] |
| 4.13 | Ensure route table changes are monitored | L1 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws logs describe-metric-filters; aws cloudwatch describe-alarms; aws events list-rules | [CF-NN] |
| 4.14 | Ensure VPC changes are monitored | L1 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws logs describe-metric-filters; aws cloudwatch describe-alarms; aws events list-rules | [CF-NN] |
| 4.15 | Ensure AWS Organizations changes are monitored | L1 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws logs describe-metric-filters; aws cloudwatch describe-alarms; aws events list-rules | [CF-NN] |
| 4.16 | Ensure AWS Security Hub is enabled | L2 | Automated | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws securityhub describe-hub | [CF-NN] |
| 5.1.1 | Ensure EBS volume encryption is enabled in all regions | L1 | Automated | EC2.7 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws ec2 get-ebs-encryption-by-default  (per region) | [CF-NN] |
| 5.1.2 | Ensure CIFS access is restricted to trusted networks to prevent unauthorized access | L1 | Automated | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws ec2 describe-security-groups --filters Name=ip-permission.from-port,Values=445 | [CF-NN] |
| 5.2 | Ensure no Network ACLs allow ingress from 0.0.0.0/0 to remote server administration ports | L1 | Automated | EC2.21 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws ec2 describe-network-acls | [CF-NN] |
| 5.3 | Ensure no security groups allow ingress from 0.0.0.0/0 to remote server administration ports | L1 | Automated | EC2.53 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws ec2 describe-security-groups --group-ids <sg-bastion> | [CF-NN] |
| 5.4 | Ensure no security groups allow ingress from ::/0 to remote server administration ports | L1 | Automated | EC2.54 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws ec2 describe-security-groups | [CF-NN] |
| 5.5 | Ensure the default security group of every VPC restricts all traffic | L2 | Automated | EC2.2 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws ec2 describe-security-groups --filters Name=group-name,Values=default | [CF-NN] |
| 5.6 | Ensure routing tables for VPC peering are 'least access' | L2 | Manual | - | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws ec2 describe-vpc-peering-connections; aws ec2 describe-route-tables | [CF-NN] |
| 5.7 | Ensure that the EC2 Metadata Service only allows IMDSv2 | L1 | Automated | EC2.8 | [Y/N] | [PASS / FAIL / N/A] | [OBSERVATION · EVIDENCE] | aws ec2 describe-instances  (MetadataOptions.HttpTokens) | [CF-NN] |

## Scorecard

| Measure | Result |
|---|---|
| PASS · FAIL · N/A | [n] · [n] · [n] |
| Score, all applicable | [PASS ÷ applicable] |
| Score, Level 1 | [ ] |
| **Score, your profile** | [ ] |
| Open findings by severity | [Critical · High · Medium · Low] |
| Claim alignment? | [GO / NO-GO by your gate] |

## Fill-in checklist

- [ ] Version, profile, scoring rule and gate written down before the first result
- [ ] Every row has a result, and every FAIL cites a finding
- [ ] Every result names its evidence and the period it covers
- [ ] Manual recommendations say who was asked; inquiry alone is labelled as weak evidence
- [ ] N/A rows say why (and are not counted as passes)
- [ ] Provider CUECs tested against the rows that evidence them

<sub>Free to use and adapt with attribution. Provided as-is, without warranty.</sub>
