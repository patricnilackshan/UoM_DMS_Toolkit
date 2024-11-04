# UoM DMS Toolkit 💻

## Introduction 📋

<div style="text-align: justify;">
The <strong >UoM DMS Toolkit</strong> is designed to streamline file management tasks for students at the University of Moratuwa (UoM). This toolkit allows for data-free downloads/uploads and multimedia processing, including support for Torrents, YouTube videos, and M3U8 links. With this toolkit, you can say goodbye to bandwidth worries and focus on your education! 😁
</div>

### Creator ✨

**Patric Nilackshan**  
Email: [nilackshanp@gmail.com](mailto:nilackshanp@gmail.com)

---

## Features 🌟

- Download files from various sources: 📥
  - Regular files 📄
  - YouTube videos 🎥
  - Torrents 🌐
  - M3U8 streams 📺
- Upload files to UoM DMS 📤
- Share files from DMS 🔗
- Get details of all shares in your DMS account 📋
- Delete shares using Share ID 🗑️
- Mount DMS WebDAV on your computer 💻

---

## Installation 🔧

This toolkit is designed to be used in a Jupyter Notebook environment.

- Open the notebook [UoM DMS Toolkit](https://colab.research.google.com/github/patricnilackshan/UoM_DMS_Toolkit/blob/main/UoM_DMS_Toolkit_by_Patric.ipynb) in Google Colab. 🌐

---

## Usage 🚀

### Sign In to DMS 🔑

Enter your UoM DMS username and password to authenticate.

### Download File from URL 📥

- Enter the download link of the file you wish to download.
- Specify a filename (required only for Torrents and direct downloads).
- Choose between downloading Torrents, regular files, or YouTube videos.

### Upload File to DMS 📤

- Upload the downloaded file to your DMS account.
- Monitor upload progress in real-time ⏳.

### Share File from the DMS 🔄

- Easily create shares for files in your DMS account.
- Obtain a share link for distribution 🔗.

### Manage Shares 📊

- View all shares associated with your DMS account.
- Delete shares using their Share ID 🗑️.

### Mount DMS WebDAV 🖴

- Instructions for mapping DMS as a local disk in Windows and Linux.

#### To map DMS as a local disk in Windows 🪟

Run this command in Command Prompt:

```
net use Z: https://dms.uom.lk/remote.php/webdav/ /user:<userName> <userPassword>
```

- Replace userName and userPassword with your actual values.

#### To access DMS in Linux 🐧

Enter the following address in the `Enter server address` field in your File Manager:

```
davs://dms.uom.lk/remote.php/webdav/
```

---

## Conclusion 😎

The UoM DMS Toolkit provides a convenient way to manage files for educational purposes, enabling data-free downloads, uploads, and sharing of files and folders. 

---

## © Patric Nilackshan
For further information, please refer to the documentation or contact the author at
Email: [nilackshanp@gmail.com](mailto:nilackshanp@gmail.com)

<img align="right" src="https://visitor-badge.laobi.icu/badge?page_id=patricnilackshan.UoM_DMS_Toolkit" />
