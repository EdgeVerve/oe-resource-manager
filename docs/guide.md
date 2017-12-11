# OE Resource Manager

The `oe-resource-manager` component is a plugin to `oe-studio` and helps managing client side resources(html, css etc.)

## Navigating to Resource Manager and adding a new file

To navigate to resource manager, first Go to [oe-designer](http://localhost:3000/designer) and click on the Resource Manager icon as marked in the below image:

![Start Page][start-page]

you will be navigated to Resource Manager, now to add new resource or file, click on `NEW` button.

![Resource Manager][resource-manager-home]

A dialogue box will appear to select and upload file and to add scope. Upload the file by clicking on `Choose or drop files` or drop the file there.

![Upload File][upload-file]

Update the file name and add scope ***if needed***, and save. To understand more about scope or personalisation, click [here](/guide/datapersonalization)

The file data will get posted in UIResources Model. 

![Upload File Config][upload-file-config]

After save the file name will appear in left panel, you can click on that to see the content of file.

![Open File][open-file]

If You want to re-upload file or download file, use the buttons in top right corner as shown below.

![Re-Upload Download][reupload-download]

## How to use uploaded file

In application, Uploaded file can be made available by making a api request to `/api/UIResources/content/<file-name>` path.

Eg.

```<link rel="import" href="/api/UIResources/content/app-theme.html">``` 

Rather than a relative path like _href="../style/app-theme.html"_ .This change, calls the api UIResources,to fetch the appropriate file data from server for the specific user/scope.

[start-page]:  images/designer-home.PNG "Start Page"
[resource-manager-home]: images/resource-manager-home.PNG "Resource Manager"
[upload-file]:images/upload-file.PNG "Upload File"
[upload-file-config]:images/upload-file-config.PNG "Upload File Config"
[open-file]:images/open-file.PNG "Open File"
[reupload-download]:images/reupload-download.PNG "Re-Upload Download"
