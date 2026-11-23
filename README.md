# Old-web

Windows XP / Internet Explorer gibi eski tarayıcılardan modern (HTTPS) sitelere girmek için
**ücretsiz** WebOne proxy sunucusu. GitHub Actions üzerinde çalışır, bore tüneli ile dışarı açılır.

## Nasıl çalışır?
- `webone.yml` workflow'u WebOne'ı kurar, şifreli (Basic auth) başlatır ve `bore.pub` üzerinden açar.
- Yaklaşık **5 saat** çalışır, sonra kapanır ve **~1 dakika** içinde kendini yeniden başlatır.
- Güncel adres her turda `status/address.txt` dosyasına yazılır (genelde `bore.pub:40080`).

## Eski bilgisayarda kurulum (Windows XP + Internet Explorer)
1. `status/address.txt` dosyasındaki **host** ve **port** değerlerine bak.
2. Internet Explorer: **Araçlar → İnternet Seçenekleri → Bağlantılar → LAN Ayarları**
3. "Proxy sunucusu kullan" kutusunu işaretle, **Adres:** `bore.pub`, **Bağlantı noktası:** `40080` (dosyadaki port) yaz, Tamam.
4. Bir siteye girince kullanıcı adı/şifre sorar: kullanıcı adı `old`, şifre repo sahibinde.
5. Siteleri her zamanki gibi aç, HTTPS siteler de açılır.

## Kesinti olursa
Her 5 saatte bir ~1 dakikalık kopma normaldir. Sayfa açılmazsa 1-2 dakika bekleyip yenile.
Adres değiştiyse `status/address.txt` dosyasına tekrar bak.

## Sahibi için
- Şifre: repo **Settings → Secrets → Actions → `PROXY_PASS`**
- Sabit port istersen: **Settings → Variables → `BORE_PORT`** (varsayılan 40080)
- İlk başlatma: **Actions → webone → Run workflow** (sonra kendi kendine devam eder)
