# REGRESSION GUARD — Gerileme Önleme

## 🔍 SANITY CHECKS (Değişiklik Öncesi/Sonrası)

### ÖNCESİ:
1. **Editor aç** → Compile error yok mu?
2. **Play Mode** → Level 1, 2, 3 açılıyor mu?
3. **Match3** → 3 taş eşleştirme çalışıyor mu?
4. **Save/Load** → Para/progress kaydediliyor mu?
5. **Console** → Error/Warning temiz mi?

### SONRASI (aynı checks):
1. Editor'i yeniden aç
2. Play Mode → 3 level test
3. Match3 → combo mechanic çalışıyor mu?
4. Save/Load → Progress korundu mu?
5. Console → Yeni error var mı?

## ⚡ TEK SEFERDE TEK PROBLEM KURALI
- **BİR commit = BİR değişiklik**
- Aynı anda Match3 fix + Idle upgrade GİBMEZ
- Her commit sonrası sanity check

## 🔄 ROLLBACK PLANI
```bash
# Son commit başarısızsa:
git revert HEAD

# Belirli bir commite dön:
git reset --hard <commit-sha>

# Force push (DİKKAT: sadece local branch):
git push --force
```

## 🚨 KRİTİK DOSYALAR (DOKUNMAK YASAK)
- `Assets/Scripts/GameGrid.cs` — Match3 oynanış
- `Assets/Scripts/GamePiece.cs` — Taş mantığı
- `Assets/Scripts/ClearablePiece.cs` — Temizleme logic

## ���� TEST SENARYOLARI
1. **Basic Match3**: 3 taş yan yana koy → patlamalı
2. **Combo**: 4 taş → özel taş oluşmalı
3. **Level Complete**: Hedef skora ulaşma → level geçiş
4. **Idle Income**: Para kazanma ve upgrade satın alma
5. **Save/Load**: Oyunu kapat/aç → progress aynı olmalı

## 📋 CHECKLIST TEMPLATE
```markdown
- [ ] Editor açıldı mı?
- [ ] Compile error yok mu?
- [ ] Level 1 açıldı mı?
- [ ] Match3 çalışıyor mu?
- [ ] Save/Load çalışıyor mu?
- [ ] Console temiz mi?
```
