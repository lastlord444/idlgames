# NEXT ACTIONS — Sıradaki Görev

## 🎯 GÖREV #1: Unity 6.3 LTS'e Yükseltme
**Açıklama**: Projeyi Unity Hub üzerinden Unity 6.3 LTS (6000.3.x) ile açarak versiyon yükseltmesi yapmak.

### Done Kriteri:
- [ ] Unity Hub'da proje Unity 6.3 LTS editor ile açılmış
- [ ] Compile error sıfır
- [ ] Play Mode'da Level 1 açılıyor
- [ ] Match3 temel mekanik çalışıyor (3 taş eşleşme)
- [ ] API Updater uyarıları temizlenmiş

### Test Adımları:
1. Unity Hub > Projects > Add > `C:\Unity\idlgames` seç
2. Editor Version: Unity 6.3 LTS seç ve Open
3. "Enter Safe Mode?" sorusu gelirse → No, Open Normally
4. API Updater çalışırsa → "I Made a Backup. Go Ahead!" tıkla
5. Console'u aç → Error/Warning sayısını not et
6. Play → Level 1 test → 3 taş eşleştir → Score arttı mı?
7. Başarılıysa bu dosyayı güncelle, yeni görev yaz

---

## 📌 KUYRUK (Sırada Bekleyenler)
1. Idle progression sistemini Match3 core'a bağla
2. CurrencyManager + UpgradeManager entegrasyon
3. SaveManager implementasyonu
4. TD (Tower Defense) modülü planlama
