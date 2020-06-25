# Changelog

## 1.0.187 (6/24/20)

### New Features:
- **McAfee ePolicy Orchestrator 5.10.0 Update 7 (2.0.0.907)**
    * This includes new images with [Update 7](https://docs.mcafee.com/bundle/epolicy-orchestrator-5.10.0-release-notes/page/GUID-91E47324-1642-4EE6-8776-3230C0EA38F8.html) for both ePO and Agent Handlers. Update 7 is cumulative in nature and includes fixes from Update 1.
- **Support for FIPS**
    * The deployment allows to choose FIPS mode which runs ePO and Agent Handler images in FIPS compliant mode
- **Custom Agent Handler HTTP Port**
    * You can configure Agent Handler HTTP port as part of deployment input parameter
- **New updated packages, extensions and bundle**
    * AH version: 5.10.0.3194
    * MA extension: 5.6.5.102
    * MA Package: 5.6.5.236
    * Support Center: 5.10.0.426

## 1.0.180 (1/21/2019)

### New Features:

- **ePO AMI is pre-installed with CU6 (2.0.0.831)**
    * New deployments will come with ePO CU6
    * Previous AWS QS deployments will have to deploy CU6 manually as auto-update of ePO AMI is not currently supported

- **AH AMI with CU6**
    * New AH AMI includes CU6 installed on top of Agent Handler RTW 5.10.0.2428 version compared to previous AMI released version for CU4.

- **New DXL AMI with Broker 6.0.0**
    * This AMI includes DXL broker 6.0.0.197

- **Update MA with the latest 5.6.3**
    * ePO will includes the latest MA 5.6.3 extension and MA client packages

- **Support for private network deployment**
    * Introduced new template "mcafee-epo-private.template" which will deploy in private only network.
    * This means there will be no publicly exposed subnets, load balancers and Route53 hosted zone records created part of this deployment when used this private template.

### Bug Fixes:

- Update Lambda Nodejs runtime

## 1.0.168 (8/27/2019)

### New Features:

- **McAfee ePolicy Orchestrator 5.10.0 Update 4**
    * New image (AMI) available for Agent Handler with Update 4  . This update resolves known issues from McAfee ePO 5.10.0 release. Update 4 is cumulative in nature and includes fixes from Update 1.
    * AH version: 5.10.0.2727 #5

- **McAfee Agent 5.6.1 with integrated McAfee® Data Exchange Layer 5.0.1 (DXL)**
    * McAfee Agent 5.6.1 bundles the McAfee Data Exchange Layer client 5.0.1 as a component. The Data Exchange Layer client is automatically installed on managed systems and connects to a DXL broker in your environment.
    * MA Version: 5.6.1.308
    * DXL Broker: 5.0.1.198

- **Bundled with latest McAfee ePolicy Orchestrator (ePO) Support Center 5.10.0**
    * Updated to Support Center: 5.10.0.398

### Bug Fixes:

- HEPOAWS-11: Remove Private Hosted Zone record sets and outputs from base template



## 1.0.156 (5/24/19)

### Bug Fixes:

- Update Lambda Nodejs runtime to 8.10

## 1.0.155 (4/9/2019)

### Bug Fixes:

- Enabled DNS fallback to support hybrid DNS

## 1.0.154 (3/21/2019)

### New Features:
- **McAfee ePolicy Orchestrator 5.10.0 Update 3**\
     New image (AMI) available for Agent Handler with Update 3 . This update resolves known issues from McAfee ePO 5.10.0 release. Update 3 is cumulative in nature and includes fixes from Update 1.

### Bug Fixes:
- Please refer the Update 3 release notes for complete list of bug fixes:

  https://kc.mcafee.com/resources/sites/MCAFEE/content/live/PRODUCT_DOCUMENTATION/28000/PD28210/en_US/March12_EPO_5_10_Update3_RN.PDF


## 1.0.151 (3/1/2019)

### New Features:
- **Additional AWS Regions Support**\
    Now, you can deploy and configure McAfee ePolicy Orchestrator end to end deployment in the following regions:
    * Europe (Paris)
    * AWS Govcloud (US) East

-	**McAfee Agent 5.6.0 with integrated McAfee® Data Exchange Layer 5.0.1 (DXL)**
    * McAfee Agent 5.6.0 bundles the McAfee Data Exchange Layer client 5.0.1 as a component. The Data Exchange Layer client is automatically installed on managed systems and connects to a DXL broker in your environment.

-	**Bundled with McAfee ePolicy Orchestrator (ePO) Support Center 5.10.0**
    Support Center is a lightweight ePO extension that includes the following capabilities:
    * Insight into the health of ePO platform elements.
    *	Ability to receive and tag SNS notifications from within the console.
    *	Access to ‘How to’ resources and best practices for ePO and Endpoint Security through the Product Information pages.
    *	Search capability across McAfee content repositories.
    *	New Stack Parameter for Product Improvement Program
    *	You can configure through AWS Cloud Formation Template stack parameter to enable or disable McAfee Product Improvement Program which collects data from the client systems where McAfee products are installed and managed by ePO.

### Bug Fixes:
-	Retry mechanism to avoid Software Manager connectivity issues
-	Increased time delay to avoid stack failures due to increased RDS provisioning time
-	CI changes to accommodate Support Center artifacts
