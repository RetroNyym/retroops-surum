# retroops-surum — RetroOps sürüm takip dosyası

> **EN:** Single-file version manifest (`surum.json`) consumed by the RetroOps
> desktop app's update checker: current version, download URL and release note.

RetroOps masaüstü uygulaması (**[RetroOps](https://github.com/RetroNyym/RetroOps)**
indirme sayfası, kaynak kodu **[Retronym](https://github.com/RetroNyym/Retronym)**)
açılışta bu depodaki `surum.json` dosyasını okur; dosyadaki `surum` değeri
yerel sürümden yeniysa kullanıcıya güncelleme uyarısı gösterilir.

## Dosya

```json
{
  "surum": "1.1.0",
  "indirme": "https://github.com/RetroNyym/RetroOps/releases/download/v1.1.0/RetroOps-v1.1.0.zip",
  "not": "1.1.0: SMS entegrasyonu, kargo API baglantilari ve guncelleme uyarisi eklendi."
}
```

| Alan | Açıklama |
|---|---|
| `surum` | Yayındaki en son sürüm (`MAJOR.MINOR.PATCH`) |
| `indirme` | Doğrudan indirme adresi (GitHub Releases) |
| `not` | Kullanıcıya gösterilecek sürüm notu |

## Yayınlama

Yeni sürüm çıkınca:

1. Uygulama paketini GitHub Releases'a yükleyin.
2. `surum.json` içindeki üç alanı güncelleyin.
3. Bu depoda commit + push edin — güncelleme kontrolü anında yayılır.
