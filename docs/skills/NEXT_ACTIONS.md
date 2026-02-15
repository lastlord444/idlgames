# NEXT ACTIONS — Sıradaki Görev

## 🎯 GÖREV #1: Unity 2021.3.45f2 Güvenli Versiyon Kurulumu + Baseline Build

**Açıklama**: Proje 2021.3.18f1 ile işaretli ama bu versiyonda **Security Alert** var. Unity 2021.3.45f2 (güvenli patch) kurulup proje bu versiyon ile açılacak, Android platform baseline alınacak.

### Done Kriteri:
- [ ] Unity 2021.3.45f2 Unity Hub'a kuruldu
- [ ] `C:\Unity\idlgames` projesi Unity Hub'da 2021.3.45f2 ile **Safe Mode** ile açıldı
- [ ] `ProjectSettings/ProjectVersion.txt` → `m_EditorVersion: 2021.3.45f2` olarak güncellendi
- [ ] Play Mode → Level 1 açıldı, Match3 çalıştı
- [ ] Build Settings → Android platform switch yapıldı
- [ ] Boş Android build başarılı (baseline APK oluşturuldu)
- [ ] Commit: `"baseline: opens on 2021.3.45f2 + android build ok"`

### Detaylı Adımlar:
#### 1. Unity 2021.3.45f2 Kurulum
- Unity Hub > Installs > Install Editor
- Version: **2021.3.45f2** (LTS)
- Modules: Android Build Support (Android SDK & NDK Tools, OpenJDK)

#### 2. Proje Açma (Safe Mode)
- Unity Hub > Projects > Add > `C:\Unity\idlgames` seç
- Editor Version dropdown → **2021.3.45f2** seç
- **Open** → "Enter Safe Mode?" gelirse → **Yes, Enter Safe Mode**
- Safe Mode'da açıldıktan sonra → **Continue Without Safe Mode**

#### 3. ProjectVersion.txt Kontrolü
- `C:\Unity\idlgames\ProjectSettings\ProjectVersion.txt` dosyasını aç
- `m_EditorVersion:` satırını kontrol et
- Eğer `2021.3.18f1` ise → Manuel olarak `2021.3.45f2` yap ve kaydet

#### 4. Play Mode Test
- Editor'de Play butonu tıkla
- Level 1 açılıyor mu?
- 3 taş eşleştir → Score artıyor mu?
- Console'da critical error yok mu?

#### 5. Android Platform Switch
- File > Build Settings
- Platform: **Android** seç
- **Switch Platform** tıkla (birkaç dakika sürebilir)

#### 6. Baseline Build
- Build Settings açık kaldığı yerde
- **Build** tıkla (Build And Run değil)
- Konum: `C:\Unity\idlgames\Builds\Android\baseline_2021.3.45f2.apk`
- Build başarılı olmalı (errors: 0)

#### 7. Commit ve Push
```bash
cd /d C:\Unity\idlgames
git add ProjectSettings/ProjectVersion.txt
git commit -m "baseline: opens on 2021.3.45f2 + android build ok"
git push origin main
```

---

## 📌 KUYRUK (Sırada Bekleyenler)
1. Unity 6.3 LTS'e yükseltme (ileride, stable olduktan sonra)
2. Idle progression sistemini Match3 core'a bağla
3. CurrencyManager + UpgradeManager entegrasyon
4. SaveManager implementasyonu
5. TD (Tower Defense) modülü planlama
