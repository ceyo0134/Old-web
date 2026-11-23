# Old-web

Windows XP / Internet Explorer gibi eski tarayıcılardan modern (HTTPS) sitelere girmek için
**ücretsiz ve herkese açık** WebOne proxy sunucusu. GitHub Actions üzerinde çalışır, bore tüneli ile dışarı açılır.

## Proxy bilgileri (herkes kullanabilir, şifre yok)

| | |
|---|---|
| Adres | `bore.pub` |
| Port | `40080` |

Port değişirse güncel adres `status/address.txt` dosyasındadır.

## Kurulum (Windows XP + Internet Explorer)
1. **Araçlar → İnternet Seçenekleri → Bağlantılar → LAN Ayarları**
2. "Proxy sunucusu kullan" kutusunu işaretle, Adres: `bore.pub`, Bağlantı noktası: `40080`, Tamam.
3. Bitti, şifre sorulmaz. Siteyi aç, HTTPS siteler de açılır.

## Modern tarayıcı indir: Supermium
Supermium, Windows XP (SP3), 2003, Vista, 7, 8.x ve üstünde çalışan güncel Chromium tabanlı tarayıcıdır.
Proxy'yi kurduktan sonra aşağıdan indir (sürüm 150.0.7871.289 R3):

- **32-bit kurulum (XP için en uygunu):** https://github.com/win32ss/supermium/releases/download/v150-r3/supermium_150_32_setup.exe
- 32-bit zip (kurulumsuz): https://github.com/win32ss/supermium/releases/download/v150-r3/supermium_150_32_nonsetup.zip
- 64-bit kurulum (XP x64 / Vista / 7 / 8): https://github.com/win32ss/supermium/releases/download/v150-r3/supermium_150_64_setup.exe
- 64-bit zip: https://github.com/win32ss/supermium/releases/download/v150-r3/supermium_150_64_nonsetup.zip
- Windows 10/11 için: https://github.com/win32ss/supermium/releases/download/v150-r3/supermium_150_64_setup_win10_11.exe
- Hep güncel sürüm: https://github.com/win32ss/supermium/releases/latest

Sade indirme sayfası (IE uyumlu): https://ceyo0134.github.io/Old-web/

## Kesinti
Her 5 saatte bir ~1 dakikalık kopma normaldir. Sayfa açılmazsa 1-2 dakika bekleyip yenile.
