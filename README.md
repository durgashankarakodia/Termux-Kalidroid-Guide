# Termux to KaliDroid (Kali Linux) Install Guide

Commands from downloading Termux to installing Kali Linux (proot-distro / NetHunter).

> ⚠️ **Note:** This is for educational / personal learning purposes only. Please use any tool responsibly and only on your own devices.

---

## 1. Install Termux

The Termux app on Google Play Store is outdated and unsupported. Use one of these instead:

- **F-Droid (Recommended):** https://f-droid.org/packages/com.termux/
- **GitHub Releases:** https://github.com/termux/termux-app/releases

---

## 2. Update Termux Packages

```bash
pkg update -y && pkg upgrade -y
```

---

## 3. Install Required Packages

```bash
pkg install wget curl git proot -y
```

---

## 4. Grant Storage Permission

```bash
termux-setup-storage
```

---

## 5. Method A: Install Kali via proot-distro (Recommended - Stable)

```bash
pkg install proot-distro -y
proot-distro install kali-linux
```

### Login to Kali

```bash
proot-distro login kali-linux
```

### Install useful packages inside Kali

```bash
apt update && apt upgrade -y
apt install -y kali-linux-headless
```

---

## 6. Method B: Kali NetHunter (Official Offensive Security Script)

```bash
wget -O install-nethunter-termux https://offs.ec/2MceZWr
chmod +x install-nethunter-termux
./install-nethunter-termux
```

### Start NetHunter

```bash
./start-nethunter.sh
```

---

## 7. GUI in Kali (Optional - with VNC)

```bash
apt install -y kali-desktop-xfce tigervnc-standalone-server
vncserver
```

---

## 8. Common Troubleshooting

```bash
# If storage access is not granted
termux-setup-storage

# If package installation fails
pkg update -y && pkg upgrade -y

# To exit Kali
exit
```

---

## References

- Termux Official: https://termux.dev/
- Kali NetHunter: https://www.kali.org/docs/nethunter/
- proot-distro: https://github.com/termux/proot-distro
