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
  
- **Tüm Wi-Fi şifrelerini görüntüle:**
  ```
  ./fpass.sh -id "EvAğı"

- **Firefox’ta belirli bir siteye ait kayıtlı parolaları görüntüle:**
```
  ./fpass.sh -w github.com
``` 
 
- **Kullanıcı adına göre filtrele:**
 ```  
./fpass.sh -u johndoe
