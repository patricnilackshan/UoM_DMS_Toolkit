# __UoM DMS Toolkit__ 💻

## Introduction 📋

UoM_DMS_Toolkit streamlines file tasks for students at UoM. Enjoy data-free downloads/uploads and multimedia processing, including Torrents, Youtube, M3U8 links. Say goodbye to bandwidth worries and focus on your education! 😁

<br>

### AN IDEA OF PATRIC NILACKSHAN 🧑‍💻 (pnilackshan@gmail.com)

<br>

## Prerequisites 🎯

- Update package lists:

`
sudo apt update -y
`

- Install ffmpeg for multimedia processing:

`
sudo apt install ffmpeg -y
`

- Variable are written within angular brackets `< >` 

<br>

## Download File from URL 📥

`
wget -O <fileName> <downloadLink>
`
<br>

or
<br>

`
curl -o <fileName> <downloadLink>
`

<br>

## Download M3U8 files to MP4 🔗

`
ffmpeg -i <downloadLink> -c copy -threads 8 <fileName>
`

<br>

## Uploading File to DMS 📤

`
curl -u <userName>:<userPassword> -T <fileName> "https://dms.uom.lk/remote.php/webdav/"
`

<br>

## Share file from the DMS 🔁

`
curl -u <userName>:<userPassword> -X POST -d "path=<fileName>&shareType=3&permissions=1" "https://dms.uom.lk/ocs/v2.php/apps/files_sharing/api/v1/shares?format=json" -H "OCS-APIRequest: true"
`

<br>

## Get details of all shares in DMS Account 📢

`
curl -u <userName>:<userPassword> -X GET "https://dms.uom.lk/ocs/v2.php/apps/files_sharing/api/v1/shares?format=json" -H "OCS-APIRequest: true"
`

<br>

## Delete a share with its share_ID 🗑️
`
curl -u <userName>:<userPassword> -X DELETE "https://dms.uom.lk/ocs/v2.php/apps/files_sharing/api/v1/shares/<share_ID>" -H "OCS-APIRequest: true"
`

<br>

### Mapping DMS WebDAV Share (For Windows OS) 🪟

- Run this command in a new Command Prompt in Windows to see DMS as a Local Disk in My Computer

`
net use Z: https://dms.uom.lk/remote.php/webdav/ /user:<userName> <userPassword>
`

<br>

## Conclusion 😎
These CLI codes provide a convenient way to interact with the DMS for educational purposes, enabling data-free downloads, uploads, and sharing of files and folders.🧑‍💻

<br>

### © PATRIC NILACKSHAN (pnilackshan@gmail.com)
