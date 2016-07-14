# FTPUpload.cs

<script type="text/javascript" src="../js/general.js"></script>

### API description
---

* constructor (建構子)

```
/*
 * parameter
 * 1. getFTPuser : ftp user name
 * 2. getFTPPwd : user password
 * 3. getFTPFullUpdPath : upload file path on ftp server
 * 4. getFTPFullLocalPath : local file for upload
 * 5. getDataString : string data type for upload
 * 6. getCSFlag : do checksum flag
 * 7. getReTryCount : count of retrying to upload
 * 8. getUploadFromFile : the data content is from file or from string
 */

public FTPUpload(
  String getFTPuser, 
  String getFTPPwd, 
  String getFTPFullUpdPath, 
  String getFTPFullLocalPath
)

public FTPUpload(
  String getFTPuser, 
  String getFTPPwd, 
  String getFTPFullUpdPath, 
  String getFTPFullLocalPath, 
  bool getCSFlag
)

public FTPUpload(
  String getFTPuser, 
  String getFTPPwd, 
  String getFTPFullUpdPath, 
  String getFTPFullLocalPath, 
  int getReTryCount, 
  bool getCSFlag
)

public FTPUpload(
  String getFTPuser, 
  String getFTPPwd, 
  String getFTPFullUpdPath, 
  String getDataString, 
  int getReTryCount, 
  bool getUploadFromFile, 
  bool getCSFlag
)
```

### API Example
---

