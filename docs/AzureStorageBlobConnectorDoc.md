## About the connector
Azure Blob storage is a service that contains information for operations on block blobs, append blobs, and page blobs. This connector helps you to perform REST operations for working with blobs in the Blob service.
<p>This document provides information about the Azure Storage Blob Connector, which facilitates automated interactions, with a Azure Storage Blob server using FortiSOAR&trade; playbooks. Add the Azure Storage Blob Connector as a step in FortiSOAR&trade; playbooks and perform automated operations with Azure Storage Blob.</p>

### Version information

Connector Version: 1.0.0


Authored By: spryIQ.co

Certified: No
## Installing the connector
<p>From FortiSOAR&trade; 5.0.0 onwards, use the <strong>Connector Store</strong> to install the connector. For the detailed procedure to install a connector, click <a href="https://docs.fortinet.com/document/fortisoar/0.0.0/installing-a-connector/1/installing-a-connector" target="_top">here</a>.<br>You can also use the following <code>yum</code> command as a root user to install connectors from an SSH session:</p>
`yum install cyops-connector-azure-storage-blob`

## Prerequisites to configuring the connector
- You must have the URL of Azure Storage Blob server to which you will connect and perform automated operations and credentials to access that server.
- The FortiSOAR&trade; server should have outbound connectivity to port 443 on the Azure Storage Blob server.

## Minimum Permissions Required
- N/A

## Configuring the connector
For the procedure to configure a connector, click [here](https://docs.fortinet.com/document/fortisoar/0.0.0/configuring-a-connector/1/configuring-a-connector)
### Configuration parameters
<p>In FortiSOAR&trade;, on the Connectors page, click the <strong>Azure Storage Blob</strong> connector row (if you are in the <strong>Grid</strong> view on the Connectors page) and in the <strong>Configurations&nbsp;</strong> tab enter the required configuration details:&nbsp;</p>
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Storage Account Name<br></td><td>Name of the storage account from which you want to perform the automated operations.<br>
<tr><td>Account SAS Token<br></td><td>Account Shared Access Signature(SAS) to perform automated operations on Storage Table Service.<br>
<tr><td>Container Name<br></td><td>Specify the name of the azure container.<br>
<tr><td>Verify SSL<br></td><td>Specifies whether the SSL certificate for the server is to be verified or not. <br/>By default, this option is set as True.<br></td></tr>
</tbody></table>

## Actions supported by the connector
The following automated operations can be included in playbooks and you can also use the annotations to access operations from FortiSOAR&trade; release 4.10.0 and onwards:
<table border=1><thead><tr><th>Function<br></th><th>Description<br></th><th>Annotation and Category<br></th></tr></thead><tbody><tr><td>Put Blob<br></td><td>The Put Blob operation creates a new block, page, or append blob, or updates the content of an existing block blob.<br></td><td>create_or_update_blob <br/>Investigation<br></td></tr>
<tr><td>List Blob<br></td><td>The List Blobs operation returns a list of the blobs under the specified container.<br></td><td>list_blob <br/>Investigation<br></td></tr>
</tbody></table>

### operation: Put Blob
#### Input parameters
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Blob Name<br></td><td>Specify the name of the blob to create or update.<br>
</td></tr><tr><td>Blob Type<br></td><td>Select the type of the blob to create block blob, page blob and append blob.<br>
</td></tr><tr><td>Blob Data<br></td><td>Specify the content of the blob. For a page blob or an append blob, the content is empty.<br>
</td></tr></tbody></table>

#### Output

 No output schema is available at this time.
### operation: List Blob
#### Input parameters
None.
#### Output

 No output schema is available at this time.
## Included playbooks
The `Sample - azure-storage-blob - 1.0.0` playbook collection comes bundled with the Azure Storage Blob connector. These playbooks contain steps using which you can perform all supported actions. You can see bundled playbooks in the **Automation** > **Playbooks** section in FortiSOAR<sup>TM</sup> after importing the Azure Storage Blob connector.

- List Blob
- Put Blob

**Note**: If you are planning to use any of the sample playbooks in your environment, ensure that you clone those playbooks and move them to a different collection, since the sample playbook collection gets deleted during connector upgrade and delete.
