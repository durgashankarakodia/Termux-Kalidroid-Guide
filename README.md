# Termux se KaliDroid (Kali Linux) Install Guide

Termux download se lekar Kali Linux (proot-distro / NetHunter) install karne tak ki commands.

> ⚠️ **Note:** Yeh sirf educational / personal learning purpose ke liye hai. Kisi bhi tool ka use responsibly aur apne devices par hi karein.

---

## 1. Termux Install Karein

Google Play Store wala Termux purana aur unsupported hai. Inme se koi ek use karein:

- **F-Droid (Recommended):** https://f-droid.org/packages/com.termux/
- **GitHub Releases:** https://github.com/termux/termux-app/releases

---

## 2. Termux Packages Update Karein

```bash
pkg update -y && pkg upgrade -y
```

---

## 3. Zaroori Packages Install Karein

```bash
pkg install wget curl git proot -y
```

---

## 4. Storage Permission Dein

```bash
termux-setup-storage
```

---

## 5. Method A: proot-distro se Kali Install (Recommended - Stable)

```bash
pkg install proot-distro -y
proot-distro install kali-linux
```

### Kali Login Karein

```bash
proot-distro login kali-linux
```

### Kali ke andar useful packages install karein

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

### NetHunter Start Karein

```bash
./start-nethunter.sh
```

---

## 7. Kali me GUI (Optional - VNC ke saath)

```bash
apt install -y kali-desktop-xfce tigervnc-standalone-server
vncserver
```

---

## 8. Common Troubleshooting

```bash
# Agar storage access na mile
termux-setup-storage

# Agar package install fail ho
pkg update -y && pkg upgrade -y

# Kali se bahar nikalne ke liye
exit
```

---

## References

- Termux Official: https://termux.dev/
- Kali NetHunter: https://www.kali.org/docs/nethunter/
- proot-distro: https://github.com/termux/proot-distro
