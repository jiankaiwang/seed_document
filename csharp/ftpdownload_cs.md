# FTPDownload.cs

<script type="text/javascript" src="../js/general.js"></script>

* constructor (建構子)

```csharp
/*
 * parameter
 * 1. getFTPuser : ftp user name
 * 2. getFTPPwd : user password
 * 3. getFTPFullDwnPath : file path on the server, including file name and sub file name
 * 4. getFTPFullLocalPath : download file path on the client, include file name and sub file name
 * 5. getFTPReTryCount : count of retring connecting to server 
 * 6. dwnFileFlag : whether to download as a file
 */

public FTPDownload(
  String getFTPuser, 
  String getFTPPwd, 
  String getFTPFullDwnPath
)
 
public FTPDownload(
  String getFTPuser, 
  String getFTPPwd, 
  String getFTPFullDwnPath, 
  String getFTPFullLocalPath
)

public FTPDownload(
  String getFTPuser, 
  String getFTPPwd, 
  String getFTPFullDwnPath, 
  int getFTPReTryCount
)

public FTPDownload(
  String getFTPuser, 
  String getFTPPwd, 
  String getFTPFullDwnPath, 
  String getFTPFullLocalPath, 
  int getFTPReTryCount, 
  bool dwnFileFlag
)
```