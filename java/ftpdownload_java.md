# FTPDownload.java

<script type="text/javascript" src="../js/general.js"></script>

### API description
---

* constructor (建構子)

```Java
public FTPDownload (
    String getFTPHost,
    int getFTPPort,
    String getFTPUser,
    String getFTPPwd,
    String getFTPDwnFilePath,
    String getFTPLocalFilePath
) {
    // download as file and file name is the same 
    ftpHost = getFTPHost;
    ftpPort = getFTPPort;
    ftpUser = getFTPUser;
    ftpPwd = getFTPPwd;
    ftpFullDownloadFilePath = getFTPDwnFilePath;
    ftpFullLocalFilePath = getFTPLocalFilePath;
    setOthersParameters("dwnFileAndSameName");
}

public FTPDownload (
    String getFTPHost,
    int getFTPPort,
    String getFTPUser,
    String getFTPPwd,
    String getFTPDwnFilePath
) {
    // download as data stream in string type
    ftpHost = getFTPHost;
    ftpPort = getFTPPort;
    ftpUser = getFTPUser;
    ftpPwd = getFTPPwd;
    ftpFullDownloadFilePath = getFTPDwnFilePath;
    setOthersParameters("dwnAsStringStream");
}
```

###API Example
---