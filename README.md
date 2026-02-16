# Unity Match3-SDK Block Blast Skeleton

Unity 6 (6000.3.8f1 LTS) üzerinde **[Match3-SDK](https://github.com/LibraStack/Match3-SDK)** kullanarak Block Blast tarzı puzzle oyunu geliştirme projesi.

## 📋 Proje Bilgileri

- **Unity Sürümü:** 6000.3.8f1 (Unity 6 LTS)
- **Platform:** Windows, Android (hedef)
- **SDK:** Match3-SDK (MIT License)
- **Ek Paketler:** UniTask, DOTween
- **Branch:** `skeleton/match3sdk`

## 🎯 Proje Durumu

✅ **Skeleton Kurulumu Tamamlandı**
- [x] Match3-SDK Unity sample projesi entegre edildi
- [x] Unity 6.3 LTS uyumluluğu sağlandı
- [x] Git repo yapısı kuruldu
- [x] Dokümentasyon hazırlandı

⏳ **Sırada:**
- [ ] Android Build Support kurulumu (Unity Hub GUI'den manuel)
- [ ] Match3 mekaniklerini Block Blast'a dönüştürme
- [ ] 8x8 sabit grid sistemi
- [ ] Blok şekilleri ve drag & drop

## 📁 Proje Yapısı

```
idlgames/
├── Assets/
│   ├── Art/               # Sprite'lar, texture'lar
│   ├── Prefabs/          # Tile ve item prefab'ları
│   ├── Scenes/           # MainScene.unity
│   ├── Scripts/          # Game logic
│   └── Plugins/          # DOTween vb.
├── Packages/
│   ├── manifest.json     # Package bağımlılıkları
│   └── packages-lock.json
├── ProjectSettings/      # Unity proje ayarları
└── docs/
    ├── MENTOR_CHECKLIST.md  # Geliştirme kontrol listesi
    └── TODO_NEXT.md        # Block Blast dönüşüm adımları
```

## 🚀 Kurulum

### 1. Repo'yu Klonla
```bash
git clone https://github.com/lastlord444/idlgames.git
cd idlgames
git checkout skeleton/match3sdk
```

### 2. Unity Hub'dan Aç
- Unity Hub > Add > Proje klasörünü seç
- Unity sürümü: **6000.3.8f1** seçilmeli
- Proje ilk açılışta package import yapacak (~2-3 dakika)

### 3. Android Build Support (Opsiyonel)
Unity Hub > Installs > 6000.3.8f1 > Add Modules:
- ✅ Android Build Support
- ✅ Android SDK & NDK Tools
- ✅ OpenJDK

## 🎮 Test Etme

1. Unity Editor'de `Assets/Scenes/MainScene.unity` sahnesini aç
2. Play butonuna bas
3. Match3 demo oynanabilir olmalı

**Beklenen:** Console'da 0 error, oyun çalışır durumda.

## 📚 Dokümanlar

- **[MENTOR_CHECKLIST.md](docs/MENTOR_CHECKLIST.md):** Her değişiklik öncesi kontrol listesi
- **[TODO_NEXT.md](docs/TODO_NEXT.md):** Block Blast'a dönüşüm roadmap

## 🛠️ Teknoloji Stack

| Kategori | Teknoloji |
|----------|-----------|
| Engine | Unity 6000.3.8f1 (LTS) |
| Grid System | Match3-SDK |
| Async | UniTask |
| Animation | DOTween |
| UI | TextMeshPro |
| Build | IL2CPP + ARM64 |

## ⚠️ Önemli Notlar

1. **Unity Sürümü:** Kesinlikle 6000.3.x LTS kullanılmalı (2021.3 uyumsuz)
2. **Package Manager:** GitHub'dan paket çekiyor, internet gerekli
3. **Android:** Manuel module kurulumu gerekiyor (Unity Hub CLI çalışmıyor)
4. **Match3 Mantığı:** Erken aşamada devre dışı bırakılmalı (Block Blast için)

## 🔗 Bağlantılar

- **Repo:** https://github.com/lastlord444/idlgames
- **Branch:** https://github.com/lastlord444/idlgames/tree/skeleton/match3sdk
- **Match3-SDK:** https://github.com/LibraStack/Match3-SDK
- **UniTask:** https://github.com/Cysharp/UniTask

## 📝 Lisans

- **Proje:** TBD
- **Match3-SDK:** MIT License
- **DOTween:** Free version (HOTween v2)

---

**Son Güncelleme:** 2026-02-16  
**Geliştirici:** @lastlord444  
**Durum:** 🟢 Skeleton Hazır
