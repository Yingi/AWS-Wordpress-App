# STAGE 1

In this stage we will setup the environment which WordPress will run from. And then we will configure ssm parameters

Login to an AWS Account

Login to an AWS account using a user with `admin privileges` or create a new user with `admin privilege` and ensure your region is set to `us-east-1 N. Virginia`

Click https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/quickcreate?stackName=A4LVPC&templateURL=https://kem-labs-stack.s3.amazonaws.com/A4LVPC.yaml

Wait for the STACK to move into the `CREATE_COMPLETE` state before continuing.

Configure some `SSM` Parameters

Storing configuration information within the SSM Parameter store scales much better than attempting to script them in some way. In this sub-section you are going to create parameters to store the important configuration items for the platform you are building.


Open a new tab to https://console.aws.amazon.com/systems-manager/home?region=us-east-1

Click on `Parameter Store` on the menu on the `left`


## `DBUser` Parameter

Create Parameter - `DBUser` (the login for the specific wordpress DB)

Click `Create Parameter` 

Set `Name` to `/A4L/Wordpress/DBUser` 

Set `Description` to `Wordpress Database User`

Set `Tier` to `Standard`

Set `Type` to `String`

Set `Data type` to `text`

Set `Value` to `a4lwordpressuser`

Click `Create parameter`





## `DBName` Parameter
Create Parameter - `DBName` (the name of the wordpress database)

Click `Create Parameter` 

Set `Name` to `/A4L/Wordpress/DBName`

Set `Description` to `Wordpress Database Name`

Set `Tier` to `Standard`

Set `Type` to `String`

Set `Data type` to `text`

Set `Value` to `a4lwordpressdb`

Click `Create parameter`



## `DBEndpoint` Parameter

Create Parameter - `DBEndpoint` (the endpoint for the wordpress DB .. )

Click `Create Parameter`

Set `Name` to `/A4L/Wordpress/DBEndpoint` 

Set `Description` to `Wordpress Endpoint Name`

Set `Tier` to `Standard`

Set `Type` to `String`

Set `Data type` to `text`

Set `Value` to `localhost`

Click `Create parameter`



## `DBPassword` Parameter

Create Parameter - `DBPassword` (the password for the DBUser)

Click `Create Parameter`

Set `Name` to `/A4L/Wordpress/DBPassword` 

Set `Description` to `Wordpress DB Password`

Set `Tier` to `Standard`

Set `Type` to `SecureString`

Set `KMS Key Source` to `My Current Account`

Leave `KMS Key ID` as `default` 

Set `Value` to `4n1m4l54L1f3` 

Click `Create parameter`



## `DBRootPassword` Parameter

Create Parameter - `DBRootPassword` (the password for the database root user, used for self-managed admin)

Click `Create Parameter` 

Set `Name` to `/A4L/Wordpress/DBRootPassword` 

Set `Description` to `Wordpress DBRoot Password`

Set `Tier` to `Standard`

Set `Type` to `SecureString`

Set `KMS Key Source` to `My Current Account`

Leave `KMS Key ID` as `default` 

Set `Value` to `4n1m4l54L1f3` 

Click `Create parameter`
