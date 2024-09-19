# __UoM DMS Toolkit__ 💻
<br>

JUST OPEN THE  [__UoM_DMS_Toolkit_by_Patric.ipynb__](https://colab.research.google.com/github/patricnilackshan/UoM_DMS_Toolkit/blob/main/UoM_DMS_Toolkit_by_Patric.ipynb) in Google Colab and Run 🧑‍💻
<br>
<br>

# BRIEF EXPLANATION IS GIVEN BELOW

## Introduction 📋
UoM_DMS_Toolkit streamlines file tasks for students at UoM. Enjoy data-free downloads/uploads and multimedia processing, including Torrents, Youtube, M3U8 links. Say goodbye to bandwidth worries and focus on your education! 😁

## Prerequisites 🎯

* Update package lists:

    > sudo apt update -y

<br>

* Install ffmpeg for multimedia processing:

    > sudo apt install ffmpeg -y

<br>

---
### Variable are written inside angular brackets `< >`
---
<br>

## Download File from URL 📥
```bash
wget -O <fileName> <downloadLink>
```

__OR__
```bash
curl -o <fileName> <downloadLink>
```

<br>

## Download M3U8 files to MP4 🔗
```bash
ffmpeg -i <downloadLink> -c copy -threads 8 <fileName>
```

<br>

## Uploading File to DMS 📤
```bash
curl -u <userName>:<userPassword> -T <fileName> "https://dms.uom.lk/remote.php/webdav/"
```

<br>

## Share file from the DMS 🔁
```bash
curl -u <userName>:<userPassword> -X POST -d "path=<fileName>&shareType=3&permissions=1" "https://dms.uom.lk/ocs/v2.php/apps/files_sharing/api/v1/shares?format=json" -H "OCS-APIRequest: true"
```

<br>

## Get details of all shares in DMS Account 📢
```bash
curl -u <userName>:<userPassword> -X GET "https://dms.uom.lk/ocs/v2.php/apps/files_sharing/api/v1/shares?format=json" -H "OCS-APIRequest: true"
```

<br>

## Delete a share with its share_ID 🗑️
```bash
curl -u <userName>:<userPassword> -X DELETE "https://dms.uom.lk/ocs/v2.php/apps/files_sharing/api/v1/shares/<share_ID>" -H "OCS-APIRequest: true"
```

<br>

## Mount DMS WebDAV in My Computer 🖥️ **(OPTIONAL)**

### To map DMS as a local disk in Windows 🪟, run this command in Command Prompt
`
net use Z: https://dms.uom.lk/remote.php/webdav/ /user:<userName> <userPassword>
`

- Replace 'userName' and 'userPassword' with actual values

### To access DMS in Linux 🐧, enter this address in the `Enter server address` field in your File Manager
`
davs://dms.uom.lk/remote.php/webdav/
`

<br>

## Conclusion 😎
This notebook provides a convenient way to interact with the DMS for educational purposes, enabling data-free downloads, uploads, and sharing of files and folders.🧑‍💻

<br>

### © PATRIC NILACKSHAN (pnilackshan@gmail.com)

<img align="right" src="https://visitor-badge.laobi.icu/badge?page_id=patricnilackshan.UoM_DMS_Toolkit" />
