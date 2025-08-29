## 🖥️ TeamViewer Setup Guide

### ✅ What is TeamViewer?

**TeamViewer** is a widely used remote desktop application that allows you to connect to computers and mobile devices from anywhere. It supports remote control, file transfer, online meetings, and cross-platform connectivity (Windows, Linux, macOS, Android, iOS).

---

### 🖥️ Step 1: Install TeamViewer

#### Arch Linux (using yay):

```bash
yay -S teamviewer
````

This installs TeamViewer from the AUR.

#### Debian/Ubuntu:

1. Add the TeamViewer repository:

```bash
wget -O - https://download.teamviewer.com/download/linux/signature/TeamViewer2017.asc | sudo apt-key add -
sudo sh -c 'echo "deb http://linux.teamviewer.com/deb stable main" >> /etc/apt/sources.list.d/teamviewer.list'
```

2. Update and install:

```bash
sudo apt update
sudo apt install teamviewer
```

#### Fedora:

```bash
sudo dnf install https://download.teamviewer.com/download/linux/teamviewer.x86_64.rpm
```

#### Windows:

Download the installer from the [official website](https://www.teamviewer.com/en/download/windows/) and run the `.exe` file.

#### macOS:

Download the `.dmg` from [TeamViewer macOS](https://www.teamviewer.com/en/download/mac-os/) and drag it to your Applications folder.

---

### ⚙️ Step 2: Launch TeamViewer

Open TeamViewer from your applications menu or run:

```bash
teamviewer
```

On first launch, TeamViewer will display your **ID** and **password**. Share them carefully to allow remote connections.

---

### 🔧 Step 3: Configure Permissions (Linux)

On Linux, ensure TeamViewer has required permissions:

* Screen sharing / recording
* Clipboard access
* Audio (if needed)

Some desktop environments (GNOME, KDE) may require you to approve permissions in system settings.

---

### 🛡️ Step 4: Security Tips

* Only share your TeamViewer ID and password with trusted people.
* Use **random passwords** for unattended access instead of static passwords.
* Enable **Two-Factor Authentication** for your TeamViewer account.
* Keep TeamViewer updated to the latest version.

---

### 🚀 Step 5: Optional: Start TeamViewer at Boot

#### Systemd (Linux):

```bash
sudo systemctl enable teamviewerd.service
sudo systemctl start teamviewerd.service
```

This ensures TeamViewer runs in the background and is ready for remote access after system startup.

---

### 📚 Additional Resources

* Official Website: [https://www.teamviewer.com](https://www.teamviewer.com)
* Arch Wiki: [TeamViewer](https://wiki.archlinux.org/title/TeamViewer)
* Man page: `man teamviewer`

```
