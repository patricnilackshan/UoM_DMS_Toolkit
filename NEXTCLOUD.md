# NEXTCLOUD API DOCUMENTATION

### Variable are written inside angular brackets `< >`

---

<br>

## Download File from URL 📥

```bash
wget -O <fileName> <downloadLink>
```

**OR**

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

## Mount DMS WebDAV in My Computer 🖥️

### To map DMS as a local disk in Windows 🪟, run this command in Command Prompt

`net use Z: https://dms.uom.lk/remote.php/webdav/ /user:<userName> <userPassword>`

- Replace 'userName' and 'userPassword' with actual values

### To access DMS in Linux 🐧, enter this address in the `Enter server address` field in your File Manager

`davs://dms.uom.lk/remote.php/webdav/`
