# 1. Simpan script
nano install-vpn.sh
chmod +x install-vpn.sh

# 2. Jalankan instalasi
sudo ./install-vpn.sh

# 3. Setelah instalasi
vpn-admin

# 4. Navigasi ke menu Auto-Lock
#    Pilih option 3: Auto-Lock System Management
 CARA AUTO-INSTALL DENGAN SATU PERINTAH
1. Buat file README.md di repository Anda (opsional tapi recommended):
markdown

# SSH & VMESS Auto-Lock VPN Manager

Auto installer script untuk VPN dengan SSH dan VMESS lengkap dengan Auto-Lock system.

## 🚀 Instalasi Satu Perintah

bash <(curl -s https://raw.githubusercontent.com/sukronwae85-design/sshvmessautolock/main/install.sh)
    atau

bash

wget -qO- https://raw.githubusercontent.com/sukronwae85-design/sshvmessautolock/main/install.sh | bash

📋 Fitur

  SSH WebSocket (Port 80/443 - NO PATH)

  VMESS WebSocket (Port 80/443 - PATH /vmess)

   UDP Custom untuk game

   Auto-Lock system

  enu management interaktif

text


### **2. Pastikan file `install.sh` sudah ada di root repository:**

Struktur repository Anda harus seperti:

sshvmessautolock/
├── install.sh # Script utama
├── README.md # Dokumentasi
└── (file lainnya jika ada)
text


### **3. Untuk pengguna: Cukup jalankan satu perintah ini:**

**Untuk Ubuntu 18.04/20.04/22.04:**

`bash
PERINTAH SATU BARIS UNTUK INSTALL:
sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/sukronwae85-design/sshvmessautolock/main/install.sh)"

Atau jika mau pakai wget:
bash

sudo wget -qO- https://raw.githubusercontent.com/sukronwae85-design/sshvmessautolock/main/install.sh | sudo bash

4. Alternatif: Buat installer yang lebih simple (buat file setup.sh):
bash

#!/bin/bash
# setup.sh - One-command installer

echo "========================================="
echo "  SSH & VMESS VPN Auto-Installer"
echo "========================================="

# Download and execute install script
curl -sL https://raw.githubusercontent.com/sukronwae85-design/sshvmessautolock/main/install.sh -o /tmp/vpn-install.sh
chmod +x /tmp/vpn-install.sh
bash /tmp/vpn-install.sh

5. Untuk testing di VPS Anda, jalankan:
bash

# Login ke VPS Ubuntu Anda, lalu jalankan:
sudo -i

# Kemudian jalankan perintah ini:
curl -sL https://raw.githubusercontent.com/sukronwae85-design/sshvmessautolock/main/install.sh | bash

🔧 TROUBLESHOOTING:

Jika ada masalah, coba perintah berikut:
bash

# 1. Update sistem dulu
apt-get update && apt-get upgrade -y

# 2. Install curl jika belum ada
apt-get install -y curl wget

# 3. Jalankan dengan verbose
bash -x <(curl -s https://raw.githubusercontent.com/sukronwae85-design/sshvmessautolock/main/install.sh)

# 4. Atau download dulu baru jalankan
wget https://raw.githubusercontent.com/sukronwae85-design/sshvmessautolock/main/install.sh
chmod +x install.sh
./install.sh

📝 CONTOH PROSES INSTALASI:
bash

# Di VPS Ubuntu Anda:
root@vps:~# curl -sL https://raw.githubusercontent.com/sukronwae85-design/sshvmessautolock/main/install.sh | bash

# Akan muncul output:
╔══════════════════════════════════════════════════════════════════╗
║                SSH & VMESS COMPLETE INSTALLATION                 ║
╚══════════════════════════════════════════════════════════════════╝
[*] Checking System Requirements...
[✓] Ubuntu 20.04 detected
[*] Updating System...
[✓] System updated
[*] Installing Dependencies...
...
[✓] Installation Complete!

To start managing:
1. Run: vpn-admin
2. Navigate to Auto-Lock menu
3. Configure your rules

🎯 SINGLE COMMAND READY-TO-USE:

Copy perintah ini untuk share ke user lain:
bash

# INSTALL DENGAN SATU PERINTAH:
sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/sukronwae85-design/sshvmessautolock/main/install.sh)"

# ATAU YANG LEBIH SINGKAT:
curl -sL bit.ly/sshvmess-install | bash   # Jika mau buat shortlink

