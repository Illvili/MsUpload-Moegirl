MsUpload
========

What's modified
---------------

修改版添加了图片注释自动添加分类（category:pagename）以及额外的作者名和源地址输入框

自动识别页面标题生成[[分类:页面名]]。

以及两个输入框。

作者，生成 [[分类:作者:输入参数]]。

源地址，生成 源地址:输入内容

举例：

在页面 舰队Collection荒潮 通过MsUploadMoegirlVer上传图片，在作者栏输入コニシ，在原地址栏输入http://www55.xxxxxxxxxxxxx.com

上传图片产生的对应页面输出结果： [[分类:作者:コニシ]] [[分类:舰队Collection荒潮]] 源地址:http://www55.xxxxxxxxxxxxx.com


Installation
------------
To install MsUpload, add the following to your LocalSettings.php:

# If necessary, adjust the global configuration:
$wgEnableWriteAPI = true; // Enable the API
$wgEnableUploads = true; // Enable uploads
$wgFileExtensions = array('png','gif','jpg','jpeg','doc','xls','mpp','pdf','ppt','tiff','bmp','docx', 'xlsx','pptx','ps','odt','ods','odp','odg');
$wgAllowJavaUploads = true; // Solves problem with Office 2007 and newer files (docx, xlsx, etc.)

# Then load the extension and configure it as needed. The values shown below are the defaults, so they may be omitted:
wfLoadExtension( 'MsUpload' );
$wgMSU_useDragDrop = true;
$wgMSU_showAutoCat = true;
$wgMSU_checkAutoCat = true;
$wgMSU_useMsLinks = false;
$wgMSU_confirmReplace = true;
$wgMSU_imgParams = '400px';

Credits
-------
* Developed and coded by Martin Schwindl (wiki@ratin.de)
* Idea, project management and bug fixing by Martin Keyler (wiki@keyler-consult.de)
* Updated, debugged and enhanced by Luis Felipe Schenone (schenonef@gmail.com)
* Some icons by Yusuke Kamiyamane (http://p.yusukekamiyamane.com). All rights reserved. Licensed under a Creative Commons Attribution 3.0 License.
