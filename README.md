# 🔐 Fpass

**Fpass**, Linux sistemlerinde kayıtlı olan **Wi-Fi şifrelerini** ve **Firefox tarayıcı şifrelerini** komut satırından görüntülemenizi sağlayan bir Bash scriptidir. Kullanıcı adı, site adresi veya SSID (Wi-Fi ağı adı) gibi filtrelerle şifreleri hızlıca bulabilirsiniz.

> ⚠️ **Uyarı:** Bu araç yalnızca **kişisel kullanım ve eğitim** amaçlıdır. İzinsiz erişim yasal değildir ve sorumluluk kullanıcıya aittir.

---

## 🛠️ Özellikler

- Wi-Fi profillerinden SSID ve şifreleri gösterir (`/etc/NetworkManager/system-connections`)
- Firefox tarayıcıdan kayıtlı kullanıcı adı ve parolaları listeler
- Filtreleme: site, kullanıcı adı veya SSID
- Komut satırı parametre desteği
- Matrix tarzı yeşil yazı efekti 🎥

---

## ⚙️ Gereksinimler

- Linux tabanlı işletim sistemi
- `sudo` yetkisi
- Python 3
- `7z` yüklü olması (yalnızca 7z içeren örneklerde gerekebilir)
- Firefox kurulu olmalı
- `firefox_decrypt.py` scripti (`fpass.sh` ile aynı dizinde bulunmalı)

---

## 🔧 Kurulum

```bash
git clone https://github.com/erogluyusuf/Fpass.git
cd Fpass
chmod +x fpass.sh
./fpass.sh [PARAMETRELER]
```
### 🧩 Parametreler:

| Parametre        | Açıklama |
|------------------|----------|
| `-w <site>`      | Belirli bir web sitesine ait girişleri filtreler (örn: `-w facebook.com`) |
| `-u <kullanıcı>` | Belirli bir kullanıcı adına ait girişleri filtreler |
| `-wifi`          | Tüm Wi-Fi profillerini ve şifrelerini gösterir |
| `-id <SSID>`     | Belirli SSID'ye (Wi-Fi ağı adı) sahip ağı gösterir |
| `-h, --help`     | Yardım ekranını görüntüler |


### 🔍 Örnekler

- **Tüm Wi-Fi şifrelerini görüntüle:**
  ```bash
  ./fpass.sh -wifi
  
- **Sadece belirli bir SSID için Wi-Fi şifresi al:**
  ```
  ./fpass.sh -id "EvAğı"

- **Firefox’ta belirli bir siteye ait kayıtlı parolaları görüntüle:**
```
  ./fpass.sh -w github.com
``` 
 
- **Kullanıcı adına göre filtrele:**
 ```  
./fpass.sh -u johndoe
```







# 🔐 Fpass

**Fpass** is a Bash script that allows you to view saved **Wi-Fi passwords** and **Firefox browser credentials** on Linux systems directly from the terminal. You can quickly filter results by username, website address, or SSID (Wi-Fi network name).

> ⚠️ **Warning:** This tool is intended for **personal and educational use only**. Unauthorized access is illegal and the responsibility lies with the user.

---

## 🛠️ Features

- Displays SSID and password from saved Wi-Fi profiles (`/etc/NetworkManager/system-connections`)
- Lists saved Firefox usernames and passwords
- Filtering support: by website, username, or SSID
- Command-line parameter support
- Matrix-style green text effect 🎥

---

## ⚙️ Requirements

- Linux-based operating system
- `sudo` privileges
- Python 3
- `7z` installed (only needed for 7z-based scenarios)
- Firefox must be installed
- `firefox_decrypt.py` script must be in the same directory as `fpass.sh`

---

## 🔧 Installation

```bash
git clone https://github.com/erogluyusuf/Fpass.git
cd Fpass
chmod +x fpass.sh
./fpass.sh [OPTIONS]
```

### 🧩 Options:

| Option            | Description |
|-------------------|-------------|
| `-w <website>`    | Filters entries by website (e.g., `-w facebook.com`) |
| `-u <username>`   | Filters entries by username |
| `-wifi`           | Shows all saved Wi-Fi profiles and passwords |
| `-id <SSID>`      | Shows password for a specific SSID |
| `-h, --help`      | Displays the help message |


### 🔍 Examples

- **Show all Wi-Fi passwords:**
  ```bash
  ./fpass.sh -wifi
  
- **Show password for a specific SSID:**
  ```
  ./fpass.sh -id "EvAğı"

- **Show saved Firefox credentials for a specific website:**
```
  ./fpass.sh -w github.com
``` 
 
- **Filter credentials by username:**
 ```  
./fpass.sh -u johndoe
