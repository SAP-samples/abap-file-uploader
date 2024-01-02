# ABAP File Uploader

[![REUSE status](https://api.reuse.software/badge/github.com/SAP-samples/abap-file-uploader)](https://api.reuse.software/info/github.com/SAP-samples/abap-file-uploader)

## Description

The ABAP File Uploader is designed to allow an ABAP developer to upload data from a file directly into a target database table in SAP Business Technology Platform ABAP Environment instance. This utility expects a json file for the uploaded data with attributes that match the column names in the database table. 

Video Introduction here: [https://youtu.be/PpXNP3ciGOc](https://youtu.be/PpXNP3ciGOc)

## Requirements

Make sure to fulfill the following requirements:

* You have access to an SAP Business Technology Platform ABAP Environment instance (see [here](https://blogs.sap.com/2018/09/04/sap-cloud-platform-abap-environment) for additional information).
* Note: The XCO APIs are available automatically in trial systems and require no further steps. In productive accounts: "The XCO library is currently only available via feature toggle. If you are interested in using this new feature, please contact SAP." https://help.sap.com/doc/43b304f99a8145809c78f292bfc0bc58/Cloud/en-US/98bf747111574187a7c76f8ced51cfeb.html
For more general information on XCO:
https://blogs.sap.com/2020/05/17/the-rap-generator
* You have downloaded and installed ABAP Development Tools (ADT). Make sure to use the most recent version as indicated on the [installation page](https://tools.hana.ondemand.com/#abap).
* You have created an ABAP Cloud Project in ADT that allows you to access your SAP Business Technology Platform ABAP Environment instance (see [here](https://help.sap.com/viewer/5371047f1273405bb46725a417f95433/Cloud/en-US/99cc54393e4c4e77a5b7f05567d4d14c.html) for additional information). Your log-on language is English.
* You have installed the [abapGit](https://github.com/abapGit/eclipse.abapgit.org) plug-in for ADT from the update site `http://eclipse.abapgit.org/updatesite/`.

## Download and Installation

Use the abapGit plug-in to install the ABAP File Uploader Examples by executing the following steps:

1. In your ABAP cloud project, create an ABAP package for the demo content to be downloaded (leave the suggested values unchanged when following the steps in the package creation wizard).
2. To add the <em>abapGit Repositories</em> view to the <em>ABAP</em> perspective, click `Window` > `Show View` > `Other...` from the menu bar and choose `abapGit Repositories`.
3. In the <em>abapGit Repositories</em> view, click the `+` icon to clone an abapGit repository.
4. Enter the following URL of this repository: `https://github.com/SAP-samples/abap-file-uploader` and choose <em>Next</em>.
5. Create a new transport request that you only use for this demo content installation (recommendation) and choose <em>Finish</em> to link the Git repository to your ABAP cloud project. The repository appears in the abapGit Repositories View with status <em>Linked</em>.
6. Right-click on the new ABAP repository and choose `pull` to start the cloning of the repository contents. Note that this procedure may take a few minutes. 
7. Once the cloning has finished, the status is set to `Pulled Successfully`. Then refresh your project tree.

As a result of the installation procedure above, the ABAP system creates an inactive version of all artifacts from the demo content

To activate all development objects from this sample:

1. Click the mass-activation icon (<em>Activate Inactive ABAP Development Objects</em>) in the toolbar.  
2. In the dialog that appears, select all development objects in the transport request (that you created for the demo content installation) and choose <em>Activate</em>.
3. Once the imported handler class is activated, you must then manually create an HTTP Service and attach this handler class to the service.  Again, make sure the handler class is activated first!!  Then in ADT, right-click on your package and choose `New` > `Other ABAP Repository Object`.
<br>![1](/images/1.png)
4. In the dialog, click Connectivity, then choose <em>HTTP Service</em>.  Click <em>Next</em>.
<br>![2](/images/2.png)
5. Give the name of the HTTP Service as ZABAP_FILE_UPLOADER, the Handler Class should prepopulate with the correct name. Click <em>Next</em>, then <em>Finish</em>.
<br>![3](/images/3.png)
6. After a couple minutes, the HTTP Service should be ready(Until all underlying objects are generated you could possiblly get a 403 error when launching the application).  Click on the URL link in the service to launch the tool.
<br>![4](/images/4.png)

## Known Issues

## How to obtain support

This project is provided "as-is": there is no guarantee that raised issues will be answered or addressed in future releases.

## License

Copyright (c) 2024 SAP SE or an SAP affiliate company. All rights reserved. 
This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
